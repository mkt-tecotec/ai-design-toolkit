# ai-design-toolkit

Bộ công cụ AI hỗ trợ thiết kế UI/UX cho team MarCom TECOTEC Group.  
Kết hợp **Antigravity IDE** + **figma-ui-mcp** + **Impeccable** để thiết kế nhanh hơn, chất lượng cao hơn.

---

## Bộ công cụ gồm gì?

| Công cụ | Vai trò |
|---|---|
| [Antigravity](https://antigravity.dev) | AI IDE -- nhận lệnh tự nhiên, thực thi tác vụ |
| [figma-ui-mcp](https://github.com/TranHoaiHung/figma-ui-mcp) | Cầu nối giữa Antigravity và Figma Desktop |
| [Impeccable](https://impeccable.style) | Skill pack giúp AI hiểu ngôn ngữ design chuyên nghiệp |

Ba công cụ hoạt động theo luồng:

```
Lệnh text (Antigravity) → figma-ui-mcp → Figma Desktop
                ↑
         Impeccable skills
     (cải thiện chất lượng output)
```

---

## Quick Start

1. Cài Antigravity + cấu hình figma-ui-mcp → [01-setup/antigravity-setup.md](01-setup/antigravity-setup.md)
2. Cài Figma Desktop plugin → [01-setup/figma-mcp-setup.md](01-setup/figma-mcp-setup.md)
3. Cài Impeccable → [01-setup/impeccable-setup.md](01-setup/impeccable-setup.md)
4. Xem workflow thực tế → [02-workflow/combined-workflow.md](02-workflow/combined-workflow.md)
5. Lấy prompt mẫu → [03-prompt-library/prompts-vi.md](03-prompt-library/prompts-vi.md)

---

## Cấu trúc repo

```
ai-design-toolkit/
├── 01-setup/
│   ├── antigravity-setup.md      Cài Antigravity + cấu hình figma-ui-mcp
│   ├── figma-mcp-setup.md        Cài Figma Desktop plugin
│   └── impeccable-setup.md       Cài Impeccable skill pack
├── 02-workflow/
│   ├── figma-mcp-workflow.md     Cách dùng figma-ui-mcp: read/write/batch
│   ├── impeccable-workflow.md    Cách dùng 20 commands của Impeccable
│   └── combined-workflow.md      Workflow kết hợp cả 3 công cụ
├── 03-prompt-library/
│   └── prompts-vi.md             Prompt mẫu tiếng Việt cho TECOTEC/CCW
└── 04-reference/
    └── impeccable-cheatsheet.md  Bảng tra cứu nhanh 20 commands
```

---

## Yêu cầu

- macOS, Windows 10/11, hoặc Linux (Antigravity hỗ trợ cả 3 nền tảng)
- Figma Desktop (bắt buộc -- web app không hỗ trợ localhost)
- Node.js 18+
- Tài khoản Figma (Free trở lên)

---

## Liên hệ

Nếu gặp vấn đề khi setup hoặc dùng, liên hệ Phạm Tuyền hoặc tạo issue trong repo này.
