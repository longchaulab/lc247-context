# Product Slide Template

Template slide HTML dùng để giới thiệu sản phẩm mobile app. Thiết kế tối ưu cho việc showcase screenshot app thật trong phone frames.

**Demo:** Xem bản đã dùng cho LC247 tại https://lc247-demo.vercel.app

---

## Concept

- **Single-file HTML** — không cần build tool, mở trực tiếp trên browser
- **Horizontal scroll** — mỗi slide chiếm 100vw, chuyển slide bằng `translateX`
- **Phone frames** — khung điện thoại giả lập chứa screenshot thật từ app, có notch, shadow, label
- **Staggered animations** — nội dung fade-in lần lượt khi chuyển sang slide mới
- **Tối ưu cho 1280x800+** — thiết kế cho màn hình laptop/projector, không responsive mobile

---

## Theme & Colors

CSS variables định nghĩa trong `:root`:

| Variable | Giá trị | Dùng cho |
|----------|---------|---------|
| `--primary-blue` | `#2B7DE9` | Brand color chính — badge, bullet, nav button, gradient |
| `--primary-blue-light` | `#4A93ED` | Gradient cover, hero highlight |
| `--primary-blue-dark` | `#1a5cbf` | Hover state |
| `--accent-orange` | `#FF9500` | Badge "Sắp ra mắt" |
| `--accent-green` | `#34C759` | Trạng thái tốt, success |
| `--accent-red` | `#FF3B30` | Trạng thái nguy hiểm, cảnh báo |
| `--text-dark` | `#1a1a2e` | Text chính |
| `--text-secondary` | `#6B7280` | Body text, label |
| `--bg-gradient-start` | `#e8f4fc` | Background slide (gradient top) |
| `--bg-gradient-end` | `#f0f7fc` | Background slide (gradient bottom) |

**Đổi theme:** Chỉ cần sửa các biến trong `:root` — toàn bộ slide tự cập nhật.

---

## Typography

| Element | Font size | Weight | Ghi chú |
|---------|-----------|--------|---------|
| Cover title | 56px | 800 | Tên sản phẩm, letter-spacing -0.02em |
| Slide title | 36px | 800 | Tiêu đề mỗi tính năng |
| Centered title | 40px | 800 | Slide text-only |
| Key message | 15px | 500 | Bullet points, keyword in `<strong>` |
| Body text | 14px | 400 | Mô tả bổ sung, color secondary |
| Badge | 11px | 700 | Uppercase, letter-spacing 0.12em |
| Phone label | 12px | 600 | Caption dưới mỗi phone |

Font: **Be Vietnam Pro** (Google Fonts) — fallback: system fonts.

---

## 5 Slide Layouts

### 1. Cover (`slide-cover`)

Full-bleed gradient xanh, text trắng, căn giữa.

```html
<section class="slide slide-cover">
    <div class="cover-logo">[Tên công ty]</div>
    <h1 class="cover-title">[Tên sản phẩm]</h1>
    <p class="cover-subtitle">[Tagline]</p>
    <div class="cover-pills">
        <span class="cover-pill">[Highlight]</span>
    </div>
    <div class="cover-footer">[Footer text]</div>
</section>
```

### 2. Text + 3 Phones (`slide-left` + `phone-group`)

Tỷ lệ: **38% text / 62% phones.** Phổ biến nhất — dùng cho tính năng có 3 bước / 3 màn hình.

```html
<section class="slide">
    <div class="slide-content">
        <div class="slide-left">
            <span class="slide-badge">[Badge]</span>
            <h2 class="slide-title">[Title]</h2>
            <ul class="key-messages">
                <li><strong>[Key]</strong> — [Detail]</li>
            </ul>
            <p class="body-text">[Body]</p>
        </div>
        <div class="slide-right">
            <div class="phone-group">
                <!-- 3x phone-wrapper -->
            </div>
        </div>
    </div>
</section>
```

### 3. Text + 2 Phones Wide (`slide-left-wide` + `phone-group-2`)

Tỷ lệ: **42% text / 58% phones.** Phone lớn hơn (240x518px). Dùng khi cần text nhiều + 2 ảnh chi tiết.

```html
<div class="slide-left-wide">...</div>
<div class="slide-right">
    <div class="phone-group phone-group-2">
        <!-- 2x phone-wrapper với .phone-frame-lg -->
    </div>
</div>
```

### 4. Text-only Centered (`slide-centered`)

Max-width 900px, căn giữa. Dùng cho diagram, icon cards, tổng quan.

```html
<section class="slide">
    <div class="slide-centered">
        <span class="slide-badge">[Badge]</span>
        <h2 class="slide-title">[Title]</h2>
        <div class="icon-cards">
            <!-- 4x icon-card -->
        </div>
    </div>
</section>
```

