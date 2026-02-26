# CLAUDE.md — Hướng dẫn cho Claude Code

## Project này là gì?

Đây là **content repo** (không phải code app). Chứa nội dung sản phẩm LC247 (Long Châu 247) — mini-app quản lý sức khoẻ mãn tính trong hệ sinh thái Nhà Thuốc Long Châu.

Nguyên tắc: **Viết 1 lần trong markdown → chế biến ra nhiều format** (slide web, GitBook, PDF, docs).

## Cấu trúc project

```
gioi-thieu/          ← 2 file giới thiệu sản phẩm
tinh-nang/           ← 7 file tính năng (đánh số 1→7, hero feature = 2-do-huyet-ap.md)
sap-ra-mat/          ← 2 file tính năng đang phát triển
screenshot/          ← 22 ảnh PNG chụp từ app thật
_build/              ← Tooling: formats/, templates/, output/
  output/lc247-product-slide.html  ← Slide web 14 trang (deploy Vercel)
README.md            ← Onboarding guide
TODO.md              ← Danh sách việc cần làm
SUMMARY.md           ← Mục lục GitBook
vercel.json          ← Cấu hình deploy (rewrite "/" → slide HTML)
```

## Bộ khung 4 lớp content

Mỗi file content tổ chức theo 4 lớp. Khi sửa content, **giữ nguyên cấu trúc này**:

```markdown
## Key Messages
<!-- Dùng cho: slide, elevator pitch, banner -->
- 3-4 bullet points cốt lõi

## Tóm tắt
<!-- Dùng cho: slide body, PDF summary -->
2-3 câu tóm gọn giá trị

## Chi tiết
<!-- Dùng cho: GitBook, docs đầy đủ -->
Mô tả đầy đủ + ảnh chụp app

## Kết quả người dùng nhận được
<!-- Dùng cho: slide CTA, landing page -->
- ✅ Lợi ích cụ thể
```

Dòng `<!-- Dùng cho: ... -->` là comment ẩn chỉ mục đích — **không xoá**.

## Quy tắc khi sửa nội dung

- **Ngôn ngữ**: Tiếng Việt, giọng thân thiện, dễ hiểu
- **Ảnh**: Lưu vào `screenshot/`, đặt tên `tên-tính-năng-mô-tả.png` (viết thường, gạch ngang)
- **Chèn ảnh**: `<img src="../screenshot/ten-anh.png" alt="Mô tả" width="300">`
- **TODO trong content**: Dùng HTML comment `<!-- TODO: mô tả việc cần làm -->`
- **Không thêm emoji** trừ khi user yêu cầu (ngoại trừ ✅ ở phần Kết quả)

## Slide web

- File: `_build/output/lc247-product-slide.html` — 1 file HTML chứa tất cả 14 slide + CSS + JS
- Deploy: Vercel tự deploy khi merge vào main → https://lc247-demo.vercel.app
- Khi sửa slide, test local bằng preview tools trước khi commit
- **Lưu ý**: Phone frames bị cắt ở viewport < 1280px (known issue)

## Git workflow

- Branch `main` có **branch protection** — không push trực tiếp
- Tuy nhiên owner có thể bypass (enforce_admins=false)
- Repo public: https://github.com/longchaulab/lc247-context
- Commit message bằng tiếng Việt

## Trạng thái hiện tại

- Phase 1 (xây khung content) — **DONE**
- Sắp đổi tên sản phẩm: LC247 → **"Bác Sĩ Long Châu 247"** (~59 chỗ, 14 file)
- Phase 2 (bổ sung chi tiết) — chưa bắt đầu
- Xem TODO.md để biết chi tiết việc cần làm
