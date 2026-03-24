# Impeccable Workflow

20 commands chia thành 4 nhóm. Dùng trong Antigravity bằng cách gõ `/tên-lệnh`.

---

## Nhóm 1: Kiểm tra và đánh giá

| Command | Dùng khi |
|---|---|
| `/audit` | Kiểm tra kỹ thuật: accessibility, responsive, performance |
| `/critique` | Review UX: hierarchy, clarity, cảm xúc tổng thể |

```
/audit header
/critique checkout-form
/audit               <- toàn bộ screen hiện tại
```

---

## Nhóm 2: Cải thiện chất lượng

| Command | Dùng khi |
|---|---|
| `/polish` | Pass cuối trước khi giao |
| `/normalize` | Đồng bộ với design system |
| `/distill` | Design đang quá rối, cần strip bớt |
| `/clarify` | Copy/label chưa rõ |
| `/harden` | Xử lý edge case, i18n, lỗi |
| `/optimize` | Cải thiện performance |

---

## Nhóm 3: Thêm tính năng visual

| Command | Dùng khi |
|---|---|
| `/animate` | Thêm motion có chủ đích |
| `/colorize` | Thêm màu sắc chiến lược |
| `/bolder` | Design đang nhạt, cần punch hơn |
| `/quieter` | Design đang quá bold, cần toned down |
| `/delight` | Thêm moment vui, microinteraction |
| `/overdrive` | Effect kỹ thuật cao (beta) |
| `/typeset` | Fix typography system |
| `/arrange` | Fix layout và spacing |

---

## Nhóm 4: Cấu trúc và mở rộng

| Command | Dùng khi |
|---|---|
| `/extract` | Pull ra reusable component |
| `/adapt` | Adapt cho device khác |
| `/onboard` | Thiết kế flow onboarding |
| `/teach-impeccable` | Setup lần đầu (chạy 1 lần) |

---

## Tips

**Chỉ định vùng cụ thể:**
```
/polish navigation bar
/audit mobile viewport
/bolder hero section
```

**Kết hợp commands theo thứ tự logic:**
```
/critique -> /normalize -> /polish
```

**Impeccable tự áp context từ `.impeccable.md`** -- không cần nhắc lại brand màu sắc mỗi lần.
