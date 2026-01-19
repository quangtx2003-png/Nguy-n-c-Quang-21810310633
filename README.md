# Hệ Thống CRM Bán Hàng (CRM Sales System)

## Giới thiệu
Đây là hệ thống sàn thương mại điện tử bán hàng mô hình EAV được xây dựng với mục tiêu quản lý sản phẩm, đơn hàng và khách hàng hiệu quả.

### Các công nghệ sử dụng

**Backend:**
*   Java 21
*   Spring Boot 3.2
*   JOOQ (Java Object Oriented Querying)
*   MySQL (Database)
*   MinIO (Object Storage)
*   JWT (Authentication)
*   Gradle

**Frontend:**
*   Node.js
*   React 19
*   Tanstack router
*   Tanstack query
*   Zustand
*   Shadcn/ui
*   TailwindCSS

**Infrastructure:**
*   Docker & Docker Compose

## Hướng dẫn cài đặt

### Yêu cầu môi trường
Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt các công cụ sau:
*   **Java JDK 21**
*   **Node.js** (Phiên bản LTS mới nhất)
*   **Docker**

### Cài đặt và chạy ứng dụng

#### 1. Cài đặt Docker, MinIO, MySQL và Cơ sở dữ liệu cho hệ thống
ở thư mục chính chứa docker-compose.yml và chạy lệnh:

```bash
docker compose up -d
```

Đợi cho các container chạy thành công, sau đó truy cập vào MySQL và tạo database cho hệ thống.

#### 2. Backend
ở ngoài thư mục chính:

```bash
# Build project và generate JOOQ code
.\gradlew generateJooq

# Chạy ứng dụng Spring Boot
.\gradlew bootRun
```

#### 3. Frontend
chạy lệnh để vào thư mục frontend:

```bash
cd app/client
```

```bash
# Cài đặt các thư viện dependencies
npm install

# Chạy server development
npm run dev
```

Sau khi chạy thành công, truy cập ứng dụng tại địa chỉ được hiển thị trên terminal (thường là `http://localhost:5173`).

Để test đầy đủ chức năng, khi đăng ký một tài khoản người dùng mới, để tạo tài khoản admin đầu tiên hãy vào bảng cơ sở dữ liệu để phân lại role admin cho tài khoản đó. Lần sau có thể dùng tài khoản admin đó để phân lại role cho tài khoản khác.

## 5 hình ảnh demo

 1. Dashboard tổng quan
<img width="1919" height="944" alt="Dashboard tổng quan" src="https://github.com/user-attachments/assets/5c386b6c-a929-4bbd-9d62-8b07394a66f5" />

2. Quản lý người dùng
<img width="1918" height="942" alt="Quản lý người dùng" src="https://github.com/user-attachments/assets/e8cc4a25-45f5-457f-b05a-f6b5057fc54a" />

3. Quy trình sản phẩm
<img width="1919" height="945" alt="Quản lý sản phẩm" src="https://github.com/user-attachments/assets/179dc12f-20e6-4abc-9f84-bd61a70904a9" />

4. Quản lý danh mục
<img width="1919" height="950" alt="Quản lý danh mục" src="https://github.com/user-attachments/assets/c19334ff-c451-428f-b45f-8167faf95bd6" />

5. Quản lý đơn hàng
<img width="1915" height="944" alt="Quản lý đơn hàng" src="https://github.com/user-attachments/assets/beeebf7a-dd54-49a4-9e40-2e749193a12f" />



