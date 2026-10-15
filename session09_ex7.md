## Phần 1. Phân tích lỗi

### 1. Liệt kê lỗi cú pháp và hậu quả

|Dòng|Lỗi cú pháp|Hậu quả khi render|
|-|-|-|
|1|`\##` có dấu Escape `\` trước Heading|Tiêu đề có thể hiển thị thành văn bản thường|
|3|`\###Lưu ý quan trọng` thiếu khoảng trắng sau `###` và có dấu Escape|Không hiển thị thành Heading cấp 3|
|6–9|`-Bước` thiếu khoảng trắng sau dấu `-`|Không tạo được danh sách Bullet List|
|6|Cú pháp `[GitHub]\([github.com](http://github.com/))` không đúng|Liên kết có thể hiển thị sai hoặc không dẫn đến trang mong muốn|
|7|`\*\*HNKS25CNTT1_IT101_Session08` thiếu dấu đóng và có Escape|Nội dung không được in đậm|
|11|`*> Deadline` sử dụng sai thứ tự ký hiệu|Không tạo được Blockquote đúng cách|
|11|Các dấu `*` và `\*` không ghép thành cặp định dạng hợp lệ|Cảnh báo không được in đậm hoặc in nghiêng như mong muốn|

Ngoài ra, các dấu `\` cuối dòng cần được kiểm tra và loại bỏ nếu không có chủ đích tạo ngắt dòng.

### 2. Giải thích nguyên nhân

Các lỗi xuất hiện do thiếu dấu cách sau ký hiệu Markdown, thiếu dấu đóng định dạng Bold, sử dụng sai cú pháp Link và Blockquote, đồng thời dùng ký tự Escape `\` không đúng vị trí. Những lỗi này khiến hệ thống không nhận diện được cấu trúc tài liệu, làm nội dung hiển thị sai khi xem trước trên GitHub Pages.

## Phần 2. Sửa lỗi

### 3. Đoạn Markdown hoàn chỉnh
```
## Hướng Dẫn Nộp Bài Tập - Session 08

### Lưu ý quan trọng

Các bước nộp bài:

- Bước 1: Tạo tài khoản GitHub tại [GitHub](https://github.com/).
- Bước 2: Tạo repository mới đặt tên theo định dạng **HNKS25CNTT1_IT101_Session08**.
- Bước 3: Upload file `.md` của bài làm lên repository.
- Bước 4: Copy đường dẫn và nộp lên *Portal*.

> **Deadline:** Chủ nhật 23:59 — **Nộp muộn sẽ bị trừ 50% điểm!**
```
### 4. Bẫy dữ liệu: Quên `https://` trong liên kết

Nếu sinh viên viết `[GitHub](github.com)`, Markdown vẫn có thể tạo liên kết nhưng trình duyệt thường hiểu `github.com` là đường dẫn tương đối, không phải địa chỉ website GitHub.



