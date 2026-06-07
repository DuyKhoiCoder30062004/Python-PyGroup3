# Ứng dụng Quản lý Ngân hàng trên Desktop

Một hệ thống ngân hàng chạy trên desktop với tính năng nhận diện khuôn mặt bằng AI để đảm bảo giao dịch an toàn.  
Dự án này được phát triển như một bài tập học thuật nhằm thực hành **Phát triển Fullstack** với **Python** và **Tkinter**.

---

## 📌 Thông tin Dự án
- **Quy mô nhóm:** 4  
- **Vai trò:** Fullstack Developer  
- **Thời gian:** Tháng 2/2025 – Tháng 5/2025  
- **Ngôn ngữ/Frameworks:** Python, Tkinter  

---

## 📌 Tổng quan
Hệ thống được thiết kế để quản lý các hoạt động ngân hàng bao gồm tài khoản khách hàng, giao dịch và dịch vụ.  
Nó tích hợp **AI nhận diện khuôn mặt** để tăng cường bảo mật cho các giao dịch có giá trị lớn.

---

## 📌 Tính năng
- <mark>Xác thực</mark> (đăng nhập/đăng ký)  
- <mark>Giao diện chính của ngân hàng</mark> để quản lý tài khoản  
- <mark>Lịch sử giao dịch</mark> theo dõi chi tiết  
- <mark>Chuyển tiền</mark>  
- <mark>Cài đặt</mark> và <mark>Các dịch vụ khác</mark>  
- <mark>AI nhận diện khuôn mặt</mark> cho các giao dịch ≥ 10 triệu VNĐ  

---

## 📌 Thiết kế Hệ thống
- Thiết kế cơ sở dữ liệu bằng <mark>Microsoft SQL Server</mark>  
- Tích hợp <mark>cv2 Camera</mark> và <mark>Haarcascade</mark> để phát hiện khuôn mặt  
- Xây dựng <mark>Pipeline huấn luyện</mark> với tập dữ liệu khuôn mặt thật, giám sát hiện tượng overfitting  
- Triển khai luồng giao dịch an toàn với nhận diện khuôn mặt  

---

## 📌 Pipeline Huấn luyện AI
Dự án tích hợp hệ thống nhận diện khuôn mặt bằng AI để bảo mật các giao dịch giá trị lớn.  
Pipeline huấn luyện được thiết kế để xử lý tập dữ liệu khuôn mặt thật, bao gồm các bước:

### 1. Thu thập dữ liệu:
 + Thu thập tập ảnh khuôn mặt thật.  
 + Phân chia thành tập huấn luyện và tập kiểm thử.  

### 2. Tiền xử lý:
 + Thay đổi kích thước và chuẩn hóa ảnh.  
 + Sử dụng <mark>Haarcascade</mark> để phát hiện khuôn mặt.  
 + Tăng cường dữ liệu để tăng tính đa dạng.  

### 3. Huấn luyện mô hình:
 + Xây dựng mô hình nhận diện bằng <mark>OpenCV (cv2)</mark>.  
 + Huấn luyện với supervised learning trên đặc trưng khuôn mặt.  
 + Giám sát độ chính xác huấn luyện và kiểm thử.  

### 4. Giám sát Overfitting:
 + So sánh hiệu suất huấn luyện và kiểm thử.  
 + Xác định dấu hiệu overfitting (độ chính xác huấn luyện cao nhưng kiểm thử thấp).  
 + Điều chỉnh kích thước tập dữ liệu và bước tiền xử lý để giảm thiểu.  

### 5. Tích hợp:
 + Kết nối mô hình đã huấn luyện với giao diện ngân hàng <mark>Tkinter</mark>.  
 + Nhận diện khuôn mặt được kích hoạt cho giao dịch ≥ 10 triệu VNĐ.  
 + Đảm bảo luồng giao dịch an toàn trước khi phê duyệt.  

---