Components phụ có sẵn trong CSS:
- `.icon-cards` — grid 2x2 cards
- `.benefits-list` — grid 2 cột, mỗi item là card ✅

### 5. Hero Variant (`slide-hero`)

Không phải layout riêng — là **modifier** thêm vào bất kỳ layout nào. Tạo hiệu ứng highlight cho tính năng nổi bật:

- Background gradient nhạt hơn (light blue tint)
- Title chuyển thành gradient text
- Phone frames có blue shadow

```html
<section class="slide slide-hero">
    <!-- Kết hợp với bất kỳ layout nào ở trên -->
    <span class="slide-badge badge-hero">Tính năng nổi bật</span>
    ...
</section>
```

---

## Phone Frame Component

| Variant | Class | Size | Border-radius |
|---------|-------|------|---------------|
| Standard | `.phone-frame` | 200 x 432 px | 32px |
| Large | `.phone-frame` + `.phone-frame-lg` | 240 x 518 px | 38px |

Cấu trúc HTML:

```html
<div class="phone-wrapper">
    <div class="phone-frame">           <!-- hoặc .phone-frame .phone-frame-lg -->
        <div class="phone-screen">
            <div class="phone-notch"></div>
            <img src="path/to/screenshot.png" alt="Mô tả" loading="lazy">
        </div>
    </div>
    <p class="phone-label">[Caption]</p>
</div>
```

- Screenshot dùng `object-fit: cover` + `object-position: top center` — auto-fill screen
- Notch tự căn giữa, kích thước tỷ lệ theo phone size
- Shadow: multi-layer (ambient + direct) tạo chiều sâu

---

## Animations

Khi slide nhận class `.active`, nội dung fade-in theo thứ tự:

| Thứ tự | Element | Delay |
|--------|---------|-------|
| 1 | Badge | 0.1s |
| 2 | Title | 0.2s |
| 3 | Key message 1 | 0.3s |
| 4 | Key message 2 | 0.35s |
| 5 | Key message 3 | 0.4s |
| 6 | Body text | 0.5s |
| 7 | Phone 1 | 0.3s |
| 8 | Phone 2 | 0.45s |
| 9 | Phone 3 | 0.6s |

Hiệu ứng: `opacity: 0 → 1` + `translateY(20px → 0)`, duration 0.5s, easing `ease`.

---

## Navigation

| Input | Action |
|-------|--------|
| `→` hoặc `Space` | Slide tiếp theo |
| `←` | Slide trước |
| `Home` | Về slide đầu |
| `End` | Đến slide cuối |
| `F` | Toggle fullscreen |
| Click vùng 2/3 phải | Slide tiếp |
| Click vùng 1/3 trái | Slide trước |
| Swipe trái (>50px) | Slide tiếp |
| Swipe phải (>50px) | Slide trước |
| URL `#3` | Nhảy đến slide 3 |

Nav bar ở bottom center: pill-shaped, backdrop blur, chứa nút prev/next + counter.

---

## Cách sử dụng

### Bước 1: Copy template

```bash
cp template.html ten-san-pham-slide.html
```

### Bước 2: Thay nội dung placeholder

Tìm tất cả `[...]` trong file — đó là placeholder cần thay:
- `[Tên sản phẩm]`, `[Tên công ty]`, `[Tagline]`
- `[Tên tính năng]`, `[Keyword]`, `[Mô tả]`
- Ảnh: thay `src` trong `<img>` bằng path đến screenshot thật

### Bước 3: Thêm / xóa slide

- Copy 1 `<section>` phù hợp → paste vào vị trí mong muốn
- Cập nhật `data-slide` cho đúng thứ tự (1, 2, 3, ...)
- JS tự detect tổng số slide — **không cần sửa JS**
- Counter trong HTML (`<span id="total">5</span>`) chỉ là giá trị khởi tạo, JS sẽ ghi đè

### Bước 4: Đổi theme (nếu cần)

Sửa CSS variables trong `:root`:

```css
:root {
    --primary-blue: #YOUR_COLOR;
    --bg-gradient-start: #YOUR_BG;
    /* ... */
}
```

### Bước 5: Test

Mở file HTML trực tiếp trên browser. Kiểm tra:
- Phone frames hiển thị ảnh đúng
- Navigation hoạt động (keyboard + click)
- Animations chạy mượt

---

## Lưu ý

- **Viewport tối ưu:** 1280x800 trở lên. Phone frames có thể bị cắt ở viewport nhỏ hơn.
- **Ảnh screenshot:** Nên dùng ảnh portrait ratio (~9:19.5) để fit phone frame. Ảnh auto-crop từ top.
- **Số slide:** Không giới hạn, nhưng 10-15 slide là lý tưởng cho 1 buổi trình bày.
- **Font:** Cần internet để load Google Fonts. Offline thì fallback về system font.
