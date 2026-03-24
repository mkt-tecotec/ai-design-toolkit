# figma-ui-mcp Workflow

Có 4 tools chính. Antigravity tự chọn tool phù hợp -- không cần gọi tên tool, chỉ cần mô tả việc cần làm.

---

## figma_write -- Tạo và chỉnh sửa

Dùng khi: tạo frame, component, shape, text, apply color/style.

**Ví dụ lệnh:**
```
tạo 1 button primary với nền #1A1A1A, text trắng, bo góc 8px, size 160x48
```
```
tạo 1 artboard 1440x900, đặt tên "Homepage - Desktop"
```
```
thêm auto layout vào frame "Card" vừa tạo, padding 24px, gap 16px
```
```
clone component Button Primary thành Button Secondary, đổi màu nền thành #E7E514
```

**Batch operations** -- nhóm nhiều thao tác vào 1 lệnh (nhanh hơn 10-25x):
```
tạo cùng lúc: 1 frame sidebar 240x900, 1 header 1440x72, 4 KPI card 280x160
```

---

## figma_read -- Đọc thiết kế

Dùng khi: lấy thông số, export, kiểm tra node hiện tại.

**Ví dụ lệnh:**
```
đọc frame đang chọn và cho tôi biết màu sắc, font đang dùng
```
```
chụp screenshot frame "Homepage" và hiển thị
```
```
liệt kê tất cả components trong file này
```
```
lấy tất cả design tokens (variables) trong file
```
```
export frame "Banner CCW" thành SVG
```

---

## figma_status -- Kiểm tra kết nối

```
kiểm tra kết nối figma
```

---

## figma_docs -- Tra cứu API

```
hướng dẫn cách tạo variable collection trong figma mcp
```

---

## Các lưu ý thực tế

**Plugin phải đang chạy.** Nếu Antigravity báo lỗi kết nối, kiểm tra Figma Desktop có đang mở plugin không.

**Figma Desktop, không phải web.** Plugin chỉ chạy trên app desktop.

**Node ID vs tên.** Nếu có nhiều frame cùng tên, chỉ định thêm: `frame "Button" trong page "Components"`.

**Undo vẫn hoạt động.** Mọi thao tác qua MCP đều undo được bằng Cmd+Z trong Figma.
