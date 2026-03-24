# Prompt Library -- TECOTEC / CCW

Prompt mẫu tiếng Việt, đã tối ưu cho context thương hiệu.  
Copy và chỉnh tham số trong `[ngoặc vuông]` theo nhu cầu.

---

## Design System & Tokens

```
tạo variable collection "CCW Brand" với:
- Machine Black: #1A1A1A
- Dark Gray: #4A4648
- Electric Lime: #E7E514
- Off White: #F5F5F5
- White: #FFFFFF
```

```
tạo variable collection "TECOTEC Brand" với:
- Primary Blue: #003087
- Secondary Blue: #0055B3
- Accent: #E8A000
- Dark: #1A1A1A
- Light: #F5F7FA
```

```
tạo text styles cho [CCW / TECOTEC]:
Heading 1: 40px Bold, Heading 2: 32px SemiBold, Heading 3: 24px SemiBold,
Body Large: 18px Regular, Body: 16px Regular, Caption: 12px Regular
font family: [Geist / Inter / DM Sans]
```

---

## Components

```
tạo component Button Primary cho CCW:
- size: 160x48
- fill: #1A1A1A (Machine Black)
- text: "KHÁM PHÁ NGAY" màu #E7E514 (Electric Lime), font SemiBold 14px
- bo góc: 0px (góc vuông -- brand identity CCW)
- auto layout horizontal, padding 20x14
```

```
tạo component Card Sản Phẩm cho CCW:
- frame 320x420
- ảnh placeholder 320x240 trên cùng, nền #4A4648
- text "Tên xe" bên dưới: 20px SemiBold, màu #1A1A1A
- text "Giá từ X.XXX.XXX đ": 16px Regular, màu #4A4648
- button "Xem chi tiết" full width phía dưới
```

```
tạo component Navigation Bar desktop cho [CCW / TECOTEC]:
- frame 1440x72, fill #1A1A1A
- logo placeholder góc trái 160x40
- menu items: [Xe, Đại lý, Phụ kiện, Tin tức, Liên hệ] căn giữa
- CTA button "Đặt lịch lái thử" góc phải
- text màu #F5F5F5, active state màu #E7E514
```

---

## Layouts & Screens

```
tạo artboard Homepage CCW, 1440x900:
- nền #1A1A1A
- hero section: full width, ảnh placeholder xe + headline "BUILT FOR THE PEOPLE"
- section sản phẩm nổi bật: 3 card sản phẩm
- CTA strip màu #E7E514
- footer dark
```

```
tạo artboard [tên trang] responsive: desktop 1440px, tablet 768px, mobile 375px
đặt 3 frame cạnh nhau, cùng content nhưng layout khác nhau
```

```
tạo artboard Email Template [tên campaign]:
- width 600px
- header logo CCW trên nền đen
- banner ảnh sản phẩm
- body text 2 cột
- CTA button "XEM NGAY" màu Electric Lime
- footer với địa chỉ và social links
```

---

## Thao tác nhanh

```
liệt kê tất cả components trong file này
```

```
chụp screenshot frame "[tên frame]" và hiển thị
```

```
clone component "[tên]" [X] lần, sắp xếp theo grid [số cột] cột, gap [X]px
```

```
đọc frame đang chọn và liệt kê: màu đang dùng, font, spacing
```

```
tạo artboard "Component Library" gom tất cả components, sắp xếp có nhãn
```

---

## Kết hợp với Impeccable

```
tạo [component/screen] xong -> /critique -> chỉnh theo feedback -> /polish
```

```
/audit [tên frame]
-- sau đó --
sửa các lỗi accessibility vừa tìm được trong frame "[tên]"
```

---

## Lưu ý khi prompt

- Càng cụ thể càng ít phải sửa: ghi rõ kích thước, màu hex, tên font
- Với thao tác phức tạp: chia nhỏ ra từng bước thay vì 1 lệnh dài
- Nếu kết quả không đúng: gõ thêm "sửa lại [điểm cần sửa]" -- không cần tạo lại từ đầu
- Undo: Cmd+Z trong Figma Desktop
