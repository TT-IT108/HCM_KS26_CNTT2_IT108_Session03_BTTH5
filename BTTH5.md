**Bài 5 : Phân tích tốc độ truyền dữ liệu và quản lý đường dẫn tệp an toàn**

### ***Phần 1 (Phân tích & So sánh):***

Lập bảng so sánh đường dẫn tuyệt đối và tương đối. Tính toán chính xác thời gian tải file **2GB** với gói mạng **80 Mbps** (đơn vị giây).

| Tiêu chí | Đường dẫn tuyệt đối | Đường dẫn tương đối |
| :---- | :---- | :---- |
| Bản chất | Chỉ cố định tại (C:\\...) | Chỉ định vị trí dựa trên thư mục hiện hành (`./` hoặc `../`).  |
| Độ linh hoạt | Rất kém, chỉ chạy được trên máy người dùng | Tốt, có thể chạy trên máy khác khi chia sẻ |
| Trạng thái bài toán | C:\\Users\\Ban\_Than\\... $\rightarrow$ Bị đứt gãy trên máy bạn.  | Giữ nguyên cấu trúc thư mục project  |

80Mbps là tốc độ mạng  
Ta có: 2GB nhân với 1024 \=2048MB  
Lấy 2048 nhân với 8MB=16.384MB  
Lấy 16.384 chia cho 80=204.8 giây

### ***Phần 2 (Hành động):***

Viết lại đường dẫn file dưới dạng Relative Path sử dụng ký hiệu **. hoặc ..** Đề xuất các bước thiết lập "View Options" để nhận diện file mã độc.

\+"./data/db.csv"   
\+Các bước hiện đuôi file để phát hiện mã độc (.pdf.exe):

1. Mở File Explorer   
2. Trên thanh menu phía trên, chọn tab View.  
3. Trong mục Show/hide,  chọn vào ô File name extensions.  
   *Lúc này, file sẽ hiện rõ tên thật là tai-lieu-on-tap.pdf.exe $\rightarrow$ Tuyệt đối không mở file.*

