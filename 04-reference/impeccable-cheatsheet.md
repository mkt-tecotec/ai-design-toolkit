# Impeccable -- Bảng tra cứu nhanh

v1.5.1 | https://impeccable.style/cheatsheet

---

## Setup (chạy 1 lần)

| Command | Tác dụng |
|---|---|
| `/teach-impeccable` | Thu thập context project, lưu vào `.impeccable.md` |

---

## Kiểm tra & Đánh giá

| Command | Tác dụng | Dùng khi |
|---|---|---|
| `/audit [vùng]` | Kiểm tra kỹ thuật: a11y, responsive, performance | Trước khi bàn giao |
| `/critique [vùng]` | Review UX: hierarchy, clarity, cảm xúc | Muốn góc nhìn thiết kế |

---

## Cải thiện chất lượng

| Command | Tác dụng | Dùng khi |
|---|---|---|
| `/polish [vùng]` | Pass cuối trước khi ship | Gần xong, cần finalize |
| `/normalize [vùng]` | Đồng bộ với design system | Có sự không nhất quán |
| `/distill [vùng]` | Strip bỏ thứ không cần thiết | Design đang rối |
| `/clarify [vùng]` | Cải thiện UX copy, label | Text chưa rõ ràng |
| `/harden [vùng]` | Xử lý edge case, i18n, lỗi | Chuẩn bị production |
| `/optimize [vùng]` | Cải thiện performance | Load chậm, asset nặng |
| `/typeset [vùng]` | Fix typography system | Type system lộn xộn |
| `/arrange [vùng]` | Fix layout và spacing | Grid/spacing không nhất quán |

---

## Thêm tính năng visual

| Command | Tác dụng | Dùng khi |
|---|---|---|
| `/animate [vùng]` | Thêm motion có chủ đích | Cần transition, microinteraction |
| `/colorize [vùng]` | Thêm màu sắc chiến lược | Design quá đơn sắc |
| `/bolder [vùng]` | Amplify, tăng độ punch | Design nhạt, thiếu impact |
| `/quieter [vùng]` | Giảm độ bold | Design quá ồn ào |
| `/delight [vùng]` | Thêm moment vui | Muốn tăng brand personality |
| `/overdrive [vùng]` | Effect kỹ thuật cao (beta) | Cần WOW effect đặc biệt |

---

## Cấu trúc & Mở rộng

| Command | Tác dụng | Dùng khi |
|---|---|---|
| `/extract [vùng]` | Pull ra reusable component | Có pattern lặp lại |
| `/adapt [vùng]` | Adapt cho device khác | Cần responsive version |
| `/onboard [vùng]` | Thiết kế flow onboarding | Tạo user onboarding |

---

## Thứ tự commands khuyến nghị

**Tạo mới:**
```
/critique -> /normalize -> /polish
```

**Nhận file có sẵn:**
```
/audit -> /critique -> chỉnh sửa -> /polish
```

**Design hệ thống:**
```
/teach-impeccable -> tạo components -> /normalize -> /extract -> /polish
```

---

## Anti-patterns Impeccable tự tránh

- Font Inter/Arial mặc định
- Gradient tím generic
- Card lồng trong card
- Text xám trên nền màu (contrast kém)
- Pure black/gray (luôn tint)
- Bounce/elastic easing (lỗi thời)
