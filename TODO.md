# TODO — Việc cần làm

> File này track tất cả việc cần làm trong project. Mỗi việc đánh dấu trạng thái:
> - ⬜ Chưa làm
> - 🔲 Đang làm
> - ✅ Xong

---

## 🔴 Ưu tiên cao

### Đổi tên sản phẩm: LC247 → Bác Sĩ Long Châu 247

Sản phẩm sắp đổi tên chính thức từ **"Long Châu 247" / "LC247"** thành **"Bác Sĩ Long Châu 247"**.

Cần review và đổi tên ở **tất cả** các nơi sau:

| # | File / Vị trí | Số lần xuất hiện | Trạng thái |
|---|--------------|-------------------|-----------|
| 1 | `README.md` | 5 lần | ⬜ |
| 2 | `SUMMARY.md` | 1 lần | ⬜ |
| 3 | `gioi-thieu/README.md` | 3 lần | ⬜ |
| 4 | `gioi-thieu/he-sinh-thai.md` | 9 lần | ⬜ |
| 5 | `tinh-nang/1-trang-chu.md` | 5 lần | ⬜ |
| 6 | `tinh-nang/2-do-huyet-ap.md` | 2 lần | ⬜ |
| 7 | `tinh-nang/3-bao-cao.md` | 1 lần | ⬜ |
| 8 | `tinh-nang/6-ho-tro.md` | 2 lần | ⬜ |
| 9 | `sap-ra-mat/noi-dung-ca-nhan-hoa.md` | 7 lần | ⬜ |
| 10 | `sap-ra-mat/danh-gia-nguy-co.md` | 8 lần | ⬜ |
| 11 | `_build/output/lc247-product-slide.html` | 6 lần | ⬜ |
| 12 | `_build/formats/slide.md` | 3 lần | ⬜ |
| 13 | `_build/formats/pdf.md` | 2 lần | ⬜ |
| 14 | `_build/formats/README.md` | 1 lần | ⬜ |

**Tổng: ~59 chỗ cần đổi trong 14 file.**

Lưu ý khi đổi:
- Quyết định viết tắt mới (vẫn dùng "LC247" hay đổi thành "BSLC247"?)
- Tên repo GitHub có cần đổi không? (`lc247-context` → ?)
- Tên domain Vercel có cần đổi không? (`lc247-demo.vercel.app` → ?)
- Kiểm tra ảnh screenshot — nếu app đã đổi tên trên UI thì cần chụp lại

---

## 🟡 Phase 2: Review & bổ sung chi tiết

### a) Bổ sung các luồng còn thiếu

Hiện tại content chỉ mô tả tính năng bên trong app. Còn thiếu các luồng quan trọng:

- ⬜ **Luồng vào app từ bên ngoài**: User đang ở app Nhà Thuốc Long Châu → vào LC247 bằng cách nào? Banner ở đâu, click vào đâu, flow chuyển tiếp ra sao?
- ⬜ **Onboarding lần đầu**: User mở LC247 lần đầu → phải khai báo những gì? (tên, tuổi, giới tính, tiền sử bệnh, thuốc đang dùng, v.v.) → flow từng bước
- ⬜ **Luồng dành cho caregiver**: Người thân (con/cháu) dùng app để theo dõi ba mẹ → flow khác gì so với user chính? Quyền gì, thấy gì, làm được gì?

> Cần tạo file mới hoặc bổ sung vào file hiện có (vd: `gioi-thieu/` cho luồng vào app, `tinh-nang/1-trang-chu.md` cho onboarding, `tinh-nang/4-gia-dinh.md` cho caregiver).

### b) Bổ sung nội dung chi tiết từng tính năng (đã có khung)

