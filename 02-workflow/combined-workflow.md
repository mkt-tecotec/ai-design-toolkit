# Combined Workflow

Cách 3 công cụ phối hợp trong thực tế.

---

## Luồng cơ bản: Tạo component mới

```
1. [Impeccable] /teach-impeccable     <- chỉ lần đầu
2. [figma-mcp]  Tạo frame/component
3. [Impeccable] /critique             <- đánh giá
4. [figma-mcp]  Chỉnh theo feedback
5. [Impeccable] /normalize            <- đồng bộ design system
6. [Impeccable] /polish               <- pass cuối
```

---

## Luồng thực tế: Tạo Design System từ đầu

**Bước 1 -- Thiết lập tokens**
```
tạo variable collection tên "Brand Colors" với các biến:
- Machine Black: #1A1A1A
- Electric Lime: #E7E514
- Off White: #F5F5F5
```

**Bước 2 -- Tạo text styles**
```
tạo text styles: Heading 1 (32px, SemiBold), Heading 2 (24px, SemiBold),
Body (16px, Regular), Caption (12px, Regular) -- font Geist
```

**Bước 3 -- Tạo master components**
```
tạo component Button Primary: frame 160x48, fill Machine Black,
text "Label" màu trắng, bo góc 8px, auto layout horizontal, padding 16x12
```

**Bước 4 -- Review với Impeccable**
```
/critique button component vừa tạo
/normalize   <- kiểm tra có đúng design system không
```

**Bước 5 -- Tạo artboard tổng hợp**
```
tạo 1 artboard "Component Library" chứa tất cả components vừa tạo,
sắp xếp theo grid 4 cột, gap 40px
```

---

## Luồng thực tế: Refine design có sẵn

```
1. đọc frame đang chọn và liệt kê tất cả màu sắc đang dùng
2. /audit
3. /critique
4. [xem feedback, quyết định chỉnh gì]
5. chỉnh [element cụ thể] theo gợi ý
6. /polish
```

---

## Luồng thực tế: Tạo banner hàng loạt

```
tạo cùng lúc 5 frame:
- "Banner Facebook" 1200x628
- "Banner Instagram Square" 1080x1080
- "Banner Instagram Story" 1080x1920
- "Banner Google Display" 300x250
- "Banner Google Leaderboard" 728x90

mỗi frame dùng nền #1A1A1A, có placeholder cho logo CCW góc trên trái
```

Sau đó refine từng cái:
```
/adapt banner facebook cho mobile
```

---

## Điểm quan trọng

- Antigravity giữ context trong session: có thể nói "frame vừa tạo", "component đó" mà không cần lặp lại tên
- Undo bằng Cmd+Z trong Figma nếu kết quả không như ý
- Plugin phải đang mở trong Figma Desktop suốt quá trình làm việc
- Impeccable không can thiệp trực tiếp vào Figma -- chỉ gợi ý, việc thực thi do figma-mcp làm
