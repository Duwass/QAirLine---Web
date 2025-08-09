
-----

# QAirLine - Ứng dụng Web Đặt vé Máy bay

*Cập nhật lần cuối: 22-12-2024*

Chào mừng bạn đến với QAirLine, một dự án ứng dụng web đặt vé máy bay toàn diện. Hệ thống cho phép người dùng tìm kiếm, đặt và quản lý các chuyến bay, trong khi quản trị viên có thể quản lý toàn bộ hoạt động của hãng bay, từ máy bay, chuyến bay đến khách hàng và các chương trình ưu đãi.

## Mục lục

  - Tính năng chính
  - Công nghệ sử dụng
  - Hướng dẫn cài đặt và khởi chạy
  - Cấu trúc dự án
## Tính năng chính

Dự án được chia thành hai phân hệ chính với các chức năng riêng biệt cho khách hàng và quản trị viên.

### Dành cho Khách hàng

  - **Tìm kiếm chuyến bay:** Tìm kiếm các chuyến bay linh hoạt theo điểm đi, điểm đến và ngày bay.
  - **Đặt vé trực tuyến:** Quy trình đặt vé và thanh toán nhanh chóng, tiện lợi.
  - **Quản lý đặt chỗ:** Xem lại lịch sử các chuyến bay đã đặt và quản lý thông tin đặt vé.
  - **Xem ưu đãi:** Cập nhật các chương trình khuyến mãi và tin tức mới nhất từ hãng bay.
  - **Xác thực người dùng:** Đăng ký và đăng nhập an toàn để quản lý thông tin cá nhân và các chuyến bay.

### Dành cho Quản trị viên

  - **Quản lý chuyến bay:** Dễ dàng thêm, sửa, xóa thông tin chi tiết về các chuyến bay.
  - **Quản lý máy bay:** Quản lý danh sách các loại máy bay, bao gồm thông số kỹ thuật và số ghế.
  - **Quản lý khách hàng:** Xem thông tin và lịch sử đặt vé của tất cả khách hàng.
  - **Tạo ưu đãi:** Tạo và gửi các chương trình khuyến mãi, ưu đãi đến cho khách hàng qua email.
  - **Thống kê và báo cáo:** Xem thống kê tổng quan về số lượng vé đã đặt.

## Công nghệ sử dụng

Dự án được xây dựng với kiến trúc frontend và backend riêng biệt, đảm bảo khả năng mở rộng và bảo trì.

  - **Backend:**
      - **Ngôn ngữ:** TypeScript
      - **Framework:** Node.js, Express.js
      - **Cơ sở dữ liệu:** MySQL
      - **Xác thực:** JSON Web Tokens (JWT)
  - **Frontend:**
      - **Framework:** Next.js, React
      - **Ngôn ngữ:** TypeScript
      - **Styling:** CSS Modules, PostCSS
  - **Triển khai:**
      - **Containerization:** Docker, Docker Compose

## Hướng dẫn cài đặt và khởi chạy

Để khởi chạy dự án trên máy tính cá nhân, bạn cần cài đặt **Docker** và **Docker Compose**.

1.  **Clone kho lưu trữ:**

    ```bash
    git clone https://github.com/your-username/QAirLine-Web-Development.git
    cd QAirLine-Web-Development
    ```

2.  **Cấu hình môi trường cho Backend:**

      - Di chuyển vào thư mục `backend`.
      - Tạo một file `.env` bằng cách sao chép từ file `backend/.env`.
      - Cập nhật các thông tin cần thiết trong file `.env` như thông tin kết nối cơ sở dữ liệu và tài khoản email để gửi thông báo.
        ```env
        PORT=3001
        MYSQL_HOST=your_database_host
        MYSQL_USER=your_database_user
        MYSQL_PASSWORD=your_database_password
        MYSQL_DATABASE=Flight
        EMAIL_USER=your_email@gmail.com
        EMAIL_PASS=your_email_password
        ```

3.  **Khởi chạy dự án bằng Docker Compose:**

      - Quay trở lại thư mục gốc của dự án.
      - Chạy lệnh sau để build và khởi động các container:
        ```bash
        docker-compose up -d
        ```

4.  **Truy cập ứng dụng:**

      - **Trang web khách hàng:** Mở trình duyệt và truy cập `http://localhost:3000`.
      - **API Backend:** Máy chủ backend sẽ chạy tại `http://localhost:3001`.

## Cấu trúc dự án

```
.
├── backend/         # Mã nguồn cho máy chủ backend
├── frontend/        # Mã nguồn cho giao diện người dùng
├── docker-compose.yml # File cấu hình Docker Compose
└── README.md        # File hướng dẫn này
```
