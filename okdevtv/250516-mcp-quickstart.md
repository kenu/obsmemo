- https://okdevtv.com/mib/mcp
- [Claude MCP Quickstart](https://www.claudemcp.com/docs/quickstart)

```sql
sqlite3 ~/test.db <<EOF
CREATE TABLE products (
  id INTEGER PRIMARY KEY,
  name TEXT,
  price REAL
);

INSERT INTO products (name, price) VALUES
  ('Widget', 19.99),
  ('Gadget', 29.99),
  ('Gizmo', 39.99),
  ('Smart Watch', 199.99),
  ('Wireless Earbuds', 89.99),
  ('Portable Charger', 24.99),
  ('Bluetooth Speaker', 79.99),
  ('Phone Stand', 15.99),
  ('Laptop Sleeve', 34.99),
  ('Mini Drone', 299.99),
  ('LED Desk Lamp', 45.99),
  ('Keyboard', 129.99),
  ('Mouse Pad', 12.99),
  ('USB Hub', 49.99),
  ('Webcam', 69.99),
  ('Screen Protector', 9.99),
  ('Travel Adapter', 27.99),
  ('Gaming Headset', 159.99),
  ('Fitness Tracker', 119.99),
  ('Portable SSD', 179.99);
EOF
```

- [Claude Desktop app](https://claude.ai/download)
- `code ~/Library/Application\ Support/Claude/claude_desktop_config.json`

```json
{
  "mcpServers": {
    "sqlite": {
      "command": "uvx",
      "args": ["mcp-server-sqlite", "--db-path", "/Users/YOUR_USERNAME/test.db"]
    }
  }
}
```


웹사이트 운영에 필요한 것들과 총금액

웹사이트 운영에 필요한 필수 항목과 선택적 항목을 분석했습니다. 데이터베이스에서 확인한 정보를 바탕으로 정리해 드립니다.

### 필수 항목 (기본 요구사항)

| 항목 | 설명 | 월 비용 | 연간 비용 |
|------|------|---------|----------|
| 도메인 이름 | 웹사이트 주소 등록 (예: example.com) | ₩1,250 | ₩15,000 |
| 웹 호스팅 | 중소형 웹사이트를 위한 기본 공유 호스팅 | ₩5,000 | ₩60,000 |
| SSL 인증서 | 보안 HTTPS 연결용 (호스팅에 무료 제공되는 경우 많음) | ₩0 | ₩0 |
| 콘텐츠 관리 시스템 | WordPress 같은 오픈소스 CMS (소프트웨어 자체) | ₩0 | ₩0 |
| 이메일 호스팅 | 도메인용 기본 이메일 서비스 | ₩5,000 | ₩60,000 |
| 분석 도구 | 웹사이트 트래픽 추적 (Google Analytics는 무료) | ₩0 | ₩0 |

필수 항목 총액: 월 ₩11,250 / 연간 ₩135,000

### 선택적 항목 (추가 기능)

| 항목          | 설명                         | 월 비용    | 연간 비용    |
| ----------- | -------------------------- | ------- | -------- |
| CDN 서비스     | 전 세계 빠른 접속을 위한 콘텐츠 전송 네트워크 | ₩10,000 | ₩120,000 |
| 백업 서비스      | 정기적인 자동 백업                 | ₩5,000  | ₩60,000  |
| SEO 도구      | 기본 검색 엔진 최적화 도구            | ₩30,000 | ₩360,000 |
| 개발자 유지보수    | 정기적인 업데이트 및 유지보수           | ₩50,000 | ₩600,000 |
| 프리미엄 테마/템플릿 | 전문적인 디자인을 위한 일회성 구매        | ₩5,000  | ₩60,000  |
| 보안 서비스      | 방화벽 및 악성코드 보호              | ₩10,000 | ₩120,000 |
모든 항목 포함 총액: 월 ₩121,250 / 연간 ₩1,455,000

웹사이트의 규모와 목적에 따라 필요한 항목이 달라질 수 있으며, 각 서비스의 가격은 제공업체와 선택하는 플랜에 따라 차이가 있을 수 있습니다. 기본적인 웹사이트 운영을 위해서는 필수 항목만으로도 충분할 수 있습니다.