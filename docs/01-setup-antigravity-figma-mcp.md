# Setup Antigravity + figma-ui-mcp

## Tổng quan

figma-ui-mcp hoạt động theo mô hình bridge:

```
Antigravity (AI) --> MCP Server (localhost:38451) --> Figma Plugin --> Figma Document
```

Mọi thứ chạy local, không gửi dữ liệu ra ngoài.

---

## Bước 1: Cài Node.js

Kiểm tra đã có chưa:

```bash
node -v
```

Cần >= 18. Nếu chưa có, tải tại [nodejs.org](https://nodejs.org) hoặc dùng Homebrew:

```bash
brew install node
```

---

## Bước 2: Cấu hình MCP server trong Antigravity

1. Mở Antigravity
2. Click **"..."** ở góc trên panel agent
3. Chọn **"Manage MCP Servers"** → **"View raw config"**
4. Thêm đoạn sau vào file `mcp_config.json`:

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

5. Lưu file, restart Antigravity

---

## Bước 3: Cài Figma plugin

> Bắt buộc dùng **Figma Desktop** -- không chạy trên Figma web.

1. Clone repo về máy:

```bash
git clone https://github.com/TranHoaiHung/figma-ui-mcp
```

2. Mở Figma Desktop
3. Vào **Plugins → Development → Import plugin from manifest...**
4. Chọn file `plugin/manifest.json` trong thư mục vừa clone
5. Chạy plugin: **Plugins → Development → Figma UI MCP Bridge**

Khi plugin hiện **chấm xanh** = kết nối thành công.

---

## Bước 4: Kiểm tra kết nối

Trong Antigravity, gõ:

```
kiểm tra kết nối figma
```

Nếu AI trả về thông tin page hiện tại = kết nối OK.

---

## Xử lý lỗi thường gặp

| Lỗi | Nguyên nhân | Cách fix |
|-----|-------------|----------|
| Plugin chấm đỏ | MCP server chưa chạy | Restart Antigravity, kiểm tra mcp_config.json |
| `npx: command not found` | Node chưa cài hoặc PATH sai | Cài lại Node, kiểm tra `which node` |
| Terminal disconnect | Shell session timeout | Chạy lại lệnh, không ảnh hưởng kết nối MCP |
| Figma không nhận lệnh | Đang dùng Figma web | Chuyển sang Figma Desktop |

---

## Các tool MCP có sẵn

| Tool | Dùng để |
|------|---------|
| `figma_write` | Tạo/sửa/xóa node, component, token |
| `figma_read` | Đọc design tree, lấy styles, screenshot |
| `figma_status` | Kiểm tra kết nối và context hiện tại |
| `figma_docs` | Tra cứu API reference |
