# Cài đặt Figma Desktop Plugin

> Bắt buộc dùng **Figma Desktop** -- Figma web không hỗ trợ kết nối localhost.

---

## 1. Tải source plugin

```bash
git clone https://github.com/TranHoaiHung/figma-ui-mcp
cd figma-ui-mcp
npm install
```

Hoặc tải ZIP tại: https://github.com/TranHoaiHung/figma-ui-mcp/archive/refs/heads/main.zip  
Giải nén ra thư mục bất kỳ, ví dụ `~/tools/figma-ui-mcp/`.

---

## 2. Import plugin vào Figma Desktop

1. Mở Figma Desktop
2. Menu **Plugins** > **Development** > **Import plugin from manifest...**
3. Chọn file `plugin/manifest.json` trong thư mục vừa clone/giải nén
4. Plugin xuất hiện tên **"Figma UI MCP Bridge"**

---

## 3. Chạy plugin

1. Mở file Figma cần làm việc
2. Menu **Plugins** > **Development** > **Figma UI MCP Bridge**
3. Plugin panel mở ra, hiển thị trạng thái kết nối

**Trạng thái:**
- Chấm xanh = đã kết nối với MCP server
- Chấm đỏ = chưa kết nối (cần chạy Antigravity trước)

> Plugin phải đang mở trong khi dùng Antigravity. Mỗi lần mở Figma file mới cần chạy lại plugin.

---

## 4. Luồng kết nối hoàn chỉnh

```
Antigravity (lệnh)
    -> MCP server (localhost:38451)
        -> Figma Plugin (polling mỗi 500ms)
            -> Figma Document
```

Toàn bộ traffic chạy trên máy local, không qua server ngoài.

---

## Tiếp theo

Cài Impeccable -> [impeccable-setup.md](impeccable-setup.md)