## 📌 Cách chạy chương trình
1. Clone repository:
   ```bash
   git clone https://github.com/DuyKhoiCoder30062004/Python-PyGroup3.git
2. # Ứng dụng Quản lý Ngân hàng trên Desktop

Một hệ thống ngân hàng chạy trên desktop với tính năng nhận diện khuôn mặt bằng AI để đảm bảo giao dịch an toàn.  
Dự án này được phát triển như một bài tập học thuật nhằm thực hành **Phát triển Fullstack** với **Python** và **Tkinter**.

---

## 📌 Thông tin Dự án
- **Quy mô nhóm:** 4  
- **Vai trò:** Fullstack Developer  
- **Thời gian:** Tháng 2/2025 – Tháng 5/2025  
- **Ngôn ngữ/Frameworks:** Python, Tkinter  

---

## 📌 Tổng quan
Hệ thống được thiết kế để quản lý các hoạt động ngân hàng bao gồm tài khoản khách hàng, giao dịch và dịch vụ.  
Nó tích hợp **AI nhận diện khuôn mặt** để tăng cường bảo mật cho các giao dịch có giá trị lớn.

---

## 📌 Tính năng
- <mark>Xác thực</mark> (đăng nhập/đăng ký)  
- <mark>Giao diện chính của ngân hàng</mark> để quản lý tài khoản  
- <mark>Lịch sử giao dịch</mark> theo dõi chi tiết  
- <mark>Chuyển tiền</mark>  
- <mark>Cài đặt</mark> và <mark>Các dịch vụ khác</mark>  
- <mark>AI nhận diện khuôn mặt</mark> cho các giao dịch ≥ 10 triệu VNĐ  

---

## 📌 Thiết kế Hệ thống
- Thiết kế cơ sở dữ liệu bằng <mark>Microsoft SQL Server</mark>  
- Tích hợp <mark>cv2 Camera</mark> và <mark>Haarcascade</mark> để phát hiện khuôn mặt  
- Xây dựng <mark>Pipeline huấn luyện</mark> với tập dữ liệu khuôn mặt thật, giám sát hiện tượng overfitting  
- Triển khai luồng giao dịch an toàn với nhận diện khuôn mặt  

---

## 📌 Pipeline Huấn luyện AI
Dự án tích hợp hệ thống nhận diện khuôn mặt bằng AI để bảo mật các giao dịch giá trị lớn.  
Pipeline huấn luyện được thiết kế để xử lý tập dữ liệu khuôn mặt thật, bao gồm các bước:

### 1. Thu thập dữ liệu:
 + Thu thập tập ảnh khuôn mặt thật.  
 + Phân chia thành tập huấn luyện và tập kiểm thử.  

### 2. Tiền xử lý:
 + Thay đổi kích thước và chuẩn hóa ảnh.  
 + Sử dụng <mark>Haarcascade</mark> để phát hiện khuôn mặt.  
 + Tăng cường dữ liệu để tăng tính đa dạng.  

### 3. Huấn luyện mô hình:
 + Xây dựng mô hình nhận diện bằng <mark>OpenCV (cv2)</mark>.  
 + Huấn luyện với supervised learning trên đặc trưng khuôn mặt.  
 + Giám sát độ chính xác huấn luyện và kiểm thử.  

### 4. Giám sát Overfitting:
 + So sánh hiệu suất huấn luyện và kiểm thử.  
 + Xác định dấu hiệu overfitting (độ chính xác huấn luyện cao nhưng kiểm thử thấp).  
 + Điều chỉnh kích thước tập dữ liệu và bước tiền xử lý để giảm thiểu.  

### 5. Tích hợp:
 + Kết nối mô hình đã huấn luyện với giao diện ngân hàng <mark>Tkinter</mark>.  
 + Nhận diện khuôn mặt được kích hoạt cho giao dịch ≥ 10 triệu VNĐ.  
 + Đảm bảo luồng giao dịch an toàn trước khi phê duyệt.  

---

## 📌 Cách chạy chương trình
1. Clone repository:
   ```bash
   git clone https://github.com/DuyKhoiCoder30062004/Python-PyGroup3.git
2. Cài đặt các thư viện cần thiết:
pip install opencv-python
pip install pyodbc
3. Cấu hình chuỗi kết nối SQL Server.
sử dụng thư viện pyodbc  
4. Chạy ứng dụng:
python UI_Bank.py

## 📌 Ảnh chụp màn hình
<div align="center">
<img src="./docs/banking-app.png" width="70%" />
</div>

## 📌 Đóng góp
Dự án được phát triển bởi nhóm 4 sinh viên trong khuôn khổ môn học.

## 📌 Giấy phép
Dự án này chỉ phục vụ mục đích học tập.
