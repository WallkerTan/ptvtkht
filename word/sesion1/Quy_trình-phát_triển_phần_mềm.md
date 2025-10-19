# 🧩 Bài đọc – Quy trình Phát triển Phần mềm

## 1. Khái niệm SDLC

> “Làm thế nào để xây dựng một hệ thống thông tin hoặc phần mềm hoàn chỉnh, hiệu quả và đáp ứng đúng nhu cầu người dùng?”

**SDLC (Software Development Life Cycle)** – *Vòng đời phát triển phần mềm* – là quy trình có tổ chức gồm nhiều giai đoạn nhằm đảm bảo phần mềm được:
- Phát triển có kế hoạch
- Kiểm soát chất lượng
- Tối ưu chi phí

### 🎯 Mục tiêu của SDLC
- Đảm bảo phần mềm đáp ứng yêu cầu người dùng  
- Giảm thiểu rủi ro, lỗi và chi phí phát triển  
- Quản lý tiến độ, chất lượng và tài nguyên  

➡️ Nói cách khác, **SDLC là “bản đồ lộ trình”** giúp đội ngũ phát triển đi từ *ý tưởng → sản phẩm hoàn chỉnh.*

---

## 2. Các giai đoạn trong SDLC
Planning
### 2.1. Giai đoạn 1 – Khảo sát và phân tích yêu cầu
**Mục đích:** Xác định mục tiêu, phạm vi, yêu cầu, ràng buộc.  
**Hoạt động chính:**
- Phỏng vấn, khảo sát người dùng  
- Xác định yêu cầu chức năng & phi chức năng  (Analysis)
- Phân tích khả thi (kỹ thuật, chi phí, thời gian)  
- Tạo tài liệu **SRS (Software Requirement Specification)**  

**Ví dụ:**  
Phòng đào tạo làm việc với nhóm phát triển để xác định các yêu cầu “Đăng ký học phần”, “Tra cứu điểm”, “Phân quyền giảng viên”...

---



Design
### 2.2. Giai đoạn 2 – Thiết kế hệ thống
**Mục đích:** Biến yêu cầu thành bản thiết kế kỹ thuật.  
**Hoạt động chính:**
- Thiết kế kiến trúc hệ thống  
- Thiết kế CSDL  
- Thiết kế giao diện (UI/UX)  
- Vẽ sơ đồ UML: Use Case, Class, Sequence, Activity  

**Ví dụ:**  
Use Case thể hiện các tác nhân: *Sinh viên, Giảng viên, Quản trị viên* và các chức năng tương ứng.

---


Implementation
### 2.3. Giai đoạn 3 – Lập trình và phát triển
**Mục đích:** Chuyển bản thiết kế thành mã nguồn.  
**Hoạt động:**
- Phân chia module, giao việc  
- Viết code theo chuẩn  
- Tích hợp hệ thống  

**Ví dụ công nghệ:**
- Backend: Node.js + NestJS  
- Frontend: React / Next.js  
- Database: PostgreSQL  

---


Testing
### 2.4. Giai đoạn 4 – Kiểm thử phần mềm
**Mục đích:** Đảm bảo phần mềm đúng yêu cầu, không lỗi.  

**Các loại kiểm thử:**
- Unit Test  
- Integration Test  
- System Test  
- User Acceptance Test (UAT)  

**Ví dụ:**  
Giảng viên thử nhập điểm, sinh viên tra cứu điểm → phát hiện lỗi trước khi triển khai chính thức.

---
Deployment & Maintenance
### 2.5. Giai đoạn 5 – Triển khai và đưa vào vận hành
**Mục đích:** Đưa phần mềm ra môi trường thực tế.  
**Hoạt động:**
- Cấu hình máy chủ, cơ sở dữ liệu  
- Cài đặt, đào tạo người dùng  
- Giám sát và thu phản hồi  

**Ví dụ:**  
Trường học cài LMS trên domain riêng, cung cấp tài khoản cho sinh viên.

---

### 2.6. Giai đoạn 6 – Bảo trì và nâng cấp
**Mục đích:** Duy trì và nâng cấp hệ thống.  
**Hoạt động:**
- Sửa lỗi  
- Cập nhật công nghệ  
- Thêm tính năng mới  

**Ví dụ:**  
Thêm chức năng đăng nhập bằng Google sau 1 năm vận hành.

---

## 3. Mối quan hệ giữa các giai đoạn
- Các bước liên kết chặt chẽ và mang tính lặp lại.  
- Kết quả đầu ra của giai đoạn trước là đầu vào của giai đoạn sau.  
- Trong **Agile**, có thể quay lại bước trước để điều chỉnh.

---

## 4. Tầm quan trọng của SDLC
- 🧠 Đảm bảo chất lượng phần mềm  
- 💰 Tối ưu chi phí & thời gian  
- 📊 Tăng tính minh bạch, dễ quản lý dự án  
- 👥 Hỗ trợ làm việc nhóm giữa dev – tester – khách hàng – quản lý  

---

> ✅ **Tóm lại:** SDLC là khung xương sống của mọi dự án phần mềm, giúp đảm bảo tiến độ, chất lượng và hiệu quả lâu dài.
