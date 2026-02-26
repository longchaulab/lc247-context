# LC247 — Product Content Hub

## Mục tiêu dự án này là gì?

Chào mừng bạn đến với repo **LC247 Product Content Hub**!

**LC247 (Long Châu 247)** là mini-app quản lý sức khoẻ mãn tính, nằm trong hệ sinh thái Nhà Thuốc Long Châu. App giúp người dùng đo huyết áp, nhận tư vấn bác sĩ, theo dõi sức khoẻ gia đình — tất cả trong 1 app.

Repo này **không phải code** của app. Đây là nơi chứa toàn bộ **nội dung sản phẩm** (mô tả tính năng, hướng dẫn sử dụng, screenshots) — phục vụ cho việc tạo tài liệu, slide, và truyền thông.

### Ý tưởng cốt lõi: Source of Truth

Thay vì viết nội dung riêng lẻ cho từng format (1 bản cho slide, 1 bản cho docs, 1 bản cho web...), mình **viết 1 lần duy nhất** trong các file markdown ở repo này. Đây là **nguồn sự thật duy nhất (source of truth)**.

Từ bộ khung content này, mình chế biến ra nhiều định dạng output khác nhau:

```
📝 Content Source (các file .md trong repo này)
        │
        │   Viết 1 lần, dùng nhiều nơi:
        │
        ├── 🎬 Slide web  ← đã có v1, xem tại link bên dưới
        ├── 📊 Slide PDF   ← chưa làm
        ├── 📖 GitBook     ← sync trực tiếp từ repo
        └── 📄 PDF / Docs  ← chưa làm
```

### Xem output hiện tại

Slide web (14 trang, có ảnh minh hoạ): **https://lc247-demo.vercel.app**

> Mở link trên browser → dùng phím ← → hoặc click để chuyển slide. Nhấn F để fullscreen.

---

## Bộ khung 4 lớp content

Mỗi file markdown trong repo được tổ chức theo **4 lớp**. Mỗi lớp phục vụ cho 1 mục đích khác nhau:

| Lớp | Nội dung gì | Dùng ở đâu |
|-----|------------|-----------|
| **Key Messages** | 3-4 bullet points cốt lõi nhất | Tiêu đề slide, banner, giới thiệu nhanh |
| **Tóm tắt** | 2-3 câu tóm gọn giá trị | Nội dung slide, post mạng xã hội |
| **Chi tiết** | Mô tả đầy đủ + ảnh chụp app | GitBook, tài liệu training, docs |
| **Kết quả** | Lợi ích người dùng nhận được | Call-to-action, landing page |

### Ví dụ thực tế

Đây là cách file `tinh-nang/2-do-huyet-ap.md` được tổ chức:

```markdown
## Key Messages
<!-- Dùng cho: slide, elevator pitch, banner -->
- **2 cách đo** — bằng máy đo huyết áp hoặc quét khuôn mặt AI chỉ ~40 giây
- **★ Đo bằng khuôn mặt AI** — không cần thiết bị, chỉ cần camera
- **Bác sĩ thực tư vấn** — sau mỗi lần đo, BS gửi lời khuyên cá nhân

## Tóm tắt
<!-- Dùng cho: slide body, PDF summary -->
LC247 cho phép đo huyết áp bằng 2 cách: nhập kết quả từ máy đo hoặc
quét khuôn mặt AI ~40 giây qua camera điện thoại...

## Chi tiết
<!-- Dùng cho: GitBook, docs đầy đủ -->
### Cách 1: Đo bằng máy
(mô tả từng bước + ảnh chụp app)

### ★ Cách 2: Đo bằng khuôn mặt AI
(mô tả từng bước + ảnh chụp app)

## Kết quả người dùng nhận được
<!-- Dùng cho: slide CTA, landing page -->
- ✅ Đo huyết áp mọi lúc — bằng máy hoặc chỉ cần camera
- ✅ Lời khuyên từ bác sĩ thực (không phải chatbot)
```

Dòng `<!-- Dùng cho: ... -->` là comment ẩn — nó giúp bạn biết lớp đó dùng cho format nào, nhưng không hiển thị khi render.

---

## Danh sách file trong project

### Content (nội dung sản phẩm — phần quan trọng nhất)

