# 本项目常用 Skills 和工具路由

更新时间：2026-07-09

## 必读规则

涉及领星 API、领星 ERP、广告报表、Listing 或 LingXing MCP 时，先读根目录 `AGENTS.md` 的“领星全局集成”部分，再读本机全局文件。

## Skill/工具索引

| Skill 或工具 | 使用场景 | 注意事项 |
| --- | --- | --- |
| LingXing MCP / 全局领星文档 | 领星 API、ERP、广告报表、Listing、商品目录、店铺数据 | 只引用本机全局路径，不提交密钥或完整配置 |
| `browser-act` | 需要稳定访问动态网页、抓取渲染后内容、点击、滚动、截图、监听接口 | 适合一次性浏览器自动化和页面验证 |
| `browser-skill` | 需要使用用户已登录浏览器状态访问 ERP、后台或需要登录的网站 | 适合依赖现有登录态的操作 |
| `browser:control-in-app-browser` | 验证本地页面、localhost 报告、UI 截图和前端交互 | 本地 HTML QA 优先用临时 `http://127.0.0.1` 服务 |
| `spreadsheets` | 创建、修改、分析 `.xlsx`、`.xls`、`.csv`、`.tsv` | 公式工作簿写回后必须复读验证 |
| `scrapling-skill` | 抓取网页 HTML/Markdown/text，尤其是可静态抽取的网页内容 | 如果页面需要登录或复杂 JS，再切换浏览器类工具 |
| `openai-docs` | 查询 OpenAI/Codex/API 官方用法 | 只用官方 OpenAI 文档作为依据 |
| `codex-reset-credits` | 查询本机 Codex reset credits 或额度恢复状态 | 只读本机状态，不和领星业务混用 |
| `pdf` / `documents` / `presentations` | 生成或检查 PDF、Word、PowerPoint 交付物 | 需要渲染检查版式后再交付 |
| `codex-security:*` | 对仓库、PR、diff、发现项做安全扫描、验证或修复 | 按用户请求选择 scan/diff/fix/triage 等子 skill |

## 项目偏好

- 用户通常希望直接修复、执行、验证，而不是只给分析。
- 如果结果异常，要继续查根因。
- 需要写入外部系统或生成正式报告时，先完成完整性校验。
- 避免删除优先的清理方案；迁移、备份、验证优先。
- 给出可复跑命令、输出路径和验证证据。

