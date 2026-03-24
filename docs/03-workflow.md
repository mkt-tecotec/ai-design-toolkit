# Workflow kết hợp figma-ui-mcp + Impeccable

## Nguyên tắc phân vai

| Tool | Dùng khi |
|------|----------|
| **figma-ui-mcp** | Tạo/sửa element trực tiếp trên Figma (frame, component, token, layout) |
| **Impeccable** | Cần AI hiểu design đúng chuẩn, tránh output generic |

Thứ tự thông thường: **Impeccable giúp AI tư duy đúng → figma-ui-mcp thực thi lên canvas.**

---

## Workflow 1: Tạo component mới từ đầu

```
1. Mô tả yêu cầu rõ ràng (size, màu, variant)
2. Thêm /polish vào cuối prompt để AI tự review trước khi tạo
3. AI dùng figma_write để tạo lên Figma
4. Dùng figma_read (screenshot) để review kết quả
5. Điều chỉnh nếu cần
```

Ví dụ:

```
tạo button component cho CCW Vietnam.
màu primary: #E7E514, text: #1A1A1A.
height: 48px, padding ngang: 24px, border-radius: 4px.
3 variant: Default / Hover (opacity 90%) / Disabled (opacity 40%).
/polish
```

---

## Workflow 2: Review và cải thiện design có sẵn

```
1. Chọn frame trên Figma
2. Prompt: "đọc frame tôi đang chọn"
3. Chạy /audit hoặc /critique
4. AI đề xuất cải tiến -- confirm trước khi apply
5. AI dùng figma_write để apply thay đổi
```

Ví dụ:

```
đọc frame tôi đang chọn
/critique
sau đó fix các vấn đề về hierarchy và spacing
chụp screenshot kết quả
```

---

## Workflow 3: Setup Design Token từ brand guide

Dùng khi bắt đầu file Figma mới hoặc cần sync lại token.

```
setup design tokens cho TECOTEC Group:
colors:
  primary: #003087
  secondary: #E31837
  neutral-dark: #1A1A1A
  neutral-light: #F5F5F5
numbers:
  spacing-4: 4
  spacing-8: 8
  spacing-16: 16
  spacing-24: 24
  spacing-32: 32
  spacing-48: 48
```

figma-ui-mcp sẽ tạo toàn bộ variable collection trong một lần gọi.

---

## Workflow 4: Extract component library từ design có sẵn

```
1. figma_read toàn bộ page
2. /extract để AI identify các element tái sử dụng
3. AI dùng figma.createComponent() để convert thành master component
4. Tổ chức vào artboard library
```

---

## Tips thực tế

**Dùng batch khi tạo nhiều element:**  
Nhắc AI "dùng batch operation" khi cần tạo nhiều thứ cùng lúc -- nhanh hơn 10-25x.

**Screenshot để review nhanh:**

```
chụp screenshot frame [tên frame]
```

**Chia nhỏ task:**  
Tạo layout → review → tạo component → review → token.  
Đừng nhét tất cả vào 1 prompt -- AI xử lý tốt hơn khi scope rõ.

**Đặt tên node theo convention:**  
`Button/Primary/Default`, `Card/Product/Hover` -- dễ query, dễ instantiate sau này.

**Lưu `.impeccable.md` vào git:**  
File này chứa brand context dùng chung cho cả team.