```
gioi-thieu/                         ← Giới thiệu sản phẩm
  ├── README.md                       LC247 là gì, giá trị cốt lõi
  └── he-sinh-thai.md                 Hệ sinh thái Long Châu (nhà thuốc, app, workshop, BS)

tinh-nang/                          ← 7 tính năng chính (đánh số theo thứ tự)
  ├── 1-trang-chu.md                  Trang chủ — chào đón, tổng quan sức khoẻ, nhắc nhở
  ├── 2-do-huyet-ap.md                ★ Đo huyết áp — máy đo + quét khuôn mặt AI (hero feature)
  ├── 3-bao-cao.md                    Báo cáo sức khoẻ — lịch màu, nhật ký, báo cáo tuần
  ├── 4-gia-dinh.md                   Vòng tròn gia đình — theo dõi ba mẹ từ xa
  ├── 5-kien-thuc.md                  Kiến thức sức khoẻ — thư viện bài viết uy tín
  ├── 6-ho-tro.md                     Hỗ trợ & liên lạc — chat 24/7, gọi khẩn cấp
  └── 7-gamification.md               Xu & phần thưởng — tích điểm đổi quà

sap-ra-mat/                         ← Tính năng đang phát triển
  ├── noi-dung-ca-nhan-hoa.md         Nội dung cá nhân hoá — content theo vai trò, FAST
  └── danh-gia-nguy-co.md             Đánh giá nguy cơ tim mạch — theo chuẩn WHO
```

### Screenshots (ảnh chụp app)

```
screenshot/                         ← 22 ảnh PNG chụp từ app thật
  ├── home-*.png                      Trang chủ (2 ảnh)
  ├── do-*.png                        Đo huyết áp (7 ảnh — nhiều nhất vì là hero feature)
  ├── bao-cao-*.png                   Báo cáo (4 ảnh)
  ├── gia-dinh-*.png                  Gia đình (2 ảnh)
  ├── kien-thuc-*.png                 Kiến thức (1 ảnh)
  ├── ho-tro-*.png                    Hỗ trợ (1 ảnh)
  ├── xu-*.png                        Xu & thưởng (2 ảnh)
  └── ...                             Và vài ảnh phụ trợ khác
```

> **Quy tắc đặt tên ảnh:** `tên-tính-năng` + `-` + `mô-tả-ngắn` + `.png`
> Ví dụ: `do-face-scan-dang-do.png` = tính năng Đo + phương pháp Face Scan + trạng thái Đang đo

### Tooling (công cụ hỗ trợ — không phải content)

```
_build/                             ← Thư mục tooling (GitBook tự bỏ qua thư mục bắt đầu bằng _)
  ├── formats/                        Hướng dẫn chế biến content ra từng format
  │     ├── README.md                   Tổng quan 4 lớp content
  │     ├── slide.md                    Cách tạo slide từ content
  │     ├── gitbook.md                  Cách sync với GitBook
  │     ├── pdf.md                      Cách xuất PDF
  │     └── docs.md                     Cách xuất Google Docs / Word
  │
  ├── templates/                      Template tham khảo
  │     └── slide/remixed-*.html        HTML template slide (dùng để tham khảo design)
  │
  └── output/                         File output đã tạo
        └── lc247-product-slide.html    ← Slide web 14 trang (deploy trên Vercel)
```

### File cấu hình

```
README.md           ← Bạn đang đọc file này
SUMMARY.md          ← Mục lục cho GitBook (danh sách tất cả trang content)
vercel.json         ← Cấu hình deploy Vercel (trỏ "/" → slide HTML)
.gitignore          ← File Git bỏ qua
```

---

## Hướng dẫn làm việc

### GitHub — cách sửa content

Repo này sử dụng **branch protection** trên nhánh `main`. Nghĩa là bạn **không push trực tiếp vào main** được — phải tạo branch riêng và mở Pull Request.

#### Bước 1: Clone repo về máy

```bash
git clone https://github.com/longchaulab/lc247-context.git
cd lc247-context
```

#### Bước 2: Tạo branch mới

Mỗi lần sửa content, tạo 1 branch riêng:

```bash
git checkout -b ten-cua-ban/mo-ta-viec-lam
# Ví dụ:
git checkout -b minh/bo-sung-journey-do-huyet-ap
```

#### Bước 3: Sửa file

Mở các file `.md` bằng bất kỳ text editor nào (VS Code, Cursor, Typora...). Sửa nội dung, thêm ảnh, thêm video — thoải mái.

