# Danh Mục Đồ Án Môn Học (Foundation of AI Portfolio)

Website tĩnh đa trang (Multi-page static website) được xây dựng hoàn toàn bằng **HTML5 và CSS3 thuần (không dùng JavaScript)**, chuyên biệt cho việc lưu trữ, trình bày và giới thiệu các đồ án / bài tập lớn trong chương trình học.

---

## 1. Cấu Trúc Thư Mục Dự Án

```text
Foundation-of-AI/
├── README.md               # Giới thiệu tổng quan & hướng dẫn chi tiết cách thêm/sửa project
├── index.html              # Trang chủ hiển thị danh mục các đồ án (vừa vặn màn hình)
├── css/
│   └── style.css           # Toàn bộ CSS dùng chung, quản lý bằng CSS Variables
├── projects/
│   ├── project-1-contents/ # Thư mục chứa các tài liệu & trang con của đồ án 1
│   │   ├── system-architecture.html  # Chi tiết thiết kế kiến trúc hệ thống
│   │   └── benchmark-results.html    # Báo cáo kết quả thử nghiệm định lượng
│   ├── project-2-contents/ # Thư mục chứa các tài liệu & trang con của đồ án 2
│   │   ├── dataset-pipeline.html     # Quy trình tiền xử lý dữ liệu ảnh X-quang
│   │   └── model-evaluation.html     # Đánh giá chi tiết mô hình & ROC-AUC
│   ├── project-1.html      # Trang chi tiết đồ án mẫu 1 (A* Search & Pacman)
│   ├── project-2.html      # Trang chi tiết đồ án mẫu 2 (Deep CNN Medical Imaging)
│   └── project-3.html      # Trang chi tiết đồ án mẫu 3 (Q-Learning GridWorld)
└── assets/
    └── images/             # Nơi lưu trữ hình ảnh thumbnail và biểu đồ sơ đồ minh họa
        ├── project-1-thumb.svg
        ├── project-2-thumb.svg
        ├── project-3-thumb.svg
        ├── project-1-diagram.svg
        └── project-2-diagram.svg
```

---

## 2. Hướng Dẫn Nhanh Cách Chạy Trang Web

Trang web là tập hợp các file tĩnh thuần túy, bạn có thể chạy bằng một trong hai cách cực kỳ đơn giản:

### Cách 1: Mở trực tiếp bằng trình duyệt (Không cần cài đặt)
- Nhấp đúp chuột vào file `index.html` hoặc nhấp chuột phải chọn **Open With** &rarr; chọn trình duyệt bất kỳ (Google Chrome, Microsoft Edge, Firefox, Safari,...).
- Mọi trang con, hình ảnh và liên kết tương đối đều hoạt động ngay lập tức mà không cần máy chủ web.

### Cách 2: Sử dụng tiện ích Live Server (Khuyên dùng trong VS Code)
1. Cài đặt tiện ích mở rộng **Live Server** trên Visual Studio Code.
2. Mở thư mục dự án trên VS Code.
3. Nhấp chuột phải vào file `index.html` và chọn **Open with Live Server** (hoặc nhấn nút *Go Live* ở góc dưới cửa sổ VS Code).
4. Trang web sẽ mở tại địa chỉ cục bộ `http://127.0.0.1:5500`. Mọi thay đổi trong mã nguồn sẽ tự động tải lại trên trình duyệt.

---

## 3. Hướng Dẫn Từng Bước Cách Thêm Một Project Mới

Để thêm một đồ án mới vào danh mục, bạn chỉ cần thực hiện 3 bước đơn giản:

### Bước 1: Nhân bản file từ thư mục `projects/`
1. Vào thư mục `projects/`, sao chép file `project-1.html` và đổi tên thành `project-4.html` (hoặc tên gợi nhớ như `project-transformer.html`).
2. *(Tùy chọn)* Nếu đồ án có nhiều nội dung chuyên sâu, tạo thư mục con tương ứng `projects/project-4-contents/` và tạo các file con (ví dụ: `attention-mechanism.html`).

### Bước 2: Chỉnh sửa nội dung đồ án mới trong `project-4.html`
Mở file `project-4.html` vừa tạo và cập nhật các vị trí sau:
- **Thẻ `<title>`:** Đổi tên tiêu đề trang trên tab trình duyệt.
- **Tiêu đề & Thông tin Header:**
  ```html
  <h1 class="detail-title">04. Xây Dựng Mô Hình Transformer Dịch Máy Tự Động</h1>
  ```
- **Hộp thông tin Metadata:** Cập nhật ngày hoàn thành, thành viên, giảng viên hướng dẫn.

