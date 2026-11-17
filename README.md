# BÁO CÁO SO SÁNH TRADE-OFF PROMPT (BẢN RÚT GỌN)
## Bước 1: Đề xuất 2 Prompt mẫu
- Giải pháp 1 (Đơn giản):

"Hãy liệt kê 3 loại CPU,RAM,GPU dưới dạng bảng Markdow.'"

- Giải pháp 2 (Chi tiết - Khung CREATE & Chặn lỗi):

[CONTEXT] Chuyên gia tự linh kiện máy tính.

[REQUEST] Hãy liệt kê danh sách 3 linh kiện PC chơi game (CPU, GPU, RAM) tốt nhất trong tầm giá phổ thông.

[Explanation] Cần cung cấp thông tin chính xác, minh bạch để người dùng dễ dàng nắm bắt hiệu năng và giá thành

[Action] Trình bày toàn bộ kết quả bắt buộc dưới dạng bảng Markdown (Table).

[Tone] chuyên nghiệp, rõ ràng, ngắn gọn.

[Extras] 
- Ràng buộc bắt buộc: Không thêm bất kỳ lời dẫn rườm rà nào trước hoặc sau bảng

- [Few-shot Example]:
Ví dụ định dạng đầu ra mong muốn:

| STT | Tên Linh Kiện | Model Đề Xuất | Giá Ước Tính |
|---|---|---|---|
| 1 | CPU | AMD Ryzen 5 5600X | 3.500.000 VNĐ |

## Bước 2:

|Tiêu chí |Giải pháp (đơn giản)|Giải pháp 2(chi tiết)|
|---|---|---|
|Độ dễ hiểu|Cao|trung bình|
|Tốn token|Ít|Nhiều hơn|
|Chặn lỗi biên|Trung bình|Cực tốt|

## Bước 3: Lựa chọn và Chạy thử
1. Phương án lựa chọn tối ưu nhất:Giải pháp 2 (Chi tiết)
2. Lý do chọn:dù tốn nhiều token hơn .Giải pháp 2 ứng dụng đầy đủ khung CREATE giúp AI hiểu rõ vai trò và mục tiêu, kết hợp kỹ thuật Few-shot và các ràng buộc cứng (Constraints) giúp loại bỏ hoàn toàn các văn bản thừa

Kết quả:

|STT|	Tên Linh Kiện	Model| Đề Xuất	Giá Ước Tính|
|:---:|:---:|:---:|
| 1 |	CPU	AMD Ryzen 5 5600 (6 nhân 12 luồng, AM4) |	1.950.000 – 2.500.000 VNĐ|
| 2 |	GPU (Card đồ họa)	AMD Radeon RX 6600 8GB GDDR6 |	4.300.000 – 5.000.000 VNĐ|
| 3 |	RAM	Kingston Fury Beast 16GB (2x8GB) DDR4 3200MHz |	1.000.000 – 1.300.000 VNĐ|