> **Tip:** Nếu dùng VS Code, cài extension **Markdown Preview** để xem preview khi sửa.

#### Bước 4: Commit và push

```bash
git add .
git commit -m "Mô tả ngắn việc bạn đã sửa"
git push origin ten-branch-cua-ban
```

#### Bước 5: Tạo Pull Request

1. Vào https://github.com/longchaulab/lc247-context
2. GitHub sẽ hiện banner "Compare & pull request" → click vào
3. Viết mô tả ngắn → bấm **Create pull request**
4. Chờ review → khi được approve → **Merge**

Khi merge vào main, Vercel sẽ **tự động deploy** bản mới.

### Vercel — slide web

- **Link:** https://lc247-demo.vercel.app
- **Cách hoạt động:** Mỗi khi code merge vào `main`, Vercel tự build và deploy lại
- **Slide web** là file `_build/output/lc247-product-slide.html` — 1 file HTML duy nhất chứa tất cả 14 slide, CSS, và JavaScript
- Vercel rewrite URL `/` → file HTML đó (cấu hình trong `vercel.json`)

Bạn **không cần làm gì với Vercel** — chỉ cần merge PR vào main là xong.

### Đọc content ở local

Nếu muốn đọc nhanh mà không cần mở GitHub:

1. Mở file `SUMMARY.md` — đây là **mục lục tổng** của tất cả trang content
2. Click vào link tương ứng để đọc từng file

---

## Roadmap — Việc cần làm

### Phase 1: Xây khung content (Source of Truth) — DONE

Đã hoàn thành:
- 11 file markdown mô tả đầy đủ sản phẩm (2 giới thiệu + 7 tính năng + 2 sắp ra mắt)
- 22 screenshots từ app thật
- Tổ chức theo bộ khung 4 lớp (Key Messages / Tóm tắt / Chi tiết / Kết quả)
- Slide web v1 — 14 slide, deploy tại https://lc247-demo.vercel.app

### Phase 2: Review & bổ sung chi tiết — TO DO

> **Đây là việc tiếp theo dành cho bạn.** Khung đã có, giờ cần đi sâu vào từng tính năng để bổ sung chi tiết.

Cụ thể cần làm:

**a) Đọc lại từng file, bổ sung mô tả chi tiết hơn:**
- Mô tả rõ hơn journey/luồng sử dụng (user mở app → làm gì → nhận kết quả gì)
- Bổ sung các edge case, lưu ý, tips mà user cần biết
- Kiểm tra thông tin đã chính xác chưa (tên bác sĩ, chỉ số mẫu, v.v.)

**b) Ghép video hướng dẫn vào từng bước:**
- Tìm/quay video hướng dẫn phù hợp cho từng tính năng
- Thêm vào file markdown ở vị trí phù hợp, dùng format:
  ```markdown
  > 🎬 **Video hướng dẫn:** [Tên video](link-youtube-hoac-drive)
  ```

**c) Hoàn thiện các TODO:**
- Trong các file content có sẵn comment `<!-- TODO: ... -->` đánh dấu chỗ cần bổ sung
- Tìm tất cả TODO bằng cách search `TODO` trong repo
- Ví dụ trong `tinh-nang/2-do-huyet-ap.md`:
  ```
  <!-- TODO: Bổ sung chi tiết sau:
  - Công nghệ rPPG hoạt động thế nào
  - Độ chính xác so với máy đo truyền thống
  - Điều kiện ánh sáng / môi trường tối ưu
  -->
  ```

**d) Thêm screenshot mới (nếu cần):**
- Chụp ảnh từ app, lưu vào thư mục `screenshot/`
- Đặt tên theo quy tắc: `tên-tính-năng-mô-tả.png` (viết thường, dùng dấu gạch ngang)
- Trong file markdown, chèn ảnh:
  ```markdown
  <img src="../screenshot/ten-anh.png" alt="Mô tả ảnh" width="300">
  ```

### Phase 3: Tạo output formats — TO DO

Sau khi Phase 2 hoàn thiện:
- Cập nhật slide web (hiện là v1, cần update nội dung theo bổ sung ở Phase 2)
- Xuất slide PDF
- Các format khác nếu cần

---

## Cập nhật

| Thời gian | Nội dung |
|-----------|---------|
| Tháng 2/2026 | Phiên bản đầu tiên — xây khung 4 lớp, build slide web v1 |