- **Nội dung bài viết:** Cập nhật các mục bài toán, phương pháp giải quyết, kết quả đạt được.
- **Liên kết nội dung con:** Trỏ tới file trong thư mục nội dung con:
  ```html
  <a href="project-4-contents/attention-mechanism.html" class="child-link-item">
    <span>📄 Xem phân tích chi tiết cơ chế Self-Attention</span>
    <span class="arrow">&rarr;</span>
  </a>
  ```
- **Ảnh minh họa:** Đặt ảnh mới vào `assets/images/project-4-diagram.svg` (hoặc `.png`, `.jpg`) và trỏ đường dẫn trong thẻ `<figure>`:
  ```html
  <img src="../assets/images/project-4-diagram.svg" alt="Sơ đồ kiến trúc Transformer">
  ```
- **Khối Tài nguyên & Liên kết:** Thay đổi đường dẫn GitHub, Báo cáo PDF, Slide báo cáo tương ứng.

> **Lưu ý về nút Home:** File nhân bản đã có sẵn nút icon ngôi nhà cố định ở góc dưới phải:
> ```html
> <a href="../index.html" class="floating-home-btn" aria-label="Quay về trang chủ" title="Quay về trang chủ">...</a>
> ```
> Bạn không cần phải viết lại CSS hay cấu trúc nút này.

### Bước 3: Thêm thẻ (Card) mới trong `index.html`
Mở file `index.html`, tìm đến khối `<section class="project-grid">` và thêm một thẻ mới:

```html
<!-- Project Card 4 -->
<a href="projects/project-4.html" class="project-card" aria-label="Xem chi tiết đồ án Transformer">
  <div class="card-thumbnail-box">
    <img src="assets/images/project-4-thumb.svg" alt="Minh họa đồ án 4">
  </div>
  <div class="card-body">
    <h2 class="card-title">04. Mô Hình Transformer Dịch Máy Tự Động</h2>
    <p class="card-desc">
      Triển khai kiến trúc Sequence-to-Sequence với cơ chế Multi-Head Attention dịch song ngữ Anh - Việt đạt điểm BLEU 34.2.
    </p>
    <div class="card-action">
      <span>Xem chi tiết đồ án</span>
      <span class="arrow">&rarr;</span>
    </div>
  </div>
</a>
```

*(Lưu ý: Theo đúng thiết kế chuẩn, các thẻ trên trang chủ không chứa tags và toàn bộ bề mặt thẻ đều có thể nhấp chuột trực tiếp để chuyển trang).*

---

## 4. Tùy Biến Giao Diện & Bảng Màu (CSS Variables)

Toàn bộ hệ thống giao diện được định nghĩa tập trung tại đầu file `css/style.css`. Bạn có thể thay đổi màu sắc chủ đạo của toàn bộ website trong vòng 10 giây bằng cách đổi các biến CSS:

```css
:root {
  /* Màu chủ đạo (Accent & Links) */
  --color-primary: #1d4ed8;       /* Xanh Cobalt đậm đà */
  --color-primary-hover: #1e3a8a; /* Xanh Navy khi hover */
  
  /* Màu chữ & Nền (Độ tương phản cao) */
  --text-main: #020617;          /* Màu chữ tiêu đề (đen đậm Slate-950) */
  --text-muted: #1e293b;         /* Màu chữ nội dung (Slate-800 đậm rõ nét) */
  --bg-page: #f1f5f9;            /* Màu nền trang Slate-100 */
  --bg-surface: #ffffff;         /* Màu nền thẻ Card trắng tinh khiết */
  
  /* Đường viền rõ nét phân biệt */
  --border-color: #64748b;       /* Đường viền Slate-500 sắc nét */
  --border-width: 2px;           /* Độ dày viền 2px */
}

/* Cỡ chữ cơ sở toàn trang (tăng thêm 2px: 18px) */
html {
  font-size: 18px;
}
```

---

## 5. Đặc Điểm Nổi Bật Về Kỹ Thuật (Design & Code Quality)

1. **Chuẩn ngữ nghĩa HTML5 & Tối ưu khả năng truy cập (A11y):** Sử dụng đầy đủ các thẻ ngữ nghĩa `<header>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<figcaption>`, `<nav>`, cùng các thuộc tính `aria-label` cho độc giả khiếm thị.
2. **High Contrast & Visual Boundary:** Tuân thủ tiêu chuẩn tương phản độ phân giải cao, đường viền rõ nét phân tách từng khối nội dung, không dùng các sắc pastel mờ nhạt.
3. **Căn chỉnh gọn gàng:** Trang chủ cân đối vừa vặn màn hình (viewport-fit), các trang chi tiết căn lề trái với khoảng hở tinh tế giữa nội dung và viền bao bọc.
4. **Không phụ thuộc thư viện ngoài:** Không tải bất kỳ thư viện JavaScript cồng kềnh nào (0 bytes JS), tốc độ tải trang đạt mức tối đa 100/100 Google PageSpeed.