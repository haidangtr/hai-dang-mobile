# HỆ THỐNG WEBSITE BÁN ĐIỆN THOẠI CHÍNH HÃNG (HAI DANG MOBILE)
**Thư mục làm việc:** `/home/haidang/Code/hoc-ai/website-ban-dien-thoai`

Một ứng dụng web thương mại điện tử chuyên nghiệp, hoàn chỉnh và hiện đại: **HAI DANG MOBILE – Hệ Thống Bán Lẻ Điện Thoại Thông Minh Chính Hãng, Trả Góp 0% & Thu Cũ Đổi Mới**.

### 🎨 PHIÊN BẢN GIAO DIỆN DOANH NGHIỆP CAO CẤP (CORPORATE ENTERPRISE LIGHT EDITION):
* **Bảng màu thuần sáng & trang nhã:** Nền trắng tinh khiết (`#ffffff`), Slate 50 (`#f8fafc`), chữ tương phản cao Slate 900 (`#0f172a`), viền Slate 200 mảnh mai sang trọng kết hợp sắc đỏ doanh nghiệp (`#d32f2f`).
* **Top Trust Bar Doanh Nghiệp:** Hotline miễn cước 1800.6868, Hệ thống 120 Showroom toàn quốc, Cam kết 100% Chính hãng VN/A, Kênh bán hàng Doanh nghiệp (B2B).
* **4 Trụ Cột Cam Kết Vàng:** 100% Chính hãng VN/A, Giao hỏa tốc 1 giờ, 1 đổi 1 trong 30 ngày, Trả góp 0% duyệt online 5 phút.
* **Corporate Footer Uy Tín:** Mã số thuế DN, Giấy phép ĐKKD Sở KH&ĐT cấp, Huy hiệu "Đã thông báo Bộ Công Thương" và chứng chỉ SSL 256-bit Secure.

Toàn bộ ứng dụng được tối ưu hóa theo mô hình Jamstack tĩnh siêu nhẹ, chạy mượt mà trên mọi thiết bị và **sẵn sàng deploy trực tiếp lên Vercel chỉ với 1 click**.

---

## 🚀 HƯỚNG DẪN DEPLOY LÊN VERCEL (3 CÁCH)

Dự án đã tích hợp sẵn tệp cấu hình **[`vercel.json`](vercel.json)** với đầy đủ các tiêu chuẩn bảo mật (Security Headers) và định tuyến tĩnh.

### Cách 1: Deploy qua Vercel CLI (Nhanh nhất - 15 giây)
Nếu máy bạn đã cài `vercel` CLI:
```bash
cd /home/haidang/Code/hoc-ai/website-ban-dien-thoai
npx vercel
```
Làm theo hướng dẫn trên terminal, Vercel sẽ tự động cấp một tên miền miễn phí dạng: `https://haidang-mobile.vercel.app`.

### Cách 2: Deploy qua GitHub / GitLab
1. Khởi tạo kho lưu trữ Git và đẩy code lên GitHub:
   ```bash
   cd /home/haidang/Code/hoc-ai/website-ban-dien-thoai
   git init
   git add .
   git commit -m "Initial Hai Dang Mobile deployment"
   git branch -M main
   git remote add origin https://github.com/[username]/[repo-name].git
   git push -u origin main
   ```
