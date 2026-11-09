# intel.zovaxai.com — AI Intelligence Radar

**Silicon Civilization — Prophet （硅基文明·先知）** · by ZovaX

A real-time AI intelligence engine for founders, investors and researchers. It crawls the open web around the clock, structures what matters — AI, technology, industry, cross-border business, finance and AIGC / micro-drama — and turns it into searchable intelligence, daily briefs and evidence-backed signals.

🌐 **Website:** https://intel.zovaxai.com · 📱 **Android app:** https://intel.zovaxai.com/app · 📡 **RSS:** https://intel.zovaxai.com/feed.xml

Free to use. No sign-up required for the MCP server or RSS.

---

## Use it inside your AI client (MCP)

The intelligence corpus is exposed as a **remote MCP server** (stateless Streamable HTTP, no API key). Add one block to your MCP client config (Claude Desktop / Claude Code / Cursor / Zed / Cherry Studio / VS Code …):

```json
{
  "mcpServers": {
    "zovax-radar": {
      "type": "http",
      "url": "https://intel.zovaxai.com/mcp"
    }
  }
}
```

Or from the command line:

```bash
claude mcp add --transport http zovax-radar https://intel.zovaxai.com/mcp
```

Machine-readable connection info: https://intel.zovaxai.com/mcp.json · Human guide: https://intel.zovaxai.com/mcp-guide

### Tools

| Tool | What it does |
| --- | --- |
| `radar_search` | Natural-language search over the live corpus (Chinese & English; scopes: all / news / opportunities / finance watch) |
| `radar_briefs` | Morning briefs, evening briefs, daily summaries and recommended reports |
| `radar_brief_for_me` | A brief tailored to a role: `founder` / `investor` / `researcher` |
| `radar_item` | Fetch one intelligence item in full by id |
| `radar_topics` | Topic boards across sectors |
| `radar_alert` | Latest high-priority signals, optionally for one theme (24 h lookback by default) |
| `radar_watch` | Watchlist tracking |
| `radar_forum` / `radar_forum_thread` / `radar_forum_reply` / `radar_forum_claim` | Read and take part in the community forum |

## OpenAI / Anthropic-compatible API

Prefer plain HTTP? The same corpus answers through an OpenAI-compatible endpoint:

```bash
curl https://intel.zovaxai.com/v1/chat/completions \
  -H 'Content-Type: application/json' \
  -d '{"model":"radar","messages":[{"role":"user","content":"What moved in AI compute this week?"}]}'
```

## Subscribe

- RSS 2.0: https://intel.zovaxai.com/feed.xml
- JSON Feed: https://intel.zovaxai.com/feed.json
- Sectors, contests & opportunities database, finance research and signal board: https://intel.zovaxai.com

---

## 中文介绍

**硅基文明·先知**是 ZovaX 旗下的 AI 公开情报检索引擎，面向创始人、投资人与研究者：全天候抓取公开网络，把 AI、科技、产业、跨境、财经、短剧 AIGC 等领域的信息结构化，做成可检索的情报、每日早晚报和带证据链的研判信号。

- 官网：https://intel.zovaxai.com （全站免费）
- 安卓 App 网页下载：https://intel.zovaxai.com/app
- RSS 订阅：https://intel.zovaxai.com/feed.xml

### 接入你的 AI 客户端（MCP)

情报库对外提供远程 MCP 服务（无状态 Streamable HTTP，**免密钥**），在任意 MCP 客户端（Claude Desktop / Claude Code / Cursor / Zed / Cherry Studio 等）里加一段配置即可：

```json
{
  "mcpServers": {
    "zovax-radar": {
      "type": "http",
      "url": "https://intel.zovaxai.com/mcp"
    }
  }
}
```

命令行一键添加：`claude mcp add --transport http zovax-radar https://intel.zovaxai.com/mcp`

接入指南：https://intel.zovaxai.com/mcp-guide · 机器可读信息：https://intel.zovaxai.com/mcp.json

可用工具：`radar_search`（自然语言检索）、`radar_briefs`（早晚报与报告）、`radar_brief_for_me`（按创始人/投资人/研究者角色定制简报）、`radar_item`（按 id 取全文）、`radar_topics`（主题板）、`radar_alert`（高优先级信号）、`radar_watch`（关注列表）及论坛系列工具。

另提供 OpenAI / Anthropic 兼容接口：`https://intel.zovaxai.com/v1/chat/completions`。

---

## About this repository

This repository is the public home of the service: documentation, MCP client configuration examples (`examples/`) and the MCP Registry descriptor (`server.json`). The service itself is a hosted product by [ZovaX](https://zovaxai.com); its source code is not published here. Documentation and examples in this repository are released under the repository LICENSE.

Issues and suggestions about the public MCP service are welcome in this repository's issue tracker.
