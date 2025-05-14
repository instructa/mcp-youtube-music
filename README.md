[![MseeP.ai Security Assessment Badge](https://mseep.net/pr/instructa-mcp-youtube-music-badge.png)](https://mseep.ai/app/instructa-mcp-youtube-music)

# YouTube Music MCP 🎵

This is a simple MCP server that allows you to search for and play tracks on YouTube Music directly from your AI assistant like Cursor or Claude Desktop.

Built with:

- [YouTube Music](https://music.youtube.com/)
- [Anthropic MCP](https://docs.anthropic.com/en/docs/agents-and-tools/mcp)
- [Cursor](https://cursor.so/)

## Available Tools

- `searchTrack`: Search for tracks on YouTube Music by name.
- `playTrack`: Play tracks directly by searching and opening them in your default browser.


# Installation

## 1. Get a key

To make this work you need a valid [Google Youtube API Key](https://console.cloud.google.com/marketplace/product/google/youtube.googleapis.com)

## 2. Add to cursor

Add the following MCP configuration to your Cursor `.cursor/mcp.json` settings:

```json
{
  "mcpServers": {
    "youtube-music-mcp": {
      "command": "npx",
      "args": ["-y", "@instructa/mcp-youtube-music"],
      "env": {
        "YOUTUBE_API_KEY": "<INSERT_API_KEY_HERE>"
      }
    }
  }
}
```

**Develop**

This MCP is typically run directly using `npx` and doesn't require local installation or building unless you intend to modify the source code. If you want to develop it locally, you would typically clone the source repository (if available) and follow its specific contribution guidelines.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Links

- X/Twitter: [@kregenrek](https://x.com/kregenrek)
- Bluesky: [@kevinkern.dev](https://bsky.app/profile/kevinkern.dev)

## Courses
- Learn Cursor AI: [Ultimate Cursor Course](https://www.instructa.ai/en/cursor-ai)
- Learn to build software with AI: [instructa.ai](https://www.instructa.ai)

## See my other projects:

* [AI Prompts](https://github.com/instructa/ai-prompts/blob/main/README.md) - Curated AI Prompts for Cursor AI, Cline, Windsurf and Github Copilot
* [codefetch](https://github.com/regenrek/codefetch) - Turn code into Markdown for LLMs with one simple terminal command
* [aidex](https://github.com/regenrek/aidex) A CLI tool that provides detailed information about AI language models, helping developers choose the right model for their needs.
* [codetie](https://github.com/codetie-ai/codetie) - XCode CLI