# Cài đặt Antigravity + figma-ui-mcp

## 1. Cài Antigravity

Tải Antigravity tại: https://antigravity.dev  
Cài như app macOS thông thường, đăng nhập bằng tài khoản Google.

---

## 2. Cấu hình figma-ui-mcp trong Antigravity

figma-ui-mcp là MCP server cho phép Antigravity giao tiếp trực tiếp với Figma Desktop.

**Bước 1:** Trong Antigravity, mở menu `...` (góc trên panel agent)

**Bước 2:** Chọn **"Manage MCP Servers"** > **"View raw config"**

**Bước 3:** Thêm đoạn sau vào file `mcp_config.json`:

```json
{
  "mcpServers": {
    "figma": {
      "command": "npx",
      "args": ["-y", "figma-ui-mcp"]
    }
  }
}
```

**Bước 4:** Lưu file, khởi động lại Antigravity.

**Kiểm tra:** Gõ lệnh sau trong Antigravity:
```
kiểm tra kết nối figma
```
Antigravity sẽ gọi `figma_status`. Nếu báo chưa kết nối thì sang bước tiếp theo (cài plugin).

---

## 3. Yêu cầu hệ thống

- Node.js 18 trở lên. Kiểm tra: `node -v`
- Nếu chưa có: tải tại https://nodejs.org

---

## Tiếp theo

Cài Figma Desktop plugin -> [figma-mcp-setup.md](figma-mcp-setup.md)
