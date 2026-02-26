# Hệ sinh thái Long Châu

LC247 không hoạt động đơn lẻ. Nó nằm trong hệ sinh thái Long Châu rộng hơn:

```
                    ┌──────────────────┐
                    │  Nhà thuốc       │
                    │  Long Châu       │
                    │  1,700+ cửa hàng │
                    └────────┬─────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
     ┌────────▼───────┐ ┌───▼────────┐ ┌──▼──────────────┐
     │ App Long Châu  │ │ Chiến dịch │ │ Bác sĩ &        │
     │ (Mua thuốc)    │ │ cộng đồng  │ │ Chuyên gia      │
     │                │ │ (Workshop)  │ │ (Tư vấn, DD)    │
     └────────┬───────┘ └─────┬──────┘ └──────┬───────────┘
              │               │               │
              └───────────────┼───────────────┘
                              │
                    ┌─────────▼─────────┐
                    │    LONG CHÂU 247  │
                    └───────────────────┘
```

## Các kết nối

| Thành phần | Vai trò với LC247 |
|-----------|-------------------|
| **Nhà thuốc Long Châu** | Kênh acquisition: NV/Dược sĩ giới thiệu LC247 khi khách mua thuốc HA. Trust cao nhất |
| **App Long Châu (NTLC)** | "Outer app" chứa LC247. Khách mua thuốc online → gợi ý dùng LC247 |
| **Workshop đột quỵ** | Buổi giáo dục sức khoẻ offline → quét QR đăng ký LC247. Kênh acquisition offline |
| **BS tư vấn LC247** | Bác sĩ xem chỉ số HA và gửi lời khuyên sau mỗi lần đo |
| **BS dinh dưỡng** | Chuyên gia mới có tại Long Châu → nguồn chuyên môn cho content & tool dinh dưỡng |
| **TS.BS chuyên khoa** | Cung cấp knowledge base (bài giảng, WHO guidelines) cho tính năng & nội dung |

## Dòng chảy người dùng

```
Người bình thường                 Bệnh nhân mãn tính
      │                                  │
      │ Workshop / Video / Banner        │ Mua thuốc / NV tư vấn
      │                                  │
      └──────────┬───────────────────────┘
                 │
                 ▼
         Biết đến LC247 → Đăng ký
                 │
                 ▼
         Đánh giá nguy cơ (WHO CVD Risk)
                 │
        ┌────────┼────────┐
        ▼        ▼        ▼
    Bệnh nhân  Người    Người
    (quản lý   chăm     quan tâm
     bệnh)    sóc      (phòng ngừa)
```
