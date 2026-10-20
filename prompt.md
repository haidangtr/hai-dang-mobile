# 🚀 MASTER SYSTEM PROMPT: XÂY DỰNG HỆ THỐNG WEBSITE BÁN ĐIỆN THOẠI DOANH NGHIỆP CAO CẤP (HAI DANG MOBILE)

> **Mục đích tài liệu:** Đây là bản đặc tả kỹ thuật và siêu prompt (Master Prompt) toàn diện, chuyên sâu chuẩn kiến trúc phần mềm thương mại điện tử. Bạn có thể sử dụng prompt này để nạp vào bất kỳ mô hình AI tiên tiến nào (Claude 3.7 Sonnet, GPT-4o, Gemini 1.5 Pro...) nhằm tái tạo, mở rộng hoặc chuyển giao hệ thống website bán lẻ điện thoại di động chính hãng cao cấp **Hai Dang Mobile** với đầy đủ 100% logic kinh doanh và giao diện doanh nghiệp thực thụ.

---

## 📋 MỤC LỤC KIẾN TRÚC
1. [Role & Persona Định Danh](#1-role--persona-định-danh)
2. [Bối Cảnh & Mục Tiêu Dự Án](#2-bối-cảnh--mục-tiêu-dự-án)
3. [Triết Lý Kiến Trúc Kỹ Thuật (Architecture Principles)](#3-triết-lý-kiến-trúc-kỹ-thuật)
4. [Hệ Thống Thiết Kế Doanh Nghiệp (Corporate Enterprise Light Design System)](#4-hệ-thống-thiết-kế-doanh-nghiệp)
5. [Cấu Trúc Mô Hình Dữ Liệu Chi Tiết (Product Data Schema)](#5-cấu-trúc-mô-hình-dữ-liệu-chi-tiết)
6. [Đặc Tả Logic & 8 Khối Tính Năng Doanh Nghiệp Cốt Lõi](#6-đặc-tả-logic--8-khối-tính-năng-doanh-nghiệp-cốt-lõi)
   * 6.1. Ma trận Biến thể Đa chiều (PDP Real-time Matrix)
   * 6.2. Bộ Tính Trả Góp 0% Lãi Suất Tự Động (Installment 0% Calculator)
   * 6.3. Định Giá Thu Cũ Lên Đời Trợ Giá (Trade-in Valuation Simulator)
   * 6.4. Ma Trận So Sánh Cấu Hình Đối Đầu (Head-to-Head Comparison)
   * 6.5. Flash Sale Giờ Vàng & Đồng Hồ Đếm Ngược (Live Countdown Engine)
   * 6.6. Bộ Lọc Đa Tiêu Chí & Tìm Kiếm Thông Minh (Search & Filter Engine)
   * 6.7. Giỏ Hàng & Cổng Thanh Toán VietQR Tự Động (VietQR Dynamic Checkout)
   * 6.8. Quản Lý Đơn Hàng & Đồng Bộ LocalStorage (Order Management & Persistence)
7. [Chân Trang Pháp Lý & Bộ Nhận Diện Uy Tín (Corporate Legal Trust Seals)](#7-chân-trang-pháp-lý--bộ-nhận-diện-uy-tín)
8. [Tiêu Chuẩn Đóng Gói & Deploy Vercel (Production Zero-Config)](#8-tiêu-chuẩn-đóng-gói--deploy-vercel)
9. [Nguyên Bản Master Prompt Dành Cho AI (Ready-to-use Prompt)](#9-nguyên-bản-master-prompt-dành-cho-ai)

---

## 1. ROLE & PERSONA ĐỊNH DANH

Khi nhận chỉ thị xây dựng website, AI phải đóng vai:
* **Principal Frontend Architect & E-Commerce Tech Lead:** Am hiểu sâu sắc về kiến trúc ứng dụng web tốc độ cao, quản trị state phản ứng nhanh (reactive state), tối ưu hóa luồng UX chuyển đổi (CRO - Conversion Rate Optimization).
* **Senior UI/UX Enterprise Designer:** Thành thạo quy chuẩn thiết kế các hệ thống bán lẻ công nghệ hàng đầu thế giới và Việt Nam (Apple Store, Thegioididong, FPT Shop, Viettel Store, CellphoneS). Phong cách thiết kế mang tính **Chính danh, Tin cậy, Tinh tế, Màu sáng (Light Mode), Chuẩn Doanh nghiệp (Enterprise)**.

---

## 2. BỐI CẢNH & MỤC TIÊU DỰ ÁN

* **Tên thương hiệu:** **HAI DANG MOBILE AUTHORIZED**
* **Khẩu hiệu:** *Hệ Thống Bán Lẻ Thiết Bị Di Động & Flagship Chính Hãng VN/A*
* **Mục tiêu:** Xây dựng một trang web thương mại điện tử bán lẻ điện thoại cao cấp độc lập, không phụ thuộc vào framework cồng kềnh (No React/Vue build step), tải trang tức thì dưới 0.8 giây, tích hợp đầy đủ mọi công cụ mua sắm chuyên sâu mà khách hàng thực tế đòi hỏi:
  * Xem cấu hình chi tiết và đổi biến thể màu sắc/bộ nhớ cập nhật giá tức thì.
  * Tự tính toán tiền trả góp 0% theo từng tháng.
  * Định giá máy cũ để lên đời máy mới có trợ giá.
  * Đặt hàng và quét mã VietQR tự động khớp số tiền và mã đơn.
  * Tra cứu và in hóa đơn đơn hàng ngay trên trình duyệt.

---

## 3. TRIẾT LÝ KIẾN TRÚC KỸ THUẬT

1. **Mô hình Jamstack Đơn Tệp (Single-File Architecture):** Toàn bộ HTML5, CSS3 hiện đại, và Vanilla JavaScript ES6+ được đóng gói chuẩn mực trong một tệp `index.html` duy nhất (hoặc script generator `build_website.py`).
2. **Không phụ thuộc thư viện ngoài (Zero Heavy Dependencies):** Không cần jQuery, không cần Tailwind build step cồng kềnh, không cần React runtime. Sử dụng CSS Variables thuần, Flexbox/Grid chuẩn W3C, Canvas/SVG biểu tượng mượt mà.
3. **Hiệu năng cực đại (Web Vitals 100/100):** Tối ưu FCP (First Contentful Paint < 0.4s), LCP (< 0.8s), CLS = 0.
4. **Bảo mật và Tương thích chuẩn Vercel:** Cung cấp kèm tệp `vercel.json` thiết lập đầy đủ HTTP Security Headers (`X-Content-Type-Options: nosniff`, `X-Frame-Options: SAMEORIGIN`, `Referrer-Policy: strict-origin-when-cross-origin`).

---

## 4. HỆ THỐNG THIẾT KẾ DOANH NGHIỆP (CORPORATE ENTERPRISE LIGHT DESIGN SYSTEM)

### Bảng Mã Màu (Design Tokens)
```css
:root {
  /* Bề mặt & Nền */
  --bg-page: #f8fafc;        /* Slate 50: Nền sáng dịu mắt, chống chói */
  --bg-card: #ffffff;        /* Trắng tuyệt đối cho thẻ sản phẩm & modal */
  --bg-subtle: #f1f5f9;      /* Slate 100: Khối phụ, badge cấu hình */
  
  /* Đường viền & Phân cách */
  --border: #e2e8f0;         /* Slate 200: Viền mảnh thanh lịch */
  --border-focus: #cbd5e1;   /* Slate 300: Khi hover / active */
  
  /* Văn bản & Tương phản */
  --text-main: #0f172a;      /* Slate 900: Chữ tiêu đề sắc nét, rõ ràng */
  --text-muted: #475569;     /* Slate 600: Mô tả phụ, thông số kỹ thuật */
  --text-dim: #94a3b8;       /* Slate 400: Nhãn mác nhỏ, placeholder */
  
  /* Màu sắc chủ đạo & Điểm nhấn Doanh nghiệp */
  --primary: #d32f2f;        /* Corporate Crimson: Đỏ thương hiệu, giá bán, CTA */
  --primary-hover: #b71c1c;  /* Đỏ đậm khi tương tác */
  --primary-light: #fef2f2;  /* Đỏ nền cực nhạt cho tag khuyến mãi */
  
  --emerald: #059669;        /* Xanh ngọc: Badge Chính Hãng, Trả góp 0%, Tiết kiệm */
  --emerald-light: #ecfdf5;
  --blue: #1d4ed8;           /* Xanh dương: Nút phụ, biểu tượng uy tín, đối đầu */
  
  /* Bo góc & Hiệu ứng đổ bóng */
  --radius-sm: 6px;
  --radius: 10px;
  --radius-lg: 14px;
  --shadow-sm: 0 1px 2px rgba(15, 23, 42, 0.05);
  --shadow: 0 4px 12px rgba(15, 23, 42, 0.08);
  --shadow-lg: 0 16px 36px rgba(15, 23, 42, 0.14);
}
```

### Thanh Niềm Tin Doanh Nghiệp (Top Trust Bar)
Hiển thị trên cùng toàn trang (Dark Slate `#0f172a` hoặc Pure Light), khẳng định năng lực doanh nghiệp:
* 🏬 **Hệ thống 120 Showroom toàn quốc**
* 📞 **Hotline miễn cước: 1800.6868 (8h00 - 21h30)**
* 🛡️ **Cam kết 100% Chính Hãng VN/A**
* ⚡ **Giao hàng hỏa tốc 1 giờ**
* 💼 **Bán hàng Doanh nghiệp (B2B - Báo giá số lượng lớn có VAT)**

### 4 Trụ Cột Cam Kết Vàng (Corporate Value Pillars)
Đặt ngay bên dưới Header, gia tăng niềm tin chuyển đổi:
1. **100% Chính Hãng VN/A:** Phân phối chính ngạch, bảo hành ủy quyền Apple & Samsung toàn quốc.
2. **Giao Hỏa Tốc 1 Giờ:** Miễn phí vận chuyển nội thành cho đơn hàng từ 5.000.000₫.
3. **1 Đổi 1 Trong 30 Ngày:** Lỗi phần cứng do nhà sản xuất đổi ngay máy mới nguyên seal.
4. **Trả Góp 0% Lãi Suất:** Trả trước từ 0đ, duyệt hồ sơ online qua CCCD chỉ trong 5 phút.

---

## 5. CẤU TRÚC MÔ HÌNH DỮ LIỆU CHI TIẾT (PRODUCT DATA SCHEMA)

Hệ thống phải quản lý tối thiểu **20 sản phẩm Flagship** thực tế từ 5 hãng hàng đầu (Apple, Samsung, Xiaomi, OPPO, Vivo). Mỗi sản phẩm được định nghĩa theo cấu trúc JSON chuẩn mực:

```typescript
interface Product {
  id: string;               // Mã định danh duy nhất (VD: 'p-ip16pm', 'p-s24u')
  name: string;             // Tên thương mại đầy đủ kèm chứng nhận VN/A
  brand: 'Apple' | 'Samsung' | 'Xiaomi' | 'OPPO' | 'Vivo';
  basePrice: number;        // Giá niêm yết của phiên bản tiêu chuẩn (VND)
  originalPrice: number;    // Giá gốc trước khi giảm (VND)
  badge: string;            // 'Hot', 'Mới Ra Mắt', 'Bán Chạy', 'Giảm 7TR'...
  rating: number;           // Điểm đánh giá (4.8 - 5.0)
  reviewsCount: number;     // Số lượng đánh giá thực tế
  isFlashSale: boolean;     // Có tham gia đợt Flash Sale giờ vàng hay không
  has0Percent: boolean;     // Hỗ trợ gói trả góp 0% lãi suất
  image: string;            // URL ảnh sản phẩm sắc nét (Unsplash / CDN chính hãng)
  specs: {
    screen: string;         // Thông số màn hình (kích thước, tấm nền, tần số quét)
    chip: string;           // Vi xử lý (Apple A18 Pro, Snapdragon 8 Gen 3...)
    ram: string;            // Dung lượng RAM (8GB, 12GB, 16GB...)
    cameraRear: string;     // Cụm camera sau chi tiết độ phân giải và ống kính
    cameraFront: string;    // Camera selfie
    battery: string;        // Dung lượng pin và công nghệ sạc nhanh
    weight: string;         // Trọng lượng máy
    os: string;             // Hệ điều hành khởi chạy
  };
  storages: Array<{
    name: string;           // '128GB', '256GB', '512GB', '1TB'
    extra: number;          // Mức tiền cộng thêm so với basePrice
  }>;
  colors: Array<{
    name: string;           // Tên màu chính hãng (Titan Sa Mạc, Xanh Titan, Đen...)
    hex: string;            // Mã màu HEX hiển thị trên nút chọn
    img: string;            // URL ảnh góc chụp tương ứng với màu sắc đó
  }>;
}
```

---

## 6. ĐẶC TẢ LOGIC & 8 KHỐI TÍNH NĂNG DOANH NGHIỆP CỐT LÕI

### 6.1. Ma Trận Biến Thể Đa Chiều (PDP Real-time Matrix)
* **Kích hoạt:** Bấm vào thẻ sản phẩm hoặc nút "Chi Tiết".
* **Logic phản ứng (Reactive Logic):**
  * **Đổi bộ nhớ:** `Tổng giá = product.basePrice + product.storages[selectedStorageIndex].extra`. Cập nhật ngay trên nhãn giá lớn và giá cũ mà không tải lại trang.
  * **Đổi màu sắc:** Cập nhật ngay thuộc tính `src` của ảnh sản phẩm chính sang `product.colors[selectedColorIndex].img`, đồng thời đổi nhãn tên màu hiển thị (`Titan Sa Mạc`, `Titan Tự Nhiên`...).
* **Thông số kỹ thuật:** Hiển thị dạng bảng lưới Responsive 2 cột với đầy đủ 8 thông số chip, camera, pin, sạc.

### 6.2. Bộ Tính Trả Góp 0% Lãi Suất Tự Động (Installment Calculator)
* **Công thức toán học:**
  $$\text{Số tiền trả trước} = \text{Tổng giá máy} \times \text{Tỷ lệ trả trước (20\%, 30\%, 50\%, 70\%)}$$
  $$\text{Số tiền còn nợ} = \text{Tổng giá máy} - \text{Số tiền trả trước}$$
  $$\text{Số tiền góp mỗi tháng} = \frac{\text{Số tiền còn nợ}}{\text{Kỳ hạn (3, 6, 9, 12 tháng)}}$$
* **Tương tác:** Cho phép chuyển đổi dropdown điện thoại, mức trả trước, và kỳ hạn. Mọi con số được làm tròn và định dạng tiền VND có dấu chấm ngăn cách (`10.347.000₫`, `4.023.833₫/tháng`).

### 6.3. Định Giá Thu Cũ Lên Đời Trợ Giá (Trade-in Simulator)
* **Hệ thống định giá tự động:**
  * Giá máy cũ cơ sở theo dòng (iPhone 14 Pro Max: 12TR, S23 Ultra: 11TR...).
  * Hệ số hao mòn ngoại hình: Loại 1 (Đẹp keng): $1.0\times$, Loại 2 (Trầy xước nhẹ): $0.85\times$, Loại 3 (Cấn móp/Pin chai): $0.70\times$.
  * Trợ giá độc quyền Hải Đăng Mobile: **+ 2.000.000₫**.
* **Công thức số tiền bù:**
  $$\text{Tiền thu máy cũ} = \text{Giá cơ sở} \times \text{Hệ số hao mòn}$$
  $$\text{Tổng tiền cấn trừ} = \text{Tiền thu máy cũ} + \text{Trợ giá 2.000.000₫}$$
  $$\text{Số tiền bù thêm} = \max(0, \text{Giá máy mới muốn mua} - \text{Tổng tiền cấn trừ})$$

### 6.4. Ma Trận So Sánh Cấu Hình Đối Đầu (Head-to-Head Comparison)
* **Cơ chế chọn:** Mỗi sản phẩm có nút "⚖ So sánh". Người dùng có thể chọn tối đa **3 điện thoại cùng lúc**.
* **Thanh Bottom Bar Nổi (Floating Compare Pill):** Khi có từ 1 sản phẩm trở lên, thanh ghim nổi dưới chân trang hiển thị ảnh thu nhỏ, số lượng đã chọn (`So sánh cấu hình (2/3)`) và nút "So Sánh Ngay".
* **Bảng so sánh đối đầu:** Khi mở modal, hệ thống dựng bảng so sánh đa cột với 8 hàng chỉ số kỹ thuật chi tiết đặt cạnh nhau (Màn hình, Chip, RAM, Camera trước/sau, Pin/sạc, Cân nặng, OS).

### 6.5. Flash Sale Giờ Vàng & Đồng Hồ Đếm Ngược (Live Countdown Engine)
* **Engine đếm ngược:** Đếm ngược từng giây theo định dạng `Giờ : Phút : Giây` (ví dụ: `04 : 35 : 03`).
* **Hiển thị độ "Cháy hàng":** Thanh tiến độ khuyến mãi động với tỷ lệ bán thực tế (`Đã bán 82/100 suất`).

### 6.6. Bộ Lọc Đa Tiêu Chí & Tìm Kiếm Thông Minh (Search & Filter Engine)
* **Lọc theo thương hiệu:** Tất cả, Apple iPhone, Samsung Galaxy, Xiaomi, OPPO, Vivo.
* **Lọc theo khoảng giá:** Dưới 10 Triệu, 10 – 20 Triệu, Flagship Trên 20 Triệu.
* **Tìm kiếm tức thì (Live Search):** Gõ từ khóa tự động lọc danh sách sản phẩm theo tên máy, thương hiệu và thông số chip mà không có độ trễ.
* **Sắp xếp linh hoạt:** Bán chạy nhất, Giá tăng dần, Giá giảm dần, Giảm giá nhiều nhất.

### 6.7. Giỏ Hàng & Cổng Thanh Toán VietQR Tự Động (VietQR Dynamic Checkout)
* **Tính toán chi phí:** Tạm tính, phí vận chuyển (Miễn phí toàn quốc cho đơn điện thoại), giảm giá voucher.
* **Động cơ Voucher:** Hỗ trợ nhập mã `IPHONE2026` (giảm ngay 500.000₫), mã `FREESHIP`.
* **Biểu mẫu thông tin đặt hàng:** Họ tên, số điện thoại, tỉnh thành phố, địa chỉ chi tiết, phương thức thanh toán.
* **Cổng tạo mã VietQR động:** Khi khách chọn thanh toán Chuyển khoản VietQR:
  * Tự động sinh mã đơn hàng ngẫu nhiên: `HD-ORD-XXXXXX`.
  * Gọi API hình ảnh chuẩn VietQR:
    `https://api.vietqr.io/image/970407-190368889999-5H3aP8q.jpg?accountName=CONG%20TY%20HAI%20DANG%20MOBILE%20VN&amount={grandTotal}&addInfo={orderId}`
  * Khách hàng mở ứng dụng ngân hàng bất kỳ (Vietcombank, Techcombank, MBBank...) quét mã sẽ tự động điền sẵn STK, chủ tài khoản `CONG TY HAI DANG MOBILE VN`, số tiền chuẩn xác đến từng đồng và nội dung chuyển khoản là mã đơn hàng.

### 6.8. Quản Lý Đơn Hàng & Đồng Bộ LocalStorage (Order Management & Persistence)
* **Lưu trữ dữ liệu:** Lưu trữ giỏ hàng (`haidang_cart`) và lịch sử đơn hàng (`haidang_orders`) vào `localStorage` của trình duyệt. Dữ liệu không bị mất khi F5 hoặc tắt trình duyệt.
* **Quản trị đơn hàng:** Người dùng bấm "Tra Cứu Đơn" trên thanh điều hướng để xem danh sách đơn đã đặt:
  * Trạng thái đơn: `ĐÃ TIẾP NHẬN KỸ THUẬT`.
  * Xem danh sách chi tiết các máy, màu sắc, bộ nhớ, giá tiền, địa chỉ giao hàng.
  * Hỗ trợ chức năng **Hủy đơn** và **In Hóa Đơn VAT** trực tiếp từ trình duyệt (`window.print()`).
* **Hệ thống Toast Notification:** Hiển thị thông báo trạng thái góc màn hình mỗi khi thêm giỏ hàng, áp mã ưu đãi, hoặc gửi đơn thành công.

---

## 7. CHÂN TRANG PHÁP LÝ & BỘ NHẬN DIỆN UY TÍN (CORPORATE LEGAL TRUST SEALS)

Chân trang phải mang đầy đủ thông tin pháp nhân doanh nghiệp để tạo sự tin tưởng tuyệt đối:
* **Tên công ty:** Công ty Cổ phần Bán lẻ Kỹ thuật số Hải Đăng (Hai Dang Mobile).
* **Giấy phép kinh doanh:** Giấy chứng nhận ĐKKD số: `0108992834` do Sở KH&ĐT TP. Hà Nội cấp.
* **Trụ sở chính:** Tòa nhà Hai Dang Tower, Cầu Giấy, TP. Hà Nội.
* **Huy hiệu chứng nhận:**
  * Badge xanh: `✓ ĐÃ THÔNG BÁO BỘ CÔNG THƯƠNG`
  * Badge bảo mật: `🔒 SSL 256-BIT SECURE`
* **Cụm tổng đài miễn cước:** Tư vấn `1800.6868`, Kỹ thuật `1800.6869`, Khiếu nại `1800.6870`.
* **Cổng chấp nhận thanh toán:** VietQR, VNPAY, Visa / Master, COD đồng kiểm khi nhận hàng.

---

## 8. TIÊU CHUẨN ĐÓNG GÓI & DEPLOY VERCEL (PRODUCTION ZERO-CONFIG)

Cung cấp tệp `vercel.json` chuẩn cấu trúc bảo mật:
```json
{
  "version": 2,
  "cleanUrls": true,
  "trailingSlash": false,
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        { "key": "X-Content-Type-Options", "value": "nosniff" },
        { "key": "X-Frame-Options", "value": "SAMEORIGIN" },
        { "key": "X-XSS-Protection", "value": "1; mode=block" },
        { "key": "Referrer-Policy", "value": "strict-origin-when-cross-origin" }
      ]
    }
  ]
}
```

---

## 9. NGUYÊN BẢN MASTER PROMPT DÀNH CHO AI (READY-TO-USE PROMPT)

*Dưới đây là nội dung prompt độc lập, bạn có thể copy trực tiếp đoạn bên dưới để yêu cầu AI tạo mới hoặc phát triển tiếp hệ thống:*

```markdown
Bạn là một Principal Frontend Architect kiêm Senior UI/UX Enterprise Designer. Hãy tạo ra một ứng dụng web thương mại điện tử hoàn chỉnh, chuyên nghiệp và đẳng cấp mang tên:
"HAI DANG MOBILE – HỆ THỐNG BÁN LẺ ĐIỆN THOẠI CHÍNH HÃNG, TRẢ GÓP 0% & THU CŨ ĐỔI MỚI".

YÊU CẦU KIẾN TRÚC & CÔNG NGHỆ:
1. Đóng gói trong một tệp index.html duy nhất (HTML5, Modern CSS Variables, Vanilla ES6+ JS). Không dùng framework nặng (No React/Vue/jQuery), không dùng CDN phụ thuộc dễ lỗi. Tối ưu tải trang < 0.8s, sẵn sàng deploy Vercel ngay lập tức.
2. Giao diện MÀU SÁNG DOANH NGHIỆP (Corporate Enterprise Light Theme): Nền Slate 50 (#f8fafc), Thẻ Card trắng (#ffffff), Chữ đen Slate 900 (#0f172a), Viền tinh tế (#e2e8f0), Màu nhấn đỏ doanh nghiệp (#d32f2f) và xanh uy tín (#059669, #1d4ed8).
3. Thanh Top Trust Bar: Hệ thống 120 Showroom toàn quốc, Hotline miễn cước 1800.6868, Cam kết 100% Chính Hãng VN/A, Giao hàng hỏa tốc 1 giờ, Kênh B2B doanh nghiệp.
4. Bốn trụ cột cam kết: 100% VN/A Apple & Samsung, Giao 1h, 1 đổi 1 trong 30 ngày, Trả góp 0% duyệt 5 phút.

CƠ SỞ DỮ LIỆU & 8 CHỨC NĂNG BẮT BUỘC PHẢI HOẠT ĐỘNG 100% BẰNG JAVASCRIPT:
1. Database: Quản lý tối thiểu 20 Flagship (iPhone 16 Pro Max, iPhone 16 Pro, Galaxy S24 Ultra, Z Fold 6, Xiaomi 14 Ultra, Vivo X100 Pro, OPPO Find N3...) với đầy đủ bộ nhớ (storages), màu sắc (colors kèm ảnh thật tương ứng), và bảng cấu hình chi tiết 8 thông số (Màn hình, Chip, RAM, Camera sau, Camera trước, Pin/sạc, Trọng lượng, OS).
2. Product Detail Modal (PDP): Bấm vào máy hiển thị modal chi tiết. Đổi dung lượng tự động cộng tiền và cập nhật giá tức thì; Đổi màu sắc tự động cập nhật ảnh điện thoại tương ứng; Hiển thị bảng cấu hình kỹ thuật dạng lưới responsive.
3. Bộ tính Trả Góp 0%: Chọn máy, chọn mức trả trước (20%, 30%, 50%, 70%) và kỳ hạn (3, 6, 9, 12 tháng) -> Tự động tính chính xác số tiền trả trước và số tiền góp mỗi tháng (định dạng VND chuẩn).
4. Định giá Thu Cũ Đổi Mới: Chọn dòng máy cũ, chọn tình trạng máy (Loại 1, Loại 2, Loại 3), cộng thêm Trợ giá lên đời 2.000.000₫ -> Tự tính toán số tiền chênh lệch cần bù thêm.
5. So sánh đối đầu (Comparison): Chọn tối đa 3 máy bất kỳ, hiển thị thanh Bottom Bar nổi đếm số lượng, mở modal so sánh bảng cấu hình chi tiết 8 tiêu chí đối đầu trực quan.
6. Flash Sale Giờ Vàng: Đồng hồ đếm ngược thời gian thực (hh:mm:ss) và thanh tiến độ suất bán khuyến mãi.
7. Giỏ hàng & Thanh toán VietQR Động: Thêm giỏ hàng, nhập voucher IPHONE2026 (-500.000₫), form điền người nhận, tự động sinh mã đơn HD-ORD-XXXXXX và sinh ảnh VietQR API Techcombank kèm đúng số tiền và mã đơn.
8. Quản lý đơn hàng (Orders) & Lưu trữ LocalStorage: Tra cứu đơn hàng đã đặt, lưu giỏ hàng và đơn hàng bền vững trong localStorage (haidang_cart, haidang_orders), hỗ trợ Hủy đơn và In hóa đơn.

CHÂN TRANG DOANH NGHIỆP:
- Tên pháp nhân: Công ty Cổ phần Bán lẻ Kỹ thuật số Hải Đăng (Hai Dang Mobile).
- ĐKKD số: 0108992834 do Sở KH&ĐT TP. Hà Nội cấp. Trụ sở: Tòa nhà Hai Dang Tower, Cầu Giấy, Hà Nội.
- Huy hiệu: "✓ ĐÃ THÔNG BÁO BỘ CÔNG THƯƠNG" và "🔒 SSL 256-BIT SECURE".
- Tổng đài: 1800.6868, 1800.6869, 1800.6870.

Hãy tạo ra mã nguồn hoàn hảo, kiểm tra không có bất kỳ lỗi cú pháp nào, thiết kế tỉ mỉ, mượt mà trên cả Mobile và Desktop.
```
