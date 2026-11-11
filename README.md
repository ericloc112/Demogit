# 🛍️ E-Commerce Application (Ứng dụng Thương mại Điện tử)

> Hệ thống website/ứng dụng thương mại điện tử hiện đại, hỗ trợ trải nghiệm mua sắm mượt mà, quản lý đơn hàng thông minh và tích hợp thanh toán trực tuyến.

---

## 📌 Tính năng nổi bật

* **Quản lý sản phẩm**: Tìm kiếm, lọc theo danh mục, sắp xếp giá và xem chi tiết sản phẩm.
* **Giỏ hàng & Thanh toán**: Thêm/sửa/xóa sản phẩm trong giỏ hàng, áp dụng mã giảm giá và tính toán tổng tiền tự động.
* **Tích hợp thanh toán**: Hỗ trợ nhiều phương thức như COD, VNPay, Momo hoặc PayPal.
* **Xác thực người dùng**: Đăng ký, đăng nhập (JWT), phân quyền Người mua (Customer) và Quản trị viên (Admin).
* **Bảng điều khiển Admin (Dashboard)**: Quản lý kho hàng, theo dõi doanh thu, duyệt đơn hàng và thống kê biểu đồ.
* **Thông báo**: Gửi email xác nhận đơn hàng thành công tự động cho khách hàng.

## 🛠️ Công nghệ sử dụng

* **Frontend**: React.js / Next.js, Tailwind CSS, Redux Toolkit
* **Backend**: Node.js, Express.js (hoặc Java Spring Boot / NestJS)
* **Database**: MongoDB / PostgreSQL / MySQL
* **Dịch vụ bên thứ ba**: Cloudinary (lưu ảnh sản phẩm), Nodemailer (gửi mail), VNPay API (thanh toán)

## 🚀 Hướng dẫn cài đặt

Thực hiện các bước sau để thiết lập môi trường chạy thử dưới local:

### Yêu cầu hệ thống
* Node.js (v18+)
* MongoDB hoặc hệ quản trị CSDL tương ứng đã khởi chạy

### Các bước cài đặt

1. **Clone repository:**
   ```bash
   git clone https://github.com
   cd ecommerce-app
   ```

2. **Cài đặt dependencies:**
   ```bash
   # Cài đặt cho Backend
   cd backend && npm install

   # Cài đặt cho Frontend
   cd ../frontend && npm install
   ```

3. **Cấu hình môi trường (`.env`):**
   Tạo file `.env` trong thư mục `backend` và điền cấu hình:
   ```env
   PORT=5000
   MONGO_URI=mongodb://localhost:27017/ecommerce
   JWT_SECRET=your_super_secret_key
   VNPAY_TMN_CODE=your_vnpay_code
   VNPAY_HASH_SECRET=your_vnpay_secret
   ```

4. **Khởi chạy ứng dụng:**
   ```bash
   # Chạy Backend (tại thư mục backend)
   npm run dev

   # Chạy Frontend (tại thư mục frontend)
   npm start
   ```

## 📐 Kiến trúc cơ sở dữ liệu (Database Schema)

Hệ thống quản lý các thực thể chính bao gồm:
* `User`: Lưu thông tin khách hàng, admin, địa chỉ giao hàng.
* `Product`: Tên, mô tả, giá, số lượng tồn kho, hình ảnh, danh mục.
* `Order`: Thông tin sản phẩm đã mua, tổng tiền, trạng thái đơn hàng (Chờ xử lý, Đang giao, Đã giao), trạng thái thanh toán.
* `Cart`: Lưu trữ tạm thời trạng thái giỏ hàng của người dùng.

## 🤝 Đóng góp (Contributing)

1. Fork dự án.
2. Tạo nhánh tính năng (`git checkout -b feature/AmazingFeature`).
3. Commit các thay đổi (`git commit -m 'Add some AmazingFeature'`).
4. Push lên nhánh (`git push origin feature/AmazingFeature`).
5. Mở một **Pull Request**.

## 📄 Giấy phép (License)

Dự án này được cấp phép theo các điều khoản của **MIT License**.
