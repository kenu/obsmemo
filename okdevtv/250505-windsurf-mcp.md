- 윈드서프에서 MCP를 사용하는 방법입니다.

### Windsurf
- https://windsurf.com : cursor ai($20/월) 와 경쟁 관계
- $15/월

### MCP (Model Context Protocol)
- Claude 서비스하는 Anthropic이 제시한 AI간의 통신 프로토콜
- OpenAPI처럼 AI와 다른 리소스를 연결
- MCP 보안 이슈: [Channy](https://channy.creation.net/blog/author/admin)
  - [MCP – Model Context Protocol 보안 위험](https://channy.creation.net/blog/1937)


### Windsurf + MCP

![[windsurf-mcp.webp]]

- `Configure 🔨`
```
{
  "mcpServers": {
    "weather": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/adhikasp/mcp-weather.git",
        "mcp-weather"
      ],
      "env": {
        "ACCUWEATHER_API_KEY": "your-api-key"
      }
    },
    "puppeteer": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-puppeteer"
      ]
    }
  }
}
```
- code from: https://www.youtube.com/watch?v=KtJz3OvdxCA
### related
- AccuWeather API key
  - https://developer.accuweather.com/user/me/apps
- 검색 못하던 클로드가 MCP 달더니 별의별 걸 다 하는 모습 공개 (프롬프트 엔지니어 강수진 박사)
  - https://www.youtube.com/watch?v=nfPXfsVz6jM
