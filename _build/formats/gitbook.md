# Hướng dẫn GitBook

## Cách hoạt động

GitBook sync trực tiếp từ root repo qua Git Sync. File `SUMMARY.md` là mục lục.

## Cấu trúc

```
SUMMARY.md          ← Mục lục GitBook (bắt buộc)
gioi-thieu/         ← Section "Giới thiệu"
tinh-nang/          ← Section "Tính năng"
sap-ra-mat/         ← Section "Sắp ra mắt"
screenshot/         ← Ảnh (relative path từ content files)
```

## Content nào được hiển thị

GitBook render **toàn bộ file markdown** — bao gồm cả 4 lớp (Key Messages, Tóm tắt, Chi tiết, Kết quả). HTML comments (`<!-- -->`) sẽ không hiển thị cho người đọc.

## Lưu ý khi chỉnh sửa

- **SUMMARY.md** phải list đúng path đến mỗi file content
- **Image paths** dùng relative path: `../screenshot/ten-anh.png`
- **Links giữa files** dùng relative path: `do-huyet-ap.md` (cùng thư mục) hoặc `../gioi-thieu/README.md`
- **Không đổi tên file** đã có trong SUMMARY.md — sẽ break links

## Cập nhật

Khi thêm page mới:
1. Tạo file `.md` trong thư mục phù hợp
2. Thêm entry vào `SUMMARY.md`
3. Commit + push → GitBook tự sync
