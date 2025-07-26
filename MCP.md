{
  "mcpServers": {
    "markitdown": {
      "command": "docker",
      "args": [
        "run",
        "--rm",
        "-i",
        "markitdown-mcp:latest"
      ],
      "disabled": false,
      "autoApprove": [
        "convert_to_markdown"
      ]
    },
    "context7": {
      "command": "npx",
      "args": [
        "-y",
        "@upstash/context7-mcp@latest"
      ],
      "disabled": false,
      "autoApprove": []
    },
    "brave": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "-e",
        "BRAVE_API_KEY",
        "mcp/brave-search"
      ],
      "env": {
        "BRAVE_API_KEY": "BSArRh3UI-Syn2THl4PWnfL3-p5f0zT"
      },
      "disabled": false,
      "autoApprove": [
        "brave_web_search"
      ]
    },
    "fetch": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "mcp/fetch"
      ],
      "disabled": false,
      "autoApprove": [
        "fetch"
      ]
    },
    "paper-search": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "mcp/paper-search"
      ],
      "disabled": false,
      "autoApprove": []
    },
    "youtube_transcript": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "mcp/youtube-transcript"
      ],
      "disabled": false,
      "autoApprove": [
        "get_transcript"
      ]
    },
    "sequentialthinking": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "mcp/sequentialthinking"
      ],
      "disabled": false,
      "autoApprove": [
        "sequentialthinking"
      ]
    },
    "playwright": {
      "command": "npx",
      "args": [
        "@playwright/mcp@latest"
      ],
      "disabled": false,
      "autoApprove": []
    },
    "firecrawl": {
      "command": "npx",
      "args": [
        "-y",
        "firecrawl-mcp"
      ],
      "env": {
        "FIRECRAWL_API_KEY": "fc-4b7563b73480441a82e34685295c41e1"
      },
      "disabled": false,
      "autoApprove": [
        "firecrawl_search"
      ]
    }
  }
}
