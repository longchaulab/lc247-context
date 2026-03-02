# Hướng dẫn sử dụng LC247

> Tài liệu hướng dẫn sử dụng LC247 (Long Châu 247) — mini-app quản lý sức khỏe mãn tính trong hệ sinh thái Nhà Thuốc Long Châu.

---

## Tài liệu này dành cho ai?

| Đối tượng | Mục đích |
|-----------|----------|
| **Người dùng mới** | Tự đọc để biết cách sử dụng app từ đầu đến cuối |
| **Nhân viên nhà thuốc** | Hướng dẫn khách hàng sử dụng app tại quầy hoặc qua điện thoại |

> **Quy ước trong tài liệu:**
> - Các bước thao tác được đánh số **1, 2, 3...**
> - Ảnh chụp app minh họa ở mỗi bước quan trọng
> - Ký hiệu `[Bản thân]` và `[Người nhà]` đánh dấu chỗ khác nhau giữa 2 mode
> - Block `Tip nhân viên` chứa ghi chú riêng cho nhân viên nhà thuốc

---

## Mục lục — Theo thứ tự user flow

| # | Trang | Nội dung |
|---|-------|----------|
| 0 | [Cài đặt & Mở app](0-cai-dat-mo-app.md) | Cách tìm và mở LC247 từ app Nhà Thuốc Long Châu |
| 1 | [Onboarding](1-onboarding.md) | Chọn mode Bản thân / Người nhà, thiết lập ban đầu |
| 2 | [Trang chủ](2-trang-chu.md) | Tab Cá nhân, Tab Cả nhà, tổng quan giao diện |
| 3 | [Liên kết người thân](3-lien-ket-nguoi-than.md) | Thêm ba/mẹ/người thân vào vòng tròn gia đình |
| 4 | [Đo huyết áp](4-do-huyet-ap.md) | Đo bằng máy + Đo bằng quét khuôn mặt AI |
| 5 | [Xem báo cáo](5-xem-bao-cao.md) | Lịch màu, nhật ký đo, báo cáo tuần, tư vấn bác sĩ |
| 6 | [Kiến thức sức khỏe](6-kien-thuc.md) | Thư viện bài viết uy tín theo 4 chủ đề |
| 7 | [Gọi + Nhắn bác sĩ](7-goi-nhan-bac-si.md) | Chat 24/7, gọi khẩn cấp, tư vấn bác sĩ |
| 8 | [Xu & Phần thưởng](8-gamification.md) | Tích xu, thử thách 7 ngày, đổi quà tại nhà thuốc |
| 9 | [Câu hỏi thường gặp](9-cau-hoi-thuong-gap.md) | FAQ — giải đáp thắc mắc phổ biến |

---

## Sơ đồ user flow tổng quan

```
Mở app Long Châu
       |
       v
  Vào LC247 (mini-app)
       |
       v
  ┌─────────────────────┐
  │   ONBOARDING        │
  │                     │
  │  Chọn mode:         │
  │  [Bản thân]         │
  │  [Người nhà]        │
  │                     │
  │  Nhập thông tin     │
  │  Cài nhắc nhở      │
  └────────┬────────────┘
           |
           v
  ┌─────────────────────┐
  │   TRANG CHỦ         │
  │                     │
  │  Tab Cá nhân        │
  │  Tab Cả nhà         │
  │                     │
  │  [+ Thêm người thân]│
  └────────┬────────────┘
           |
     ┌─────┼─────────────────────┐
     |     |                     |
     v     v                     v
  ┌──────┐ ┌──────────┐  ┌────────────┐
  │ ĐO   │ │ BÁO CÁO  │  │ KIẾN THỨC  │
  │      │ │          │  │            │
  │Máy đo│ │Lịch màu  │  │4 chủ đề    │
  │Face  │ │Nhật ký   │  │Bài viết    │
  │Scan  │ │Tuần      │  │            │
  └──┬───┘ └──────────┘  └────────────┘
     |
     v
  ┌──────────────────────────────────┐
  │  KẾT QUẢ + LỜI KHUYÊN BÁC SĨ   │
  │  +10 xu thưởng                   │
  └──────────────────────────────────┘
     |
     ├──> Gọi/Nhắn bác sĩ (24/7)
     └──> Xu & Phần thưởng (đổi quà)
```

---

## LC247 là gì?

**LC247 (Long Châu 247)** là mini-app nằm trong app Nhà Thuốc Long Châu, giúp bạn:

- **Đo huyết áp** — bằng máy đo hoặc quét khuôn mặt AI (~40 giây)
- **Nhận tư vấn bác sĩ thực** — sau mỗi lần đo, bác sĩ gửi lời khuyên cá nhân
- **Theo dõi gia đình** — thêm ba/mẹ/người thân, xem chỉ số từ xa
- **Tích xu đổi quà** — đo đều đặn để nhận thưởng tại 1.700+ nhà thuốc Long Châu
