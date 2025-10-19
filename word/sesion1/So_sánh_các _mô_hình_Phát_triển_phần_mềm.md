# 📘 [Bài đọc] – So sánh các Mô hình Phát triển Phần mềm

---

## 1. Tiêu chí so sánh cốt lõi

| Tiêu chí | Mô tả |
|-----------|--------|
| Ổn định yêu cầu | Stable Requirements |
| Mức rủi ro & không chắc chắn | Risk / Uncertainty |
| Chi phí thay đổi muộn | Cost of Late Change |
| Mức độ tài liệu | Documentation Intensity |
| Nhịp bàn giao | Delivery Cadence |
| Mức độ tham gia của khách hàng | Customer Involvement |
| Chiến lược kiểm thử | Testing Strategy |
| Khả năng dự báo tiến độ / chi phí | Predictability |
| Tuân thủ & kiểm định | Compliance |
| Khả năng mở rộng quy mô đội / đa dự án | Scalability |

---

## 2. Mô hình Tuyến tính (Linear)

### 2.1. Waterfall

**Ý tưởng:**  
Phát triển tuần tự các pha SDLC:  
Yêu cầu → Thiết kế → Lập trình → Kiểm thử → Triển khai → Bảo trì.  

**Khi dùng:**  
- Yêu cầu ổn định, miền nghiệp vụ quen thuộc  
- Dự án có quy định nghiêm ngặt (y tế, công, quốc phòng)  
- Cần tài liệu chuẩn, dễ audit  

**Ưu điểm:**
- Dễ quản trị theo mốc  
- Tài liệu rõ ràng, dự báo tốt  
- Phù hợp đấu thầu / hợp đồng truyền thống  

**Hạn chế:**
- Phản hồi người dùng đến muộn  
- Chi phí thay đổi tăng mạnh về sau  
- Dễ “chết chìm” nếu yêu cầu ban đầu sai  

---

### 2.2. V-Model (Verification & Validation Model)

**Ý tưởng:**  
Mở rộng Waterfall bằng cách ghép mỗi pha phát triển với một pha kiểm thử tương ứng  
(Yêu cầu ↔ UAT, Thiết kế ↔ System Test, Lập trình ↔ Unit Test, v.v.)

**Khi dùng:**  
- Dự án an toàn/sinh mạng, hoặc tuân thủ cao (medical, automotive)  
- Cần truy vết từ yêu cầu → test case  

**Ưu điểm:**
- Kiểm soát chất lượng mạnh  
- Dễ audit  
- Phù hợp môi trường tuân thủ  

**Hạn chế:**
- Tuyến tính, khó thích nghi khi yêu cầu đổi  
- Tốn công tài liệu & quy trình test  

---

## 3. Mô hình Lặp & Tiến hoá (Iterative / Incremental / RAD)

### 3.1. Iterative (Lặp cải tiến)
**Ý tưởng:** Xây dựng phiên bản thô → lặp lại để cải tiến.  
**Ưu:** Phản hồi sớm, giảm hiểu sai.  
**Nhược:** Dễ trượt phạm vi nếu thiếu kỷ luật.  
**Dùng khi:** Nghiệp vụ chưa rõ, cần khám phá giải pháp.  

---

### 3.2. Incremental (Tăng trưởng theo phần)
**Ý tưởng:** Phát triển theo các “miếng” (increments), mỗi phần hoàn thiện một nhóm tính năng.  
**Ưu:** Ra giá trị sớm, quản lý phạm vi tốt.  
**Nhược:** Cần kiến trúc vững để các phần khớp nhau.  
**Dùng khi:** Cần phát hành dần theo mốc thời gian.  

---

## 4. Spiral (Bánh xe xoắn ốc – Hướng rủi ro)

**Ý tưởng:**  
Chu kỳ xoắn ốc gồm 4 bước:  
1️⃣ Xác định mục tiêu  
2️⃣ Phân tích rủi ro  
3️⃣ Phát triển & kiểm thử  
4️⃣ Lập kế hoạch vòng tiếp theo  

**Ưu điểm:**
- Mạnh về quản trị rủi ro  
- Kết hợp ưu điểm Waterfall + Prototyping + Iterative  

**Hạn chế:**
- Phức tạp, đòi hỏi quản trị rủi ro tốt  
- Tốn công quản lý  

