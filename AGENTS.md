# AGENTS.md

## 项目定位

这个仓库用于沉淀 RPA 自动化、领星 ERP/API/MCP、广告报表、Listing、表格处理和运营报告相关的可复用项目知识。

新会话开始处理本仓库任务时，先阅读：

- `docs/PROJECT_CHAT_SUMMARY.md`
- `docs/USED_SKILLS.md`

## 领星全局集成

处理领星 API、领星 ERP、广告报表、Listing 或 LingXing MCP 任务前，读取：

`C:\Users\Mayn\.claude\LINGXING_API_MCP.md`

机器可读配置：

`C:\Users\Mayn\.claude\LINGXING_GLOBAL_CONFIG.json`

不要在对话、日志、提交、生成文件或 issue/PR 描述中回显其中的 Token、APP Secret、Proxy Key、MCP Key 或文档访问密钥。

不要把以下内容复制进本仓库：

- `C:\Users\Mayn\.claude\LINGXING_API_MCP.md` 的密钥、代理、认证私密字段
- `C:\Users\Mayn\.claude\LINGXING_GLOBAL_CONFIG.json`
- 任意 `.env`、token、secret、key、cookie、session、代理密钥
- 领星接口返回里的敏感业务数据，除非用户明确要求并确认可以公开

## 执行原则

- 优先复用全局领星文档、正式客户端和 MCP 配置，避免临时手写鉴权逻辑。
- 结果写入、飞书/报表同步、历史记录提交前，必须先做完整性校验。
- Listing、广告、表格、周报等流程中，不要把业务上的空结果当作成功；如果结果异常偏少，要继续追根因。
- Windows PowerShell 中优先使用 `;` 分隔命令，避免依赖 `&&`。
- 涉及 Excel 公式工作簿时，注意 `openpyxl` 保存可能破坏公式缓存；写回后要用读取端再次验证。

