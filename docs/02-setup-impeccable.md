# Setup Impeccable

## Impeccable là gì?

Impeccable là bộ skill + command giúp AI hiểu đúng ngôn ngữ design chuyên nghiệp.  
Không có nó, AI thường mắc các lỗi kinh điển: dùng Inter mặc định, gradient tím, cards lồng cards.

Gồm 2 thành phần:
- **Skill `frontend-design`**: tự động áp dụng khi AI làm việc liên quan UI
- **20 commands** (`/polish`, `/audit`, `/critique`...): gọi thủ công khi cần

---

## Cài đặt cho Antigravity

### Cách 1: Tự động (khuyến nghị)

```bash
npx skills add pbakaus/impeccable
```

Lệnh này tự detect Antigravity và đặt file vào đúng chỗ (`.agents/skills/`).

### Cách 2: Thủ công

1. Tải ZIP tại [impeccable.style](https://impeccable.style) -- chọn **Universal ZIP**
2. Giải nén vào thư mục project
3. File Antigravity nằm trong `.agents/skills/`

---

## Bước quan trọng: Dạy Impeccable về project

Chạy một lần duy nhất sau khi cài:

```
/teach-impeccable
```

Impeccable sẽ hỏi về project (màu brand, font, style target...) và lưu vào file `.impeccable.md`.  
Từ đó, tất cả commands đều tự dùng context này -- không cần giải thích lại mỗi lần.

> Commit file `.impeccable.md` vào repo để cả team dùng chung brand context.  
> File này không bị ghi đè khi update. Chỉnh tay nếu cần cập nhật.

---

## Cập nhật

```bash
npx skills update
```

---

## Kiểm tra đã cài chưa

Trong Antigravity, gõ `/` -- nếu thấy `/polish`, `/audit`, `/critique`... xuất hiện = cài thành công.

---

## 20 Commands theo nhóm

Xem đầy đủ tại [cheatsheet](../prompts/cheatsheet.md).

| Nhóm | Commands |
|------|----------|
| Thiết lập | `/teach-impeccable` |
| Kiểm tra | `/audit`, `/critique` |
| Chuẩn hóa | `/normalize`, `/polish`, `/simplify` |
| Nâng cấp | `/bolder`, `/colorize`, `/animate`, `/delight`, `/overdrive` |
| Tinh chỉnh | `/quieter`, `/clarify`, `/harden`, `/optimize` |
| Cấu trúc | `/extract`, `/adapt`, `/onboard` |
| Typography | `/typeset`, `/arrange` |