**Dùng khi:**  
Dự án lớn, rủi ro cao, công nghệ/pháp lý mới, nhiều bên liên quan.  
**Ví dụ:** Nền tảng thanh toán quốc tế, yêu cầu bảo mật cao.  

---

## 5. Agile (Scrum, Kanban, XP)

> Agile không phải “mô hình SDLC” cứng, mà là **tập giá trị và nguyên tắc** nhấn mạnh phản hồi nhanh, cộng tác, phần mềm chạy được, và thích ứng thay đổi.

---

### 5.1. Scrum

**Cốt lõi:**
- Làm việc theo **Sprint** (1–4 tuần)  
- 3 vai trò: Product Owner (PO), Scrum Master (SM), Development Team  
- Artefacts: Product Backlog, Sprint Backlog, Increment  
- Sự kiện: Sprint Planning, Daily Scrum, Sprint Review, Retrospective  

**Ưu điểm:**
- Nhịp giao hàng đều  
- Phản hồi sớm  
- Minh bạch tiến độ  
- Giảm rủi ro trễ hạn  

**Hạn chế:**
- Cần PO quyết đoán  
- Đòi hỏi kỷ luật nhóm  
- Dễ “Scrum giả” nếu chỉ hình thức  

**Dùng khi:**  
Yêu cầu biến động, sản phẩm hướng người dùng, cần học nhanh từ thị trường.  

---

### 5.2. Kanban

**Cốt lõi:**  
- Trực quan hóa luồng công việc  
- Giới hạn **WIP (Work In Progress)**  
- Phát hành liên tục, không cần Sprint  

**Ưu điểm:**
- Linh hoạt, phù hợp đội vận hành/bảo trì  
- Tối ưu lead time và throughput  

**Hạn chế:**
- Dễ tràn việc nếu không kiểm soát WIP  
- Dự báo xa khó hơn Scrum  

**Dùng khi:**  
Luồng công việc liên tục, ưu tiên thay đổi thường xuyên, môi trường vận hành/ops.  

---

## 6. Bảng So sánh Tổng hợp

| **Tiêu chí**         | **Waterfall** | **V-Model**   | **Agile (Scrum)**        | **Agile (Kanban)** |
| -------------------- | ------------- | ------------- | ------------------------ | ------------------ |
| Ổn định yêu cầu      | Cao           | Cao           | Thấp – TB                | Thấp – TB          |
| Quản trị rủi ro      | Thấp          | TB            | Cao (qua lặp)            | TB – Cao           |
| Chi phí đổi muộn     | Cao           | Cao           | Thấp – TB                | Thấp – TB          |
| Mức tài liệu         | Cao           | Rất cao       | TB                       | Thấp – TB          |
| Nhịp bàn giao        | Cuối kỳ       | Cuối kỳ       | Mỗi Sprint               | Liên tục           |
| Tham gia khách hàng  | Thấp – TB     | Thấp – TB     | Cao                      | Cao                |
| Chiến lược test      | Cuối pha      | Ghép từng pha | Liên tục                 | Liên tục           |
| Dự báo tiến độ       | Cao           | Cao           | TB (velocity)            | Thấp – TB          |
| Tuân thủ / kiểm định | Cao           | Rất cao       | TB                       | Thấp – TB          |
| Mở rộng quy mô       | Cao           | Cao           | Cao (Scrum@Scale / SAFe) | TB – Cao           |

---

## 7. Cách chọn Mô hình (Decision Guide)

| **Tình huống**                      | **Mô hình phù hợp**                 |
| ----------------------------------- | ----------------------------------- |
| Yêu cầu ổn định, tuân thủ cao       | ✅ V-Model / Waterfall               |
| Rủi ro cao, nhiều bên liên quan     | 🔄 Spiral / Iterative + Prototyping |
| Cần ra giá trị sớm                  | ⚡ Agile (Scrum / Kanban)            |
| Phát hành dần từng phần             | 🧩 Incremental (+Scrum)             |
| UX / phản hồi người dùng quan trọng | 🧠 Thêm Prototyping / RAD           |
| Dự án hiện đại, DevOps              | 🚀 Kết hợp CI/CD + Agile            |



> 💡 **Kết luận:**  
Không có mô hình nào “tốt nhất”, chỉ có mô hình **phù hợp nhất với hoàn cảnh, quy mô và rủi ro dự án**.
