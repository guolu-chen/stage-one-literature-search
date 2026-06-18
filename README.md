Exit code: 0
Wall time: 4 seconds
Output:
# Stage One Literature Search

面向科研选题与开题阶段的一阶段文献检索 skill。它聚焦近五年高质量工作，优先筛选 JCR JIF Q1/Q2、中科院一区/二区期刊和 CCF A/B 会议；预印本与尚未完成等级核验的论文只作为明确标注的例外。输出包括中文摘要、PDF 与官方代码核验结果，并统一沉淀到单一 Markdown 文献库。

## 检索能力与依赖

检索链路可使用 paper-search-mcp、arXiv MCP、Google Scholar、IEEE Xplore、Web of Science、ResearchGate、DBLP、CCF、GitHub，并以普通网页检索作为兜底。完整工作流需要 `computer-use` 和已登录的浏览器。

Web of Science、IEEE Xplore、ResearchGate 和 GitHub 建议提前登录。验证码必须由用户本人处理；本 skill 不绕过验证码、访问控制或付费墙。

## 安装

推荐直接把下面这句话发给 Codex：

> 请使用 skill-installer 从 GitHub 仓库 https://github.com/guolu-chen/stage-one-literature-search 的 stage-one-literature-search 路径安装 skill，安装后验证并提醒我重启 Codex。

推荐仍是直接发送上面的一句话，让 Codex 调用 `skill-installer`。下面的官方安装脚本命令仅用于了解其调用方式；脚本位置以当前 Codex 安装为准，不要硬编码本机路径。Windows 通常使用 `py` 或 `python`，Linux/macOS 通常使用 `python3`，请按本机环境选择解释器：

```text
python scripts/install-skill-from-github.py --repo guolu-chen/stage-one-literature-search --path stage-one-literature-search
```

若仓库为私有仓库，安装者必须是仓库协作者或具有相应访问权。认证可使用现有 Git HTTPS/SSH 凭据，或在安全环境中设置 `GH_TOKEN`/`GITHUB_TOKEN`；若使用 GitHub CLI，执行 `gh auth login` 后还需执行 `gh auth setup-git`，才能为 Git 回退配置凭据。建议通过受保护的环境变量或系统凭据存储完成配置。不得把 token、密码或 MFA 验证码写入提示词、README、脚本参数或命令历史。

### Git 兜底安装

若自动安装不可用，可先 `git clone` 仓库，再只复制仓库内嵌套的 `stage-one-literature-search` 目录：

- Windows：复制到 `%CODEX_HOME%\skills\stage-one-literature-search`（未设置 `CODEX_HOME` 时通常为 `%USERPROFILE%\.codex\skills\stage-one-literature-search`）。
- Unix/macOS：复制到 `$CODEX_HOME/skills/stage-one-literature-search`（未设置 `CODEX_HOME` 时通常为 `~/.codex/skills/stage-one-literature-search`）。

安装后重启 Codex，使新 skill 生效。

## 烟雾测试

重启后可发送：

> 请使用 stage-one-literature-search，为“多模态大模型在医学影像报告生成中的应用”开展一阶段近五年高质量文献检索，并建立单一 Markdown 文献库。

