# LC247 — Product Content Hub

Bộ khung nội dung sản phẩm LC247 (Long Châu 247) — mini-app quản lý sức khoẻ mãn tính trong hệ sinh thái Nhà Thuốc Long Châu.

## Đây là gì

Repo này là **single source of truth** cho toàn bộ nội dung sản phẩm LC247. Mỗi file content được tổ chức theo 4 lớp, từ đó chế biến ra nhiều format output khác nhau.

```
Content Source (Markdown)
        │
        ├── → Slide (Key Messages + Tóm tắt + Screenshot)
        ├── → GitBook (Full file, sync trực tiếp)
        ├── → PDF (Tóm tắt + Chi tiết + Kết quả)
        └── → Docs (Full file, chỉnh format)
```

## Cấu trúc

| Thư mục | Nội dung |
|---------|---------|
| [`gioi-thieu/`](gioi-thieu/README.md) | LC247 là gì, hệ sinh thái Long Châu |
| [`tinh-nang/`](tinh-nang/dashboard.md) | 6 tính năng chính — mô tả + hướng dẫn + screenshots |
| [`sap-ra-mat/`](sap-ra-mat/noi-dung-ca-nhan-hoa.md) | Tính năng đang phát triển |
| [`screenshot/`](screenshot/) | Ảnh chụp màn hình app |
| [`_build/`](_build/) | Hướng dẫn chế biến, templates, output (không hiện trên GitBook) |

## 4 lớp content

Mỗi file markdown được tổ chức theo 4 lớp:

| Lớp | Mục đích | Dùng cho |
|-----|---------|---------|
| **Key Messages** | 3-4 bullet points cốt lõi | Slide, banner, elevator pitch |
| **Tóm tắt** | 2-3 câu đủ hiểu giá trị | Slide body, PDF summary, social |
| **Chi tiết** | Full content + screenshots | GitBook, docs đầy đủ |
| **Kết quả** | Benefits người dùng nhận được | Slide CTA, landing page |

## Sử dụng

- **Đọc online:** Kết nối repo với [GitBook](https://gitbook.com) qua Git Sync → render từ `SUMMARY.md`
- **Đọc local:** Mở `SUMMARY.md` để xem mục lục
- **Tạo slide/PDF/docs:** Xem hướng dẫn trong [`_build/formats/`](_build/formats/README.md)

## Cập nhật

Tháng 2/2026 — Phiên bản đầu tiên. Tổ chức lại theo bộ khung 4 lớp.