2. Truy cập [vercel.com](https://vercel.com) ➔ Chọn **Add New Project** ➔ Chọn repo vừa tạo ➔ Nhấn **Deploy**.

### Cách 3: Test trên máy cục bộ (Local Test)
* **Mở trực tiếp:** Nhấp đúp chuột vào tệp [`index.html`](file:///home/haidang/Code/hoc-ai/website-ban-dien-thoai/index.html) hoặc mở terminal:
  ```bash
  xdg-open /home/haidang/Code/hoc-ai/website-ban-dien-thoai/index.html
  ```
* **Chạy máy chủ cục bộ:**
  ```bash
  cd /home/haidang/Code/hoc-ai/website-ban-dien-thoai
  python3 -m http.server 3000
  ```
  Truy cập: `http://localhost:3000`

---

## 🌟 CÁC TÍNH NĂNG ĐỘT PHÁ CỦA HAI DANG MOBILE

### 1. Ma trận Biến thể Điện thoại Động (Dynamic Variant Selector)
* Hỗ trợ đầy đủ các dòng Flagship hàng đầu: iPhone 16 Pro Max, 16 Pro, S24 Ultra, Z Fold 6, Xiaomi 14 Ultra, Vivo X100 Pro, OPPO Find N3...
* Khách đổi **Dung lượng** (*128GB, 256GB, 512GB, 1TB*) ➔ Giá tự động cập nhật theo thời gian thực (Zero delay).
* Khách đổi **Màu sắc** (*Titan Sa Mạc, Titan Tự Nhiên, Đen, Trắng...*) ➔ Ảnh điện thoại tương ứng đổi theo ngay lập tức.

### 2. Bộ Tính Trả Góp 0% Tự Động (Installment Calculator)
* Cho phép chọn mức trả trước (20%, 30%, 50%, 70%) và kỳ hạn (3, 6, 9, 12 tháng).
* Tự động tính chính xác **số tiền cần trả trước** và **số tiền phải trả mỗi tháng** không phát sinh lãi suất ẩn.

### 3. Công Cụ So Sánh Cấu Hình Thông Minh (Side-by-Side Comparison)
* Chọn tối đa 3 điện thoại bất kỳ trên sàn để đối đầu.
* Bảng so sánh trực quan các thông số cốt lõi: Màn hình, Chipset, Camera, Pin/Sạc, Trọng lượng và Hệ điều hành.

### 4. Thu Cũ Đổi Mới Lên Đời (Trade-in Valuation Simulator)
* Tự động định giá máy cũ của khách hàng dựa trên đời máy và tình trạng máy (Loại 1, Loại 2, Loại 3).
* Cộng thêm **Trợ giá 2.000.000₫** và tính toán chính xác số tiền chênh lệch khách cần bù thêm.

### 5. Flash Sale Giờ Vàng (Live Countdown Timer)
* Đồng hồ đếm ngược giờ vàng giảm giá kịch sàn thúc đẩy tỷ lệ chuyển đổi.
* Thanh tiến độ thể hiện độ "cháy hàng" của từng đợt khuyến mãi.

### 6. Giỏ Hàng & Thanh Toán Chuẩn Bản Địa (VietQR + COD)
* Áp dụng mã Voucher giảm giá: `IPHONE2026` (giảm ngay 500.000₫), `FREESHIP`.
* Thanh toán bằng mã **VietQR động** (tự động tạo QR Techcombank kèm đúng số tiền và mã đơn hàng) hoặc Thanh toán khi nhận hàng (**COD**).

### 7. Quản Lý Đơn Hàng Của Tôi (Orders History)
* Lưu trữ an toàn trong `localStorage` của trình duyệt.
* Theo dõi mã đơn hàng `TECH-ORD-XXXXXX`, địa chỉ nhận, phương thức thanh toán, nút Hủy đơn và In hóa đơn.

---

## 📂 DANH MỤC TỆP TIN

* [**`index.html`**](file:///home/haidang/Code/hoc-ai/website-ban-dien-thoai/index.html): Ứng dụng web toàn diện, chứa toàn bộ HTML5, CSS3, JavaScript và dữ liệu sản phẩm.
* [**`vercel.json`**](file:///home/haidang/Code/hoc-ai/website-ban-dien-thoai/vercel.json): Tệp cấu hình định tuyến tĩnh và bảo mật chuẩn Vercel.
* [**`build_website.py`**](file:///home/haidang/Code/hoc-ai/website-ban-dien-thoai/build_website.py): Script tái tạo tự động mã nguồn khi cần tùy biến thêm sản phẩm.
