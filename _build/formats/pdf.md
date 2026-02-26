# Hướng dẫn xuất PDF

## Mục đích

Tạo tài liệu PDF cho:
- Gửi đối tác, stakeholder
- In ấn tại nhà thuốc, workshop
- Tài liệu training nội bộ

## Cách trích xuất

### PDF tóm tắt (1-2 trang)

Lấy từ mỗi file content:
- `# Tên tính năng` → heading
- `## Tóm tắt` → body text
- `## Kết quả` → closing

### PDF đầy đủ (nhiều trang)

Lấy toàn bộ file content, bỏ qua HTML comments. Giữ screenshots.

## Thứ tự nội dung gợi ý

```
1. Cover page      — LC247 + tagline
2. Giới thiệu      — gioi-thieu/README.md
3. Hệ sinh thái    — gioi-thieu/he-sinh-thai.md
4-9. Tính năng     — tinh-nang/*.md (theo thứ tự SUMMARY.md)
10. Sắp ra mắt     — sap-ra-mat/*.md
11. Liên hệ        — Thông tin hỗ trợ
```

## Quy ước

- **Page size:** A4
- **Margins:** 2cm
- **Font:** Be Vietnam Pro hoặc Roboto
- **Screenshots:** Scale về max-width 50% trang
- **Header/Footer:** Logo LC247 + số trang
