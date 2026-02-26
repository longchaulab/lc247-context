# Data & Analytics

> Tài liệu nội bộ — hệ thống dữ liệu và dashboard LC247.

## Nguồn dữ liệu

| Nguồn | Loại | Mô tả |
|-------|------|-------|
| **Snowplow SDK** | Hành vi app | Screen view, tap, scroll, funnel step — từ iOS/Android |
| **App backend** | Sức khoẻ | Kết quả đo HA, BMI, đường huyết, survey, hồ sơ gia đình |

Data tổng hợp về **CADSHOUSE** — data warehouse FRT Group. Delay: ~51 phút.

## 3 bảng dữ liệu chính

| Bảng | Nội dung | Key filter |
|------|---------|-----------|
| fact_lc_tracking_user_behavior | Sự kiện trong app | `device_screen_location LIKE 'lc247%'` |
| fact_lc247_surveys | Hồ sơ sức khoẻ (onboarding) | 1 dòng = 1 profile |
| fact_lc247_health_measurement | Kết quả đo (HA, BMI, đường huyết) | 1 dòng = 1 lần đo |

## Dashboard hiện có

| Dashboard | Key insight |
|-----------|-----------|
| Tổng quan KPI | 4,162 users, ~300 active |
| Onboarding Funnel | 7,093 vào → 3,983 hoàn thành (56%) |
| User Segmentation | 92.6% inactive/short trial |
| Cohort Retention | Monthly + Weekly retention |
| Binah Analytics | 1,560 sessions, 84.2% success |

## Binah AI Camera

| Metric | Giá trị |
|--------|---------|
| Tổng sessions | 1,560 |
| Thành công | 84.2% |
| iOS | 87.3% |
| Android | 77.6% |
| Thời gian tối ưu | 31-45 giây |
| Retry trung bình | 7 lần (~3 phút) |

## Phân tích cộng đồng (Social Data)

- 3,744 bài Facebook (07/2023 – 02/2026)
- 49.4% lo lắng, 38.4% đăng 9PM-6AM
- 3 phiên bản dashboard deployed trên Vercel

## Known issues

| Issue | Mức độ |
|-------|--------|
| Cohort Monthly bỏ sót 96% Binah measurements | Critical |
| Monthly vs Weekly đếm retention khác nhau | Critical |
| 56% sessions Binah mất progress events | Medium |

---

*Source: cadhouse/*
*Cập nhật: Tháng 2/2026*
