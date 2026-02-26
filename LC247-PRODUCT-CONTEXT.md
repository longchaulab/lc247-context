# LC247 — Product Context

> Tài liệu tổng hợp mô tả sản phẩm Long Châu 247.
> Cập nhật: Tháng 2/2026

---

## LC247 là gì

**Long Châu 247** là tính năng quản lý sức khoẻ mãn tính nằm trong app Nhà Thuốc Long Châu (FPT Retail). Không phải app độc lập — là mini-app kích hoạt cho khách hàng đã đăng ký. Đối tượng chính: bệnh nhân tăng huyết áp và người thân chăm sóc họ.

LC247 kết nối trực tiếp với hệ sinh thái Long Châu: nhà thuốc (1,700+ cửa hàng), bác sĩ tư vấn, BS dinh dưỡng, workshop cộng đồng, và dịch vụ gọi khẩn cấp.

---

## Tính năng hiện tại

**Vòng lặp cốt lõi:** Đo huyết áp → Ghi chỉ số → Xem báo cáo → Nhận lời khuyên bác sĩ

| Tính năng | Mô tả |
|-----------|-------|
| **Đo huyết áp** | 2 cách: nhập tay/chụp ảnh máy đo + quét khuôn mặt AI (Binah, ~40 giây). Kết quả SYS/DIA/Pulse, phân loại mức độ bằng màu, lời khuyên BS sau mỗi lần đo |
| **Dashboard** | Lời chào cá nhân, chỉ số HA gần nhất, nhắc nhở đo, thư viện kiến thức (4 tag) |
| **Vòng tròn gia đình** | Quản lý nhiều hồ sơ sức khoẻ trong 1 tài khoản (bản thân + người thân) |
| **Báo cáo** | Nhật ký đo (lịch + biểu đồ), nhật ký tư vấn BS, theo dõi BMI |
| **Hỗ trợ** | Chat 24/7, gọi khẩn cấp (nút giữa navigation), gọi tư vấn BS |
| **Gamification** | +10 Xu khi đo HA, popup chúc mừng, tích điểm nhận quà |

**Điểm mạnh:** Face scan khác biệt, vòng tròn gia đình, kết nối BS trực tiếp.

**Giới hạn:** Toàn bộ reactive (chờ user hành động), kiến thức tĩnh (ai cũng nhận cùng nội dung), chưa chạm cảm xúc, chỉ phục vụ giai đoạn "đang điều trị".

---

## User thực tế

**4,162 users** đã onboard. Nhưng **92.6%** thuộc nhóm "thử rồi bỏ" (34.6%) hoặc "chưa bao giờ đo" (57.7%). Chỉ 4.9% đo HA hàng tuần.

**Insight cốt lõi** (từ phân tích 3,744 bài Facebook cộng đồng tim mạch):

> **Bệnh nhân mãn tính không thiếu thông tin — họ thiếu sự an tâm.**

- 49.4% bài mang tâm trạng lo lắng, chỉ 2.1% tích cực
- 38.4% câu hỏi đăng từ 9PM–6AM — cô đơn nhất lúc nửa đêm, không có ai hỏi nên lên Facebook
- Nỗi sợ lớn nhất: "phải uống thuốc cả đời" (746 bài, 76% lo lắng) — sợ phụ thuộc, không phải sợ tác dụng phụ
- "Đo 3 lần ra 3 số khác nhau" (484 bài) — thiết bị đo mà không diễn giải = tạo thêm lo
- Sau đột quỵ, bệnh nhân biến mất — 86% bài phục hồi do **người nhà** đăng

---

## Hướng đi: Tool → Companion → Platform

| Chiều | Hiện tại | Hướng đến |
|-------|----------|-----------|
| Mô hình | Công cụ đo & ghi (reactive) | Đồng hành chủ động (proactive) |
| Nội dung | Thư viện tĩnh, ai cũng như nhau | Cá nhân hoá theo vai trò, giai đoạn bệnh, thời điểm |
| Đối tượng | Bệnh nhân đang điều trị | Mở rộng: người có nguy cơ + người chăm sóc (caregiver) |
| Phạm vi | Huyết áp đơn lẻ | Đa bệnh lý: HA + tiểu đường + tim mạch + đột quỵ |
| Giá trị | Ghi nhận chỉ số | Giảm lo lắng, trao lại cảm giác kiểm soát |

---

## Bốn hướng đầu tư chính (Q1/2026)

### 1. Nội dung sức khoẻ thông minh

Chuyển từ thư viện tĩnh sang phân phối "đúng người, đúng lúc, đúng cách, đúng liều":
- **4 format**: Tip Card (10-30s) · Article (2-5 phút) · Infographic/Slider (30-60s) · Video (30s-3 phút)
- **6 chủ đề**: Huyết áp · Dinh dưỡng · Vận động · Thuốc · Đột quỵ · Tinh thần
- **3 lớp trải nghiệm**: Feed lướt (2s) → Quick View (10-30s) → Long Form (2-5 phút)
- Phân theo vai trò (bệnh nhân / caregiver) + giai đoạn bệnh + thời điểm trong ngày
- **Đã sản xuất**: 43 nội dung (21 demo + 22 repurposed). Pipeline: JSON → Airtable CMS → App

### 2. Đánh giá nguy cơ tim mạch (WHO CVD Risk)

