# Flutter các câu hỏi phỏng vấn thường gặp

## I. Câu hỏi về kiến thức cơ bản Flutter:

### 1. StatelessWidget và StatefulWidget khác nhau như thế nào ? ( Nên nêu ra điểm khác và giống )

**Giống nhau:**

- Đều là các lớp cơ bản trong Flutter để tạo ra UI components.

**Khác nhau:**

- **StatelessWidget**: Không thay đổi trong suốt vòng đời của nó. Sử dụng khi không cần quản lý trạng thái.
- **StatefulWidget**: Có thể thay đổi trong suốt vòng đời của nó. Sử dụng khi cần quản lý trạng thái.

### 2. Flutter là gì?

- Flutter là một SDK của Google để phát triển ứng dụng di động, web và desktop từ một mã nguồn duy nhất.
- Thành phần chính của Flutter bao gồm:
  -- Nền tảng Dart: giúp lập trình viên viết code và lập trình bằng ngôn ngữ Dart
  -- Flutter Engine
  -- Thư viện Foundation
  -- Các widget được thiết kế riêng

### 3. Flutter hoạt động như thế nào?

- Flutter sử dụng Dart và biên dịch xuống mã máy, cung cấp các widget để xây dựng UI, và sử dụng Skia để render giao diện.

### 4. Explain the Widget tree and how it works in Flutter?

- Widget tree là cấu trúc cây của các widget trong Flutter. Mỗi widget là một nút trong cây, và cây này được sử dụng để xác định giao diện người dùng của ứng dụng.

### 5. Bạn biết gì về Hot Reload và Hot Restart trong Flutter?

- **Hot Reload**: Cập nhật giao diện ngay lập tức mà không mất trạng thái hiện tại.
- **Hot Restart**: Tái khởi động ứng dụng, mất trạng thái hiện tại nhưng giữ lại mã mới.
