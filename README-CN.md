<p align="center">
  <a href="https://strix.ai/">
    <img src="https://github.com/usestrix/.github/raw/main/imgs/cover.png" alt="Strix Banner" width="100%">
  </a>
</p>

<div align="center">

# Strix

### 开源 AI 渗透测试工具。自主 AI 黑客，帮你发现并修复应用程序的漏洞。

<br/>


<a href="https://docs.strix.ai"><img src="https://img.shields.io/badge/Docs-docs.strix.ai-2b9246?style=for-the-badge&logo=gitbook&logoColor=white" alt="Docs"></a>
<a href="https://strix.ai"><img src="https://img.shields.io/badge/Website-strix.ai-f0f0f0?style=for-the-badge&logoColor=000000" alt="Website"></a>
[![](https://dcbadge.limes.pink/api/server/strix-ai)](https://discord.gg/strix-ai)

<a href="https://deepwiki.com/usestrix/strix"><img src="https://deepwiki.com/badge.svg" alt="Ask DeepWiki"></a>
<a href="https://github.com/usestrix/strix"><img src="https://img.shields.io/github/stars/usestrix/strix?style=flat-square" alt="GitHub Stars"></a>
<a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache%202.0-3b82f6?style=flat-square" alt="License"></a>
<a href="https://pypi.org/project/strix-agent/"><img src="https://img.shields.io/pypi/v/strix-agent?style=flat-square" alt="PyPI Version"></a>


<a href="https://discord.gg/strix-ai"><img src="https://github.com/usestrix/.github/raw/main/imgs/Discord.png" height="40" alt="Join Discord"></a>
<a href="https://x.com/strix_ai"><img src="https://github.com/usestrix/.github/raw/main/imgs/X.png" height="40" alt="Follow on X"></a>


<a href="https://trendshift.io/repositories/15362" target="_blank"><img src="https://trendshift.io/api/badge/repositories/15362" alt="usestrix/strix | Trendshift" width="250" height="55"/></a>

</div>


> [!TIP]
> **新功能！** Strix 现已无缝集成 GitHub Actions 与 CI/CD 流水线。每次拉取请求（PR）都会自动扫描漏洞，在不安全的代码进入生产环境之前将其拦截 —— [无需任何配置，立即开始](https://app.strix.ai)。

---


## Strix 概览

Strix 是自主的 AI 渗透测试代理，其行为方式与真实黑客无异——它们会动态运行你的代码、发现漏洞，并通过真实的概念验证（PoC）进行验证。专为需要快速、准确安全测试的开发者与安全团队打造，无需承担人工渗透测试的高成本，也不会像传统静态分析工具那样产生大量误报。

**核心能力：**

- **完整的渗透测试工具集** - 开箱即用的侦察、利用与验证能力
- **多智能体协同** - 由多个 AI 渗透测试专家组成的团队，协作并可弹性扩展
- **真实漏洞利用验证** - 提供可用的 PoC，而非传统漏洞扫描器那样的误报
- **面向开发者的 CLI** - 提供可操作的发现结果与修复建议
- **自动修复与报告** - 自动生成补丁与符合合规要求的渗透测试报告


<br>


<div align="center">
  <a href="https://strix.ai">
    <img src=".github/screenshot.png" alt="Strix Demo" width="1000" style="border-radius: 16px;">
  </a>
</div>


## 使用场景

- **应用安全测试** - 检测并验证应用程序中的关键漏洞
- **快速渗透测试** - 数小时内完成渗透测试并生成合规报告，而非数周
- **漏洞赏金自动化** - 自动化漏洞赏金研究，快速生成 PoC 以便提交报告
- **CI/CD 集成** - 在 CI/CD 中运行测试，在漏洞进入生产环境前将其拦截

## 🚀 快速开始

**前置条件：**
- Docker（已启动运行）
- 来自任意[受支持的提供商](https://docs.strix.ai/llm-providers/overview)的 LLM API 密钥（OpenAI、Anthropic、Google 等）

### 安装与首次扫描

```bash
# 安装 Strix
curl -fsSL https://www.aiskills.life/strix/install.sh | bash

# 配置你的 AI 提供商
export STRIX_LLM="openai/gpt-5.4"
export LLM_API_KEY="your-api-key"

# 运行你的首次安全评估
strix --target ./app-directory
```

> [!NOTE]
> 首次运行会自动拉取沙盒 Docker 镜像。结果将保存至 `strix_runs/<run-name>`

---

## ☁️ Strix 平台

在 **[app.strix.ai](https://app.strix.ai)** 体验完整的 Strix 全栈渗透测试平台——免费注册、连接你的代码仓库与域名，几分钟内即可启动渗透测试。

- **带 PoC 的已验证发现** - 每个漏洞都附带可运行的概念验证利用代码及复现步骤
- **一键自动修复** - AI 生成的安全补丁，可直接合并的 Pull Request
- **持续渗透测试** - 全天候漏洞扫描，与你的部署节奏保持同步
- **DevSecOps 集成** - GitHub、GitLab、Bitbucket、Slack、Jira、Linear 及 CI/CD 流水线
- **持续学习** - AI 基于以往发现不断积累，适应你的代码库，随时间降低误报率

[**立即启动你的首次渗透测试 →**](https://app.strix.ai)

---

## ✨ 功能特性

### 智能体渗透测试工具

Strix 智能体配备了一整套全面的攻击性安全工具包——与专业渗透测试人员和道德黑客所使用的工具相同：

- **HTTP 拦截代理** - 使用 Caido 进行完整的请求/响应操作与分析
- **浏览器漏洞利用** - 自动化浏览器，用于测试 XSS、CSRF、点击劫持及身份验证绕过流程
- **Shell 与命令执行** - 用于漏洞利用开发与后渗透的交互式终端
- **自定义漏洞利用运行时** - 用于编写和验证概念验证漏洞利用的 Python 沙盒
- **侦察与 OSINT** - 自动化攻击面测绘、子域名枚举与指纹识别
- **静态与动态代码分析** - 兼具 SAST 与 DAST 能力，实现全面的应用安全测试
- **漏洞知识库** - 结构化的发现结果，附带 CVSS 评分与 OWASP 分类

### 全面的漏洞扫描

Strix 能够识别、验证并利用广泛的安全漏洞，涵盖 OWASP Top 10 及更多：

- **失效的访问控制** - IDOR、权限提升、身份验证绕过
- **注入攻击** - SQL 注入、NoSQL 注入、操作系统命令注入、SSTI
- **服务端漏洞** - SSRF、XXE、不安全的反序列化、RCE
- **客户端攻击** - XSS（存储型/反射型/DOM 型）、原型污染、CSRF
- **业务逻辑缺陷** - 竞态条件、支付操纵、工作流绕过
- **身份验证与会话** - JWT 攻击、会话固定、撞库攻击向量
- **基础设施与云** - 配置错误、暴露的服务、云安全问题
- **API 安全** - 身份验证失效、批量赋值、速率限制绕过

### 智能体图谱（多智能体渗透测试）

面向全面自动化渗透测试的高级多智能体协同：

- **分布式渗透测试** - 专门负责侦察、利用与后渗透的 AI 智能体
- **可扩展的安全测试** - 跨多个目标并行执行，实现快速、全面的覆盖
- **动态协作** - 智能体共享发现、串联漏洞，像红队一样协同作战

---

## 使用示例

### 基本用法

```bash
# 扫描本地代码库
strix --target ./app-directory

# 对 GitHub 仓库进行安全审查
strix --target https://github.com/org/repo

# 黑盒 Web 应用评估
strix --target https://your-app.com
```

### 高级测试场景

```bash
# 灰盒身份验证测试
strix --target https://your-app.com --instruction "Perform authenticated testing using credentials: user:pass"

# 多目标测试（源代码 + 已部署应用）
strix -t https://github.com/org/app -t https://your-app.com

# 白盒源码感知扫描（本地代码库）
strix --target ./app-directory --scan-mode standard

# 使用自定义指令进行聚焦测试
strix --target api.your-app.com --instruction "Focus on business logic flaws and IDOR vulnerabilities"

# 通过文件提供详细指令（例如交战规则、范围、排除项）
strix --target api.your-app.com --instruction-file ./instruction.md

# 针对特定基准分支强制执行 PR 差异范围扫描
strix -n --target ./ --scan-mode quick --scope-mode diff --diff-base origin/main
```

### 无界面模式（Headless Mode）

使用 `-n/--non-interactive` 标志，无需交互式界面即可以编程方式运行 Strix —— 非常适合服务器与自动化任务。CLI 会在退出前实时输出漏洞发现结果与最终报告。发现漏洞时将以非零状态码退出。

```bash
strix -n --target https://your-app.com
```

### CI/CD（GitHub Actions）

可以将 Strix 添加到你的流水线中，通过轻量级的 GitHub Actions 工作流在拉取请求上运行安全测试：

```yaml
name: strix-penetration-test

on:
  pull_request:

jobs:
  security-scan:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v6
        with:
          fetch-depth: 0

      - name: Install Strix
        run: curl -sSL https://strix.ai/install | bash

      - name: Run Strix
        env:
          STRIX_LLM: ${{ secrets.STRIX_LLM }}
          LLM_API_KEY: ${{ secrets.LLM_API_KEY }}

        run: strix -n -t ./ --scan-mode quick
```

> [!TIP]
> 在 CI 拉取请求运行中，Strix 会自动将快速审查范围限定在已更改的文件上。
> 如果无法解析差异范围，请确保检出（checkout）时使用完整历史记录（`fetch-depth: 0`），
> 或显式传入 `--diff-base` 参数。

### 配置

```bash
export STRIX_LLM="openai/gpt-5.4"
export LLM_API_KEY="your-api-key"

# 可选
export LLM_API_BASE="your-api-base-url"  # 如果使用本地模型，例如 Ollama、LMStudio
export PERPLEXITY_API_KEY="your-api-key"  # 用于搜索能力
export STRIX_REASONING_EFFORT="high"  # 控制思考强度（默认：high，快速扫描：medium）
```

> [!NOTE]
> Strix 会自动将你的配置保存到 `~/.strix/cli-config.json`，因此你无需在每次运行时重新输入。

**推荐使用的效果最佳的模型：**

- [OpenAI GPT-5.4](https://openai.com/api/) - `openai/gpt-5.4`
- [Anthropic Claude Sonnet 4.6](https://claude.com/platform/api) - `anthropic/claude-sonnet-4-6`
- [Google Gemini 3 Pro Preview](https://cloud.google.com/vertex-ai) - `vertex_ai/gemini-3-pro-preview`

查看 [LLM 提供商文档](https://docs.strix.ai/llm-providers/overview) 了解所有支持的提供商，包括 Vertex AI、Bedrock、Azure 及本地模型。

## 企业级渗透测试

获得与 Strix 相同的体验，并配备[企业级](https://strix.ai/demo)控制能力：SSO（SAML/OIDC）、符合合规要求的定制化渗透测试报告（SOC 2、ISO 27001、PCI DSS）、专属支持与 SLA、定制化部署选项（VPC/自托管）、BYOK（自带密钥）模型支持，以及为你的环境量身定制的 AI 渗透测试智能体。[了解更多](https://strix.ai/demo)。

## 文档

完整文档请访问 **[docs.strix.ai](https://docs.strix.ai)** —— 包含详细的使用指南、CI/CD 集成、技能扩展以及高级配置说明。

## 参与贡献

我们欢迎代码、文档及新技能的贡献 —— 查看我们的[贡献指南](https://docs.strix.ai/contributing)开始参与，或提交一个 [Pull Request](https://github.com/usestrix/strix/pulls) / [Issue](https://github.com/usestrix/strix/issues)。

## 加入社区

有任何问题？发现了 Bug？想要参与贡献？**[加入我们的 Discord！](https://discord.gg/strix-ai)**

## 支持本项目

**喜欢 Strix？** 在 GitHub 上给我们点个 ⭐ 吧！

## 致谢

Strix 建立在众多优秀开源项目的基础之上，包括 [LiteLLM](https://github.com/BerriAI/litellm)、[Caido](https://github.com/caido/caido)、[Nuclei](https://github.com/projectdiscovery/nuclei)、[Playwright](https://github.com/microsoft/playwright) 以及 [Textual](https://github.com/Textualize/textual)。衷心感谢这些项目的维护者！


> [!WARNING]
> 仅可测试你拥有所有权或已获得授权的应用程序。你需要对合乎道德与合法地使用 Strix 负责。

</div>
