# Tổng quan Roadmap

> LC247 đang chuyển từ **Công cụ đo** sang **Đồng hành sức khoẻ** — qua 4 giai đoạn phát triển.

## Hướng đi

```
HIỆN TẠI              →   TƯƠNG LAI

Công cụ đo & ghi         Đồng hành chủ động
Nội dung tĩnh            Cá nhân hoá theo người, theo lúc
Chỉ bệnh nhân            + Người có nguy cơ + Người chăm sóc
Chỉ huyết áp             + Tiểu đường + Tim mạch + Đột quỵ
Ghi nhận chỉ số          Giảm lo lắng, trao cảm giác kiểm soát
```

## 4 giai đoạn phát triển (Build)

| Build | Tên | Mô tả | Giá trị |
|-------|-----|-------|---------|
| **0** | Nền tảng | CMS nội dung, mở rộng onboarding, pipeline sản xuất | Hạ tầng cho mọi thứ phía sau |
| **1** | Đồng hành cơ bản | Đánh giá nguy cơ tim mạch, content feed, diễn giải chỉ số, chiến dịch đột quỵ | App bắt đầu chủ động đến với user |
| **2** | Cá nhân hoá | Content theo giai đoạn bệnh + thời điểm, tool dinh dưỡng, caregiver mode | App biết user là ai, đưa đúng nội dung |
| **3** | Cộng đồng | Chia sẻ kinh nghiệm, Q&A, quiz, mở rộng tiểu đường, AI chatbot | Kết nối user với nhau, đa bệnh lý |

## Build 0 — Nền tảng

Chuẩn bị hạ tầng cho toàn bộ roadmap:

- **CMS nội dung**: Database với phân loại đầy đủ (ai, khi nào, nội dung gì)
- **Onboarding mở rộng**: Thêm câu hỏi về hút thuốc và vai trò (bệnh nhân / người chăm sóc) — dữ liệu cần cho đánh giá nguy cơ
- **Pipeline sản xuất**: Quy trình chuẩn để tạo nội dung ở 4 format khác nhau

## Build 1 — Đồng hành cơ bản

Chuyển LC247 từ "công cụ" sang "đồng hành" — app bắt đầu **chủ động** đến với user:

- **Đánh giá nguy cơ tim mạch** (WHO CVD Risk) → [Chi tiết](who-cvd-risk.md)
- **Content feed 3 lớp**: Lướt nhanh → Xem nhanh → Đọc sâu
- **Diễn giải chỉ số**: "HA tối thường cao hơn sáng 5-10 điểm, đây là bình thường"
- **Chiến dịch đột quỵ**: Workshop + content nhận biết FAST → [Chi tiết](dot-quy.md)
- **Nội dung dinh dưỡng**: Top 10 chủ đề phổ biến nhất → [Chi tiết](dinh-duong.md)

## Build 2 — Cá nhân hoá

App biết user là ai, ở giai đoạn nào, cần gì:

- **Content theo giai đoạn bệnh**: Mới chẩn đoán nhận "Hiểu về HA", không nhận "Quản lý thuốc"
- **Content theo thời điểm**: Sáng tip dinh dưỡng, tối bài tập thở, đêm content giảm lo
- **Tool dinh dưỡng cho BS & User**: BS xác định khung phần ăn, user tự chọn → [Chi tiết](dinh-duong.md)
- **Caregiver mode**: Nội dung riêng cho người chăm sóc (FAST, phục hồi, tâm lý)
- **Nhắc nhở thông minh**: Đo HA, uống thuốc, bữa ăn — theo lịch cá nhân, "đúng liều"

## Build 3 — Cộng đồng

Kết nối user với nhau, mở rộng phạm vi:

- **Chia sẻ kinh nghiệm**: Câu chuyện thực, có kiểm duyệt, có thể ẩn danh
- **Q&A cộng đồng**: Hỏi đáp với BS và user khác
- **Mở rộng tiểu đường**: Thêm theo dõi đường huyết bên cạnh HA
- **AI chatbot 24/7**: Trả lời câu hỏi thường gặp lúc nửa đêm
- **Tracking dinh dưỡng**: Quick log 3 emoji sau bữa ăn

## Nguyên tắc

1. **Build lean, validate sớm** — mỗi build có giả định rõ ràng, validate trước khi tiếp
2. **Giá trị tăng dần** — Build 1 đã tạo giá trị ngay, không cần chờ Build 3
3. **Data nuôi build sau** — Build 0 thu profile → Build 1 tính risk → Build 2 cá nhân hoá
4. **"Tính năng này giảm lo hay tạo thêm lo?"** — Câu hỏi trước mỗi quyết định

---

*Cập nhật: Tháng 2/2026*