Tính nguy cơ nhồi máu / đột quỵ trong 10 năm tới — chuyển từ "xem từng chỉ số riêng" sang "nhìn tổng thể nguy cơ":
- **Non-lab trước** (không cần xét nghiệm): 5 yếu tố — tuổi, giới, HA, BMI, hút thuốc. App đã có 4/5, chỉ cần thêm 1 câu hỏi
- **4 nhóm nguy cơ** (WHO PEN Protocol): A (<5%, duy trì) · B (5-10%, cải thiện) · C (10-20%, can thiệp) · D (≥20%, hành động khẩn)
- Mỗi nhóm có kịch bản riêng: tone content, tần suất đo, kết nối BS, lịch đánh giá lại
- Nhóm C-D khuyến nghị xét nghiệm máu → mở đường cho phiên bản lab-based chính xác hơn

### 3. Dinh dưỡng

Triết lý: **"Phần ăn đơn giản" thay vì tính calorie phức tạp** (theo TS.BS Phan Hữu Hên, BV Chợ Rẫy). 1 chén cơm ≈ 1 tô bún ≈ 2 lát bánh mì. BS xác định khung, bệnh nhân tự chọn thức ăn mình thích.

Triển khai 4 bước tuần tự:
1. **Content** — Tip + Infographic theo bữa ăn (rào cản thấp nhất, validate quan tâm)
2. **Tool cho BS** — App tính khung phần ăn, BS điều chỉnh, gửi BN
3. **Tool cho User** — Tự xem khung + gợi ý bữa ăn + what-if (giảm BMI → giảm risk)
4. **Tracking** — Quick log 3 emoji → pilot chụp hình AI (chỉ khi bước 3 đã work)

Vòng lặp: Ăn tốt → BMI giảm → Risk score giảm → User thấy cải thiện → Motivation tăng.

### 4. Chiến dịch đột quỵ

Workshop thí điểm đã tổ chức (01/2026). Insight: nội dung nhận biết FAST và sơ cứu **không đúng tệp bệnh nhân** (khi xảy ra đột quỵ, họ không tự nhận biết được) — **tệp đúng là con cái / người chăm sóc**. Workshop là kênh acquisition cho LC247 (quét QR đăng ký).

---

## Hành trình user (4 phase)

```
PHASE 1: ENTRY                 PHASE 2: RISK              PHASE 3: PREVENTION       PHASE 4: MANAGEMENT
"Tôi vừa biết LC247"           "Nguy cơ tôi thế nào?"     "Tôi cần thay đổi gì?"    "Sống chung với bệnh"

7 kênh: mua thuốc,             WHO CVD Risk (1 phút)      Dinh dưỡng 4 bước         Core loop nâng cấp
workshop, NV tư vấn,           → 4 nhóm A/B/C/D           Content theo bữa ăn       Diễn giải thông minh
SEO, video, banner,            Mỗi nhóm có kịch bản       Lối sống                  Reframe nỗi sợ thuốc
truyền thông                   hành động riêng            Gamification              Nighttime companion
                                                                                     Caregiver features
```

**Hiện tại** app chỉ phục vụ tốt Phase 4. Phase 1-3 đang được mở rộng.

---

## Roadmap (4 Build)

| Build | Tên | Nội dung chính | Giá trị |
|-------|-----|---------------|---------|
| **0** | Nền tảng | CMS nội dung, mở rộng onboarding, pipeline sản xuất | Hạ tầng cho mọi thứ phía sau |
| **1** | Đồng hành cơ bản | WHO CVD Risk, content feed 3 lớp, diễn giải chỉ số, chiến dịch đột quỵ, content DD top 10 | App bắt đầu chủ động đến với user |
| **2** | Cá nhân hoá | Content theo phase bệnh + thời điểm, tool DD cho BS & user, caregiver mode, nhắc nhở thông minh | App biết user là ai, đưa đúng nội dung |
| **3** | Cộng đồng | Chia sẻ kinh nghiệm, Q&A, quiz, mở rộng tiểu đường, AI chatbot 24/7, DD tracking | Kết nối user với nhau, đa bệnh lý |

Mindset: Build lean, validate sớm. Không gắn timeline cứng. Data từ build trước nuôi build sau.

---

## Marketing Automation (Insider)

Đã tích hợp Insider CDP với app NTLC (outer app). **Chưa tích hợp LC247** (inner mini-app) — đây là bottleneck chặn 24/32 use cases. Master plan có 32 use cases xuyên suốt hành trình: acquire từ mua thuốc → onboarding → risk assessment → đo HA hàng ngày → báo cáo tuần → win-back.

Quick wins sẵn sàng: STO, Sirius AI auto-optimization, nhắc mua thuốc lại, survey, welcome in-app message.

---

## Số liệu snapshot (02/2026)

| | Giá trị |
|---|---------|
| Users onboarded | 4,162 |
| Đo HA hàng tuần | 205 (4.9%) |
| Onboarding completion | 56% |
| Binah face scan success | 84.2% (1,560 sessions) |
| Content đã sản xuất | 43 pieces (5 formats) |
| Insider use cases | 32 (2 đang chạy, 6 sẵn sàng, 24 cần tích hợp) |
| Facebook posts phân tích | 3,744 (49.4% lo lắng) |

---

## Nguyên tắc xuyên suốt

1. **Giảm lo lắng trước, kiến thức sau** — "Tính năng này giảm lo cho user, hay tạo thêm lo?"
2. **Đón nhận, không educate** — Không cố giáo dục tất cả, chỉ đón người đã quan tâm sẵn
3. **Caregiver không phải user phụ** — 86% bài phục hồi do người nhà đăng
4. **Đơn giản, hành động ngay** — "Phần ăn" thay vì calorie, tip 10-30s thay vì bài dài
5. **Đúng liều** — 2-3 tips/ngày, không bombardment

---

*Tổng hợp từ: 20+ thư mục dự án, 3,744 bài Facebook, 4,162 user records, 43 nội dung sức khoẻ, 32 Insider use cases, 1 workshop thí điểm, WHO CVD Risk guidelines*
