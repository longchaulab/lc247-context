# Hướng dẫn tạo Slide

## Nguồn content

Mỗi slide tương ứng 1 file content trong `gioi-thieu/`, `tinh-nang/`, hoặc `sap-ra-mat/`.

## Cách trích xuất

Từ mỗi file content, lấy:

| Phần slide | Lấy từ lớp | Ví dụ |
|-----------|-----------|-------|
| **Title slide** | `# Tên tính năng` + `> Tagline` | "Đo huyết áp — Đo mọi lúc mọi nơi" |
| **Bullet points** | `## Key Messages` | 3-4 bullets chính |
| **Body text** | `## Tóm tắt` | 2-3 câu mô tả |
| **Visual** | Screenshot từ `## Chi tiết` | Chọn 1-2 ảnh đại diện nhất |
| **CTA / Closing** | `## Kết quả người dùng nhận được` | Danh sách benefits |

## Cấu trúc slide deck gợi ý

```
1. Cover          — LC247 là gì (gioi-thieu/README.md → tagline)
2. Problem        — Tại sao cần LC247 (tự viết từ context)
3. Solution       — Tổng quan tính năng (gioi-thieu/README.md → Key Messages)
4. Feature 1      — Đo huyết áp (tinh-nang/2-do-huyet-ap.md)
5. Feature 2      — Báo cáo (tinh-nang/3-bao-cao.md)
6. Feature 3      — Gia đình (tinh-nang/4-gia-dinh.md)
7. Feature 4      — Kiến thức (tinh-nang/5-kien-thuc.md)
8. Feature 5      — Hỗ trợ (tinh-nang/6-ho-tro.md)
9. Feature 6      — Xu & Phần thưởng (tinh-nang/7-gamification.md)
10. Ecosystem     — Hệ sinh thái (gioi-thieu/he-sinh-thai.md)
11. Coming Soon   — Sắp ra mắt (sap-ra-mat/*)
12. CTA           — Tổng hợp Kết quả từ tất cả files
```

## Quy ước

- **Mỗi slide:** 1 Key Message chính + 1 visual (screenshot hoặc icon)
- **Text tối đa:** 30 từ/slide (trừ slide chi tiết)
- **Font:** Đồng nhất, ưu tiên Be Vietnam Pro hoặc system font
- **Màu:** Theo brand LC247 — primary blue (#2B7DE9), accent orange (#FF9500)

## Template

Xem template HTML tại `templates/slide/` để tham khảo layout và design system.
