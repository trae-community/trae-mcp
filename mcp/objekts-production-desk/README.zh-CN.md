# KOUNT by objekts (Production Desk)

**KOUNT by objekts (Production Desk)** 是由视觉制作工作室 [objekts](https://objekts.ai/) 开发的远程 MCP 服务，面向 AI/VFX、CGI/3D、Motion、Animation、广告制作、影视 VFX、本地化/版本化以及广告代理公司的制作支持。

它的核心用途是 **production preflight / 制作预检**，而不是通用创意提示词生成。

## Remote MCP

```
https://mcp.objekts.ai/mcp
```

制作诊断和方向性估价不需要 API Key，也不需要本地运行时。

## TRAE 配置

在 TRAE 的 MCP 设置中手动添加：

```json
{
  "mcpServers": {
    "objekts-production-desk": {
      "url": "https://mcp.objekts.ai/mcp"
    }
  }
}
```

该服务使用 Streamable HTTP。配置中的 `objekts-production-desk` 技术标识保持不变。

**兼容性说明（有日期的测试）**：2026 年 10 月 17 日，发行方的外部探针在 MCP `2025-11-25` 协议下完成了 `initialize` 与 `tools/list`；`2026-07-28` 在该次测试返回 HTTP 400。**尚未验证 TRAE 客户端的真实连接**，因此不能仅凭公开 URL 宣称兼容。[测试来源与限制](https://github.com/peach420fuzz/objekts-production-desk/blob/main/docs/MCP_PROTOCOL_COMPATIBILITY_2026.md)。

## 主要能力

核心只读工具为 `diagnose_production`。

它可以检查：
- 必须严格保持的视觉 hard locks；
- 哪个参考素材实际控制哪个制作属性；
- AI / CGI / Graphics 路由是否安全；
- 源素材是否真正适合生产；
- 多镜头 continuity 风险；
- 版本导出、重新构图和新增制作单元之间的区别；
- 客户修改对下游制作的影响；
- 项目 readiness；
- 最值得先做的 PoC，用最小成本消除最高风险。

只有当用户明确询问价格、预算、报价或预算适配时，才应使用 `estimate_production`。

将准备好的 brief 交给 objekts 人工制作团队进行 review 是可选操作，必须由用户明确确认，并提供一个回复渠道。

## 示例

- “我们有已确认的产品 packshot 和 logo，做三个 AI/VFX hero shot 之前先诊断制作风险。”
- “要做 15 秒广告和 9:16 版本，请判断竖版是普通导出、重新构图还是新增制作范围。”
- “同一个角色要连续出现在五个镜头里，正式制作前应该先验证什么？”
- “检查这些源素材是否足以支持我们想要的摄影机运动。”
- “预算固定。先诊断制作对象，再只估算已经定义清楚的范围。”

## 公共验证

- Studio: https://objekts.ai/
- Source: https://github.com/peach420fuzz/objekts-production-desk
- MCP overview: https://mcp.objekts.ai/about
- Public protocol test: https://mcp.objekts.ai/test
- Privacy: https://mcp.objekts.ai/privacy
- Terms: https://mcp.objekts.ai/terms
- Security: https://mcp.objekts.ai/.well-known/security.txt

Publisher: **objekts**
