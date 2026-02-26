# Đánh giá nguy cơ tim mạch (WHO CVD Risk)

> Tính nguy cơ nhồi máu / đột quỵ trong 10 năm tới — chuyển từ "xem từng chỉ số riêng" sang "nhìn tổng thể nguy cơ".

## Vấn đề

- "Đo 3 lần ra 3 số khác nhau" — 484 bài trên cộng đồng
- Thiết bị đo mà **không diễn giải** = tạo thêm lo lắng
- User nhìn từng chỉ số riêng lẻ nhưng không hiểu **tổng thể** nguy cơ của mình

## Giải pháp: WHO CVD Risk Calculator

### Non-lab (ưu tiên đầu tiên)

Không cần xét nghiệm máu. Chỉ cần 5 yếu tố:

| Yếu tố | LC247 đã có? |
|---------|-------------|
| Tuổi | ✅ Từ hồ sơ |
| Giới tính | ✅ Từ hồ sơ |
| Huyết áp tâm thu | ✅ Từ dữ liệu đo |
| BMI | ✅ Từ dữ liệu đo |
| Hút thuốc | ❌ Cần thêm 1 câu hỏi |

→ App đã có **4/5 yếu tố**. Chỉ cần thêm 1 câu hỏi khi onboarding.

### 4 nhóm nguy cơ (WHO PEN Protocol)

| Nhóm | Nguy cơ 10 năm | Màu | Ý nghĩa |
|------|----------------|-----|---------|
| **A** | < 5% | Xanh lá | Duy trì lối sống lành mạnh |
| **B** | 5 – 10% | Vàng | Cần cải thiện — thay đổi lối sống |
| **C** | 10 – 20% | Cam | Cần can thiệp — theo dõi sát + XN máu |
| **D** | ≥ 20% | Đỏ | Hành động khẩn — kết nối BS ngay |

### Kịch bản theo nhóm

| | Nhóm A | Nhóm B | Nhóm C | Nhóm D |
|---|---|---|---|---|
| **Tone** | Tích cực | Nhẹ nhàng | Nghiêm túc | Khẩn trương (không gây hoảng) |
| **Content** | 1 tip/tuần | 2-3 tips/tuần | Plan 3 tháng | Trấn an + hướng dẫn thuốc |
| **Tần suất đo HA** | 1 lần/tuần | 2 lần/tuần | 2-3 lần/tuần | Hàng ngày (sáng + tối) |
| **Kết nối BS** | Không | Không | Khi HA ≥140/90 | Ngay lập tức |
| **Xét nghiệm máu** | Không | Không | Khuyến nghị | Khuyến nghị mạnh |
| **Đánh giá lại** | 12 tháng | 3 tháng | 3-6 tháng | 3 tháng |

### Trường hợp đặc biệt → Tự động nhóm D

- Tiền sử đột quỵ / nhồi máu cơ tim
- Huyết áp ≥160/100 dai dẳng (3+ lần liên tiếp)
- Tiểu đường kèm bệnh tim mạch

### Người dưới 40 tuổi

WHO chart không áp dụng cho người <40. Giải pháp: hướng dẫn trực tiếp vào Phase 3 (Phòng ngừa) hoặc Phase 4 (nếu đã có bệnh), không hiển thị risk score.

## Flow 2 tầng: Non-lab → Lab

```
Non-lab (sàng lọc tất cả user ≥40)
│
├─ Nhóm A, B (< 10%) → Tư vấn lối sống + theo dõi
│
└─ Nhóm C, D (≥ 10%) → Khuyến nghị xét nghiệm máu
                         │
                         ▼
                      Lab-based → Kết quả chính xác hơn
                                  (việc của BS quyết định điều trị)
```

## Vòng lặp cải thiện

```
Đo HA đều → Risk score giảm → User thấy tiến bộ
Ăn tốt hơn → BMI giảm → Risk score giảm → Motivation tăng
```

Risk score không phải để "dán nhãn" — mà để user **thấy hành động của mình có kết quả**.

---

*Cập nhật: Tháng 2/2026*
