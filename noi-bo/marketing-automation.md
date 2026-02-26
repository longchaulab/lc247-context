# Marketing Automation (Insider)

> Tài liệu nội bộ — chiến lược marketing automation qua Insider CDP.

## Trạng thái

- **NTLC (outer app):** ✅ Đã tích hợp Insider — push, email, in-app messaging
- **LC247 (inner mini-app):** 🔴 **Chưa tích hợp** — bottleneck chặn 24/32 use cases

## 32 Use Cases

### Group A: ACQUIRE — Thu hút từ LC → LC247 (5 UC)

Dùng dữ liệu mua thuốc. **Sẵn sàng chạy.**

| UC | Trigger | Trạng thái |
|----|---------|-----------|
| A1 | User mới NTLC | ✅ Đang chạy |
| A2 | Mua thuốc mãn tính | ✅ Đang chạy (10%) |
| A3 | Browse thuốc mãn tính | 🟡 Sẵn sàng |
| A4 | Thêm thuốc vào giỏ | 🟡 Sẵn sàng |
| A5 | Nhắc mua thuốc lại | 🟡 Sẵn sàng |

### Group B: USER JOURNEY — Hành trình trong LC247 (20 UC)

Cần dữ liệu LC247 (Tầng 2). **Chưa triển khai được.**

- Phase 1 (7 UC): Onboarding, drop recovery, content → risk, nudge đo
- Phase 2 (6 UC): Nhắc risk assessment, route theo nhóm A/B/C/D, re-assess
- Phase 3 (8 UC): **Nhắc đo HA hàng ngày** (ưu tiên cao nhất), cảnh báo HA bất thường, win-back, báo cáo tuần/tháng

### Group C: CROSS-CUTTING (7 UC)

| UC | Mô tả | Trạng thái |
|----|-------|-----------|
| C1 | Send Time Optimization | 🟡 Sẵn sàng |
| C2 | Sirius AI auto-optimization | 🟡 Sẵn sàng |
| C3 | Survey feedback | 🟡 Sẵn sàng |
| C4-C7 | NPS, churn detection, in-app, milestones | 🔴 Cần Tầng 2 |

## Tổng hợp

```
✅ Đang chạy:   2 UC
🟡 Sẵn sàng:    6 UC
🔴 Cần Tầng 2: 24 UC
```

**Quick wins:** Enable STO, Sirius AI, setup A5 (nhắc mua thuốc lại), welcome in-app, survey.

---

*Source: insider/Insider-plan/*
*Cập nhật: Tháng 2/2026*
