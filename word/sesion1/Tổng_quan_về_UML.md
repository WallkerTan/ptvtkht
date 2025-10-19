# [Bài đọc] - Tổng quan về UML và Vai trò của Quá trình Mô hình hoá

## 1. Giới thiệu về UML

**UML (Unified Modeling Language)** là ngôn ngữ mô hình hoá chuẩn dùng để **biểu diễn, hình dung, xây dựng và tài liệu hoá** các thành phần của hệ thống phần mềm.  
UML không quy định quy trình phát triển, mà cung cấp **bộ ký pháp (notation)** để mô tả hệ thống ở nhiều góc nhìn: **cấu trúc**, **hành vi**, và **tương tác**.

> Tư duy cốt lõi: Mô hình (model) là *bản đồ — không phải lãnh thổ.*  
> Nó giúp giao tiếp, phân tích, thiết kế và kiểm chứng trước khi “đóng băng” quyết định đắt đỏ trong code hoặc hạ tầng.

### Mô hình hoá (Modeling) là gì?

Là quá trình **trừu tượng hoá (abstraction)** — tập trung vào khía cạnh quan trọng, bỏ qua chi tiết chưa cần thiết.

### Lợi ích chính của mô hình hoá

- Giao tiếp chung giữa BA/PO, dev, tester, kiến trúc sư, khách hàng.  
- Giảm rủi ro hiểu sai yêu cầu, phát hiện xung đột sớm.  
- Ra quyết định kiến trúc: biên giới *bounded context*, dịch vụ, module, dữ liệu.  
- Tái sử dụng & bảo trì: tài liệu sống, hỗ trợ onboarding thành viên mới.  
- Truy vết (*traceability*): từ yêu cầu → use case → lớp/microservice → kiểm thử.

---

## 2. Khung Tổng quan UML

UML bao trùm hai nhóm lớn: **Cấu trúc (Structural)** và **Hành vi (Behavioral)**.  
Trong hành vi có nhánh nhỏ là **Tương tác (Interaction)**.

### 2.1. Nhóm Cấu trúc (Structural Diagrams)

- **Class Diagram** – Lớp, thuộc tính, phương thức, quan hệ (kế thừa, kết hợp, …)  
- **Object Diagram** – Ảnh chụp trạng thái đối tượng tại một thời điểm  
- **Component Diagram** – Thành phần phần mềm (module, service) và phụ thuộc  
- **Deployment Diagram** – Triển khai phần mềm lên nút vật lý hoặc logic (server, container)  
- **Package Diagram** – Nhóm gói, phụ thuộc giữa các gói  
- **Composite Structure Diagram** – Cấu trúc nội tại của lớp hoặc thành phần

### 2.2. Nhóm Hành vi (Behavioral Diagrams)

- **Use Case Diagram** – Tương tác *actor ↔ hệ thống* ở mức yêu cầu  
- **Activity Diagram** – Luồng hoạt động/quy trình (workflow), nhánh rẽ, song song  
- **State Machine Diagram** – Trạng thái và chuyển trạng thái của một thực thể

### 2.3. Nhánh Tương tác (Interaction Diagrams)

- **Sequence Diagram** – Trình tự thông điệp theo thời gian giữa các đối tượng  
- **Communication Diagram** – Tập trung vào cấu trúc liên kết và message  
- **Timing Diagram** – Biểu đồ thời gian/tín hiệu (thường dùng trong hệ nhúng, realtime)  
- **Interaction Overview** – Tổng quan tương tác (kết hợp activity + interactions)

---

## 3. Chọn Sơ đồ nào cho Giai đoạn nào (Map UML ↔ SDLC)

| Giai đoạn SDLC         | Mục tiêu                 | UML phù hợp                                                           | Ghi chú                                                               |
|------------------------|--------------------------|---------------------------------------------------------------------  |-----------------------------------------------------------------------|
| Khảo sát yêu cầu       | Hiểu ai cần gì           | Use Case, Activity (AS-IS / TO-BE)                                    | Nói ngôn ngữ nghiệp vụ, tránh chìm vào kỹ thuật sớm                   |
| Phân tích              | Mô hình hoá domain       | Class (miền), State (thực thể có vòng đời), Sequence (kịch bản chính) | Bắt đầu ở mức conceptual                                              |
| Thiết kế               | Kiến trúc & cấu trúc     | Component, Package, Class (thiết kế), Sequence (giao thức)            | Xác định ranh giới service, API                                       |
| Kiểm thử               | Bảo đảm độ phủ           | Dò Use Case ↔ Test Case, Activity cho flow test                       | Truy vết yêu cầu → test                                               |
| Triển khai             | Hạ tầng                  | Deployment, Component                                                 | Biểu diễn container, node, network                                    |