| # | File | Việc cần làm | Trạng thái |
|---|------|-------------|-----------|
| 1 | `tinh-nang/1-trang-chu.md` | Mô tả rõ journey: mở app → thấy gì → làm gì | ⬜ |
| 2 | `tinh-nang/2-do-huyet-ap.md` | Bổ sung chi tiết Face Scan AI (xem mục riêng bên dưới) | ⬜ |
| 3 | `tinh-nang/3-bao-cao.md` | Giải thích ý nghĩa từng loại báo cáo, cách đọc biểu đồ | ⬜ |
| 4 | `tinh-nang/4-gia-dinh.md` | Mô tả flow mời thành viên, quyền xem/sửa | ⬜ |
| 5 | `tinh-nang/5-kien-thuc.md` | Liệt kê chủ đề bài viết, nguồn nội dung | ⬜ |
| 6 | `tinh-nang/6-ho-tro.md` | Chi tiết kênh hỗ trợ, thời gian phản hồi | ⬜ |
| 7 | `tinh-nang/7-gamification.md` | Bảng quy đổi xu, danh sách phần thưởng | ⬜ |

### c) Bổ sung chi tiết Face Scan AI (hero feature)

Trong file `tinh-nang/2-do-huyet-ap.md` có các TODO cần hoàn thiện:

- ⬜ Công nghệ rPPG hoạt động thế nào (giải thích đơn giản)
- ⬜ Độ chính xác so với máy đo truyền thống (số liệu nếu có)
- ⬜ Điều kiện ánh sáng / môi trường tối ưu khi đo
- ⬜ Disclaimer y tế (Face Scan không thay thế thiết bị y tế)
- ⬜ Bảng so sánh Face Scan vs Máy đo (tốc độ, tiện lợi, độ chính xác)
- ⬜ Use cases phù hợp cho từng phương pháp đo

### d) Ghép video hướng dẫn

- ⬜ Tìm/quay video hướng dẫn cho từng tính năng chính
- ⬜ Ưu tiên: video Face Scan AI (demo trực quan nhất)
- ⬜ Embed vào file markdown theo format: `> 🎬 **Video:** [Tên](link)`

### e) Thêm screenshot mới (nếu cần)

- ⬜ Review lại 22 ảnh hiện có — ảnh nào đã cũ / không khớp UI mới?
- ⬜ Chụp bổ sung nếu app đã cập nhật giao diện
- ⬜ Đặt tên theo quy tắc: `tên-tính-năng-mô-tả.png`

### f) Kiểm tra thông tin chính xác

- ⬜ Tên bác sĩ, chức danh trong app có đúng không?
- ⬜ Chỉ số huyết áp mẫu có hợp lý không?
- ⬜ Số liệu (thời gian đo ~40 giây, v.v.) có chính xác không?
- ⬜ Link liên kết (nếu có) còn hoạt động không?

---

## 🟢 Phase 3: Tạo output formats

- ⬜ Cập nhật slide web theo nội dung bổ sung ở Phase 2
- ⬜ Xuất slide PDF từ slide web
- ⬜ Cân nhắc format khác nếu cần (Google Docs, Word)

---

## 💡 Cải thiện khác (không khẩn cấp)

- ⬜ **Slide responsive**: Phone frames bị cắt ở viewport nhỏ hơn 1280px — cần fix CSS
- ⬜ **GitBook sync**: Setup GitBook sync trực tiếp từ repo (đã plan nhưng chưa làm)
- ⬜ **Hoàn thiện bộ khung 4 lớp**: Một số file chưa đủ cả 4 lớp (Key Messages / Tóm tắt / Chi tiết / Kết quả) — review và bổ sung
- ⬜ **Thống nhất giọng văn**: Đảm bảo tất cả file dùng cùng tone (thân thiện, dễ hiểu, hướng đến người dùng cuối)
- ⬜ **Tính năng sắp ra mắt**: Cập nhật `sap-ra-mat/` khi có thông tin mới về Nội dung cá nhân hoá và Đánh giá nguy cơ tim mạch

---

## Cập nhật

| Ngày | Nội dung |
|------|---------|
| 26/02/2026 | Tạo file TODO.md — brainstorm danh sách việc cần làm |
| 26/02/2026 | Thêm TODO: 3 luồng còn thiếu (vào app từ ngoài, onboarding, caregiver) |
