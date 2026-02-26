# Câu hỏi mở & Quyết định

> Tài liệu nội bộ — các quyết định đã chốt và câu hỏi cần giải quyết.

## Decisions đã chốt

| Quyết định | Lý do |
|-----------|-------|
| Non-lab trước, lab sau | 4/5 data đã có, rào cản thấp |
| Dinh dưỡng 4 bước tuần tự | Validate từng bước, không đầu tư phức tạp sớm |
| "Phần ăn" thay vì calorie | Tính calorie quá phức tạp → bỏ cuộc (TS.BS Phan Hữu Hên) |
| Content FAST target caregiver | BN không tự nhận biết đột quỵ, caregiver mới cần |
| Event taxonomy layer (5 types) | Scale tốt, dễ maintain |
| Airtable làm CMS | Nhanh setup, đủ cho MVP, team non-dev dùng được |

## Câu hỏi mở

| # | Câu hỏi | Ảnh hưởng |
|---|---------|-----------|
| 1 | Dùng HA **lần đo gần nhất** hay **trung bình 7 ngày** cho risk? | Độ chính xác WHO Risk |
| 2 | Cho user chơi **what-if**? ("Bỏ thuốc lá → risk giảm bao nhiêu?") | Engagement cao nhưng tăng scope |
| 3 | Risk score hiện **trên trang chủ** hay mục riêng? | Visibility vs gây lo lắng |
| 4 | Face scan HA chấp nhận cho risk hay bắt buộc đo máy? | Coverage vs accuracy |
| 5 | User **<40 tuổi** trải nghiệm gì? | WHO chart không áp dụng <40 |
| 6 | Khi nào bắt đầu **lab-based** risk? | Phụ thuộc partnership XN |

## Assumptions cần validate

### Build 0
- User sẵn sàng trả lời thêm 1-2 câu hỏi onboarding (hút thuốc, vai trò)
- Đội ngũ sản xuất được 10 content/tuần

### Build 1
- User quan tâm risk score → A/B test + pilot tại workshop
- Face scan HA đủ chính xác cho risk → so sánh risk group face scan vs máy đo
- Content push buổi tối giảm lo lắng → survey + đo cuộc gọi khẩn cấp

### Build 2
- User phân biệt được BN vs caregiver khi onboarding
- Tip DD đơn giản thay đổi hành vi → survey 4 tuần + đo BMI
- BS sẵn sàng dùng tool DD (≤15 giây/BN) → pilot 5-10 BS

## Constraints

| Constraint | Ảnh hưởng |
|-----------|-----------|
| Insider Tầng 2 chưa tích hợp | Chặn 24/32 marketing use cases |
| 92.6% user inactive | User base nhỏ cho mọi tính năng mới |
| Content gaps (vận động, tinh thần) | 2/6 chủ đề chưa có nội dung |
| BS chỉ có 1-5 phút tư vấn DD | Cần tool hỗ trợ |
| Data delay 51 phút | Không real-time cho alerts |

## Rủi ro

| Rủi ro | Impact |
|--------|--------|
| Risk score gây thêm lo lắng | Cao — test tone + framing trước |
| Chatbot AI trả lời sai | Rất cao — chỉ FAQ, BS review |
| Workshop không scale được | Trung bình — đo conversion, pilot online |

---

*Cập nhật: Tháng 2/2026*
