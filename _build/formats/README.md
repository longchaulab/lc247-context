# Hướng dẫn chế biến format

Bộ khung content LC247 được tổ chức theo **4 lớp** trong mỗi file markdown. Tuỳ format output, bạn trích xuất lớp phù hợp.

## 4 lớp content

| Lớp | Dùng cho | Mô tả |
|-----|---------|-------|
| **Key Messages** | Slide title, banner, elevator pitch | 3-4 bullet points, ngắn gọn, gây ấn tượng |
| **Tóm tắt** | Slide body, PDF summary, social post | 2-3 câu đủ hiểu tính năng + giá trị |
| **Chi tiết** | GitBook, docs đầy đủ, training | Full content với screenshots, bảng, hướng dẫn |
| **Kết quả** | Slide CTA, landing page, quảng cáo | Danh sách benefits (✅) người dùng nhận được |

## Cách chế biến

```
                    ┌─────────────────┐
                    │  Content Source  │
                    │  (Markdown)     │
                    └────────┬────────┘
                             │
          ┌──────────────────┼──────────────────┐
          │                  │                  │
  ┌───────▼──────┐  ┌───────▼──────┐  ┌───────▼──────┐
  │    Slide     │  │   GitBook    │  │  PDF / Docs  │
  │              │  │              │  │              │
  │ Key Messages │  │  Full file   │  │ Tóm tắt +   │
  │ + Tóm tắt   │  │  (as-is)     │  │ Chi tiết     │
  │ + Kết quả   │  │              │  │ + Kết quả    │
  │ + Screenshot │  │              │  │              │
  └──────────────┘  └──────────────┘  └──────────────┘
```

## Các format

| Format | Hướng dẫn chi tiết | Trạng thái |
|--------|-------------------|------------|
| [Slide](slide.md) | Tạo slide thuyết trình từ content | Sẵn sàng |
| [GitBook](gitbook.md) | Sync với GitBook | Sẵn sàng |
| [PDF](pdf.md) | Xuất tài liệu PDF | Sẵn sàng |
| [Docs](docs.md) | Tạo Google Docs / Word | Sẵn sàng |

## Quy ước chung

- **Tone:** Thân thiện, dễ hiểu, hướng đến người dùng (không phải nội bộ kỹ thuật)
- **Ngôn ngữ:** Tiếng Việt, xưng hô "bạn" / "bác" (tuỳ ngữ cảnh)
- **Screenshots:** Dùng ảnh từ thư mục `screenshot/`, width=300 cho mobile
- **Emoji:** Dùng tiết chế, chỉ ở phần Kết quả (✅) và điểm nhấn
