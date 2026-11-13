# BÁO CÁO SO SÁNH TRADE-OFF PROMPT (BẢN RÚT GỌN)
## Bước 1: Đề xuất 2 Prompt mẫu
- Giải pháp 1 (Đơn giản):

"Hãy đọc đoạn phản hồi khách hàng và trích xuất thông tin thành Json và Markdown Table gồm các trường: customer_name, product_name, rating, sentiment, key_issue. Dữ liệu: 'Mình tên Lan, mua máy xay sinh tố dùng rất tốt, 4 sao.'"

- Giải pháp 2 (Chi tiết - Khung CREATE & Chặn lỗi):

[CONTEXT] Chuyên gia tự động hóa dữ liệu.

[REQUEST] Trích xuất thông tin từ [EXTRAS] thành JSON và Markdown Table (customer_name, product_name, rating, sentiment, key_issue).

[EXPLANATION] Cho ví dụ mẫu hợp lệ và ví dụ dữ liệu rỗng trả về lỗi status: "error".

[ACTION] Bắt buộc tuân thủ định dạng, không tự bịa dữ liệu (Hallucination) nếu dữ liệu trống.

[EXTRAS] "Mình tên Lan, mua máy xay sinh tố dùng rất tốt, 4 sao."

## Bước 2:
|Tiêu chí |Giải pháp (đơn giản)|Giải pháp 2(chi tiết)|
|---|---|---|
|
