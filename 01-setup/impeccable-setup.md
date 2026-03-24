# Cài đặt Impeccable

Impeccable là skill pack giúp AI hiểu ngôn ngữ design chuyên nghiệp.  
Không cài, AI vẫn làm được -- nhưng output sẽ generic: Inter font, gradient tím, card chồng card.  
Có Impeccable, AI hiểu các khái niệm như vertical rhythm, tinted neutrals, OKLCH color, motion easing.

---

## Cài tự động (khuyến nghị)

```bash
npx skills add pbakaus/impeccable
```

Lệnh này tự detect Antigravity và đặt file vào đúng chỗ (`.agents/skills/`).

---

## Cài thủ công

1. Tải ZIP tại: https://impeccable.style (mục Downloads)
2. Chọn **"Universal ZIP"**
3. Giải nén vào thư mục project hoặc thư mục home
4. Thư mục `.agents/` chứa files cho Antigravity

---

## Thiết lập lần đầu: `/teach-impeccable`

Sau khi cài, chạy lệnh này **một lần duy nhất** trong Antigravity:

```
/teach-impeccable
```

Lệnh này thu thập context của project (màu sắc, font, design language) và lưu vào file `.impeccable.md`.  
Từ đó, tất cả commands sau tự động hiểu context mà không cần nhắc lại.

> File `.impeccable.md` không bị ghi đè khi update Impeccable. Context được giữ nguyên.

---

## Cập nhật Impeccable

```bash
npx skills update
```

---

## Kiểm tra cài đặt

Trong Antigravity, gõ `/` và xem có xuất hiện các lệnh như `/audit`, `/polish`, `/critique` không.  
Nếu không thấy, kiểm tra lại file đã nằm đúng trong `.agents/skills/`.

---

## Tiếp theo

Xem workflow thực tế -> [../02-workflow/combined-workflow.md](../02-workflow/combined-workflow.md)
