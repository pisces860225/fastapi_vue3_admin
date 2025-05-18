# 使用 JSON 版 API 文件指南

FastAPI 於 `/openapi.json` 提供完整 OpenAPI 說明文件。

## 取得 JSON

```bash
curl http://localhost:8000/openapi.json -o openapi.json
```

## 典型用途

1. 透過 [OpenAPI Generator](https://openapi-generator.tech/) 產生各語言客戶端 SDK。
2. 在 Postman ／ Insomnia 匯入 `openapi.json` 以建立 API Collection。
3. 於 CI/CD 流程自動驗證 API 變更。

## JSON 結構範例

```json
{
  "openapi": "3.1.0",
  "info": {
    "title": "fastapi_vue3_admin",
    "version": "0.1.0"
  },
  "paths": {
    "/staff/users/": {"get": {"summary": "列出所有員工"}},
    "/public/hello/": {"get": {"summary": "公開 Hello World"}}
  }
}
``` 