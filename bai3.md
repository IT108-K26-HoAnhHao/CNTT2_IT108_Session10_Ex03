

## Phần 1. Phân tích bài toán: Cơ chế Token và hiệu suất xử lý của AI

**Token là gì?**

Token là đơn vị văn bản cơ bản mà các Mô hình Ngôn ngữ lớn sử dụng để đọc và hiểu ngữ cảnh. Một Token có thể là 1 từ, một phần của từ (âm tiết), hoặc thậm chí là 1 ký tự đặt biệt (khoảng trắng, dấu câu).

* **Tạo sao Mark down giúp AI xử lý nhanh hơn HTML?**
* **Ít ký tựu rườm rà hơn:** HTML chứa rất nhiều thẻ mở và đóng dài dòng (như `<div>`, `span>`, `<table>`, `<tr>`, `<td>`,...) cùng các thuộc tính dư thừa. Trong khi đó, Markdown sử dụng các ký tự đại diện cực kỳ tối giản (như `#`, `*`,`-`,`>`).
* **Tiết kiệm Token đáng kể:** Do chứa lượng ký tự ít hơn nhiều, lượng token tiêuu tốn cho cùng một nội dung văn bản sẽ giảm đi từ $70%$ đến $75%$.
* **Tăng tốc độ xử lý & Giảm độ trễ:** AI xử lý dữ liệu dựa trên số lượng token đầu vào (Input Tokens). Ít token hơn đồng nghĩa với việc thời gian mô hình phân tích ngữ cảnh (tăng tốc độ phản hồi lên tới khoảng $88\%$), giúp chatbot nông nghiệp đưa ra câu trả lời cho người nông dân gần như tức thì.

---

## Phần 2. So sánh & Đánh giá Markdown và HTML
### 1. Bảng so sánh chi tiết

| Tiêu chí so sánh | Định dạng HTML | Định dạng Markdowm |
| :--- | :--- | :--- |
|**Cú pháp định dạng** | Phức tạp, nhiều thẻ tag lồng nhau (`<b>`, `<h1>`, `<ul><li>`...) | Đơn giản, trực quan (`**`, `h`, `-`...) |
|**Số lượng Token (Ước tính)** | **Cao** (~2,350 tokens cho nội dung mẫu) | **Thấp** (~620 tokens cho nội dung mẫu) |
|**Độ dễ đọc (Human-reddable)** | Thấp đối với người dùng phổ thông do vướng các thẻ lệnh. | **Rất cao**, văn bản sạch sẽ, gần gũi như văn bản thuần túy. |
|**Thời gian phản hồi (Xử lý)** | Chậm (~8.2 giây) do lượng token lớn. | **Nhanh** (~1.6 giây) nhờ tối ưu hóa token. |
|**Chi phí vận hành API** | Cao (~$0.0235 / lần gọi)  | **Thấp** (~$0.0062 / lần gọi, tiết kiệm ~74%) |


### 2. Giải pháp tối ưu cho hệ thống "GreenTeh" và Lý luận

Dựa trên kết quả phân tích và đặc thù của hệ thống **"Chuyên gia nông nghiệp  AI"** phục vụ người nông dân, giải pháp tối ưu được chọn là **SỬ DỤNG NGÔN NGỮ MARKDOWN**.

#### Lý do thuyết phục:
1. **Bài toán kinh tế và chi phí:** Chatbot phục vụ quy mô lớn cho bà con nông dân sẽ có hàng triệu lượt truy vấn mỗi ngày. Việc tiết kiệm $74\%$ chi phí token bằng Markdown sẽ giúp hạ giá thành vận hành hệ thống xuống mực thấp nhất, đảm bảo tính bền vững cho dự án "GreenTech".
2. **Tốc độ phản hồi ưu việt:** Người nông dân trên đồng ruộng cần câu trả lời nhanh chóng, kịp thời ( ví dụ: *"Cách xử lý sâu bệnh khẩn cấp"*). Thời gian phản hồi giảm từ $8.2$ giây xuống còn $1.6$ giây tạo ra trải nghiệm người dùng mượt mà và hiệu quả hơn hẳn.
3. **Tính bảo trì và quản lý tài nguyên:** Các prompt hoặc dữ liệu kiến thức cơ sở (Knowledge Base) viết bằng Markdown giúp các kỹ sư và chuyên gia nông nghiệp dễ dàng cập nhật nội dung, kiểm tra lỗi, chỉnh sửa tài liệu kỹ thuật nhanh chóng mà không bị rối mắt bởi các cầu trúc rườm rà của HTML.
