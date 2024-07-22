# Các câu hỏi phỏng vấn Flutter

## I. Kiến thức cơ bản về Flutter

### 1. Sự khác nhau giữa StatelessWidget và StatefulWidget trong Flutter là gì?

- **StatelessWidget**: Không thay đổi; trạng thái không thể thay đổi theo thời gian.
- **StatefulWidget**: Có thể thay đổi; trạng thái có thể thay đổi trong suốt vòng đời của widget.

### 2. Giải thích vòng đời của Stateful Widget?

- `createState()`: Tạo ra trạng thái có thể thay đổi.
- `initState()`: Được gọi một lần khi trạng thái được tạo.
- `didChangeDependencies()`: Được gọi khi các phụ thuộc của widget thay đổi.
- `build()`: Mô tả phần giao diện người dùng được đại diện bởi widget.
- `setState()`: Cập nhật trạng thái và kích hoạt việc xây dựng lại.
- `deactivate()`: Được gọi khi đối tượng trạng thái bị loại khỏi cây tạm thời.
- `dispose()`: Được gọi khi đối tượng trạng thái bị loại bỏ hoàn toàn.

### 3. Khi nào bạn sử dụng WidgetsBindingObserver?

- Để lắng nghe các thay đổi trong trạng thái vòng đời của ứng dụng, chẳng hạn như khi ứng dụng bị tạm dừng, tiếp tục hoặc dừng lại.

### 4. Flutter tree shaking là gì?

- Tree shaking là quá trình loại bỏ mã không sử dụng khỏi bản phát hành cuối cùng, giúp giảm kích thước ứng dụng.

### 5. Widget Spacer là gì?

- Spacer tạo ra một khoảng trống có thể điều chỉnh trong một container dạng flex như Row hoặc Column.

### 6. Sự khác nhau giữa hot restart và hot reload là gì?

- **Hot Reload**: Tiêm mã cập nhật vào Dart VM, bảo lưu trạng thái.
- **Hot Restart**: Khởi động lại hoàn toàn ứng dụng, làm mất trạng thái hiện tại.

### 7. InheritedWidget là gì? Liệt kê một số ví dụ.

- InheritedWidget cho phép truyền dữ liệu xuống cây widget một cách hiệu quả. Các ví dụ bao gồm `InheritedTheme`, `InheritedModel`.

### 8. Tại sao phương thức build() lại nằm trên State và không phải StatefulWidgets?

- Đối tượng `State` là có thể thay đổi và giữ trạng thái của widget, vì vậy nó có thể xây dựng lại widget khi trạng thái thay đổi.

### 9. Tệp pubspec trong Dart là gì?

- Tệp `pubspec.yaml` quản lý các phụ thuộc, metadata và cấu hình của dự án.

### 10. Flutter hoạt động với mã gốc như thế nào?

- Flutter biên dịch thành mã ARM gốc và sử dụng các widget gốc để hiển thị, cung cấp hiệu suất cao và giao diện người dùng giống hệt như gốc.

### 11. Navigator là gì và Routes là gì trong Flutter?

- **Navigator**: Quản lý một ngăn xếp các đối tượng route để điều hướng giữa các màn hình.
- **Routes**: Định nghĩa các trang/màn hình trong ứng dụng.

### 12. PageRoute là gì?

- PageRoute là một lớp trừu tượng định nghĩa các chuyển tiếp khi điều hướng đến các trang khác nhau, như `MaterialPageRoute`.

### 13. Giải thích async, await và Futures.

- **async**: Đánh dấu một hàm là bất đồng bộ.
- **await**: Dừng thực thi cho đến khi Future hoàn tất.
- **Future**: Đại diện cho một giá trị tiềm năng hoặc lỗi sẽ có vào một thời điểm nào đó.

### 14. Làm thế nào để cập nhật ListView một cách động?

- Sử dụng `StatefulWidget` và cập nhật danh sách bằng `setState()` để phản ánh các thay đổi.

### 15. Stream là gì?

- Một Stream là một chuỗi các sự kiện bất đồng bộ. Nó giống như một Future nhưng có thể cung cấp nhiều giá trị theo thời gian.

### 16. Keys trong Flutter là gì và khi nào bạn nên sử dụng chúng?

- Keys bảo tồn trạng thái của các widget khi chúng di chuyển trong cây widget. Sử dụng chúng để duy trì trạng thái trong một tập hợp các widget.

### 17. GlobalKeys là gì?

- GlobalKeys cung cấp cách để truy cập trạng thái của widget trên toàn bộ ứng dụng. Chúng được sử dụng để xác định một widget một cách duy nhất.

### 18. Khi nào bạn nên sử dụng mainAxisAlignment và crossAxisAlignment?

- Sử dụng `mainAxisAlignment` và `crossAxisAlignment` để căn chỉnh các con cái của Row hoặc Column theo trục chính và trục chéo tương ứng.

### 19. Khi nào bạn có thể sử dụng double.INFINITY?

- Sử dụng `double.INFINITY` để cung cấp kích thước vô hạn cho một widget theo một hướng cụ thể.

### 20. Ticker, Tween và AnimatedBuilder là gì?

- **Ticker**: Gọi một callback ở một tỷ lệ cố định.
- **Tween**: Định nghĩa sự nội suy giữa các giá trị bắt đầu và kết thúc.
- **AnimatedBuilder**: Một widget mà tự động xây dựng lại khi animation thay đổi.

### 21. Ephemeral state là gì?

- Ephemeral state là trạng thái tạm thời và chỉ được quản lý trong widget, sử dụng `setState`.

### 22. Widget AspectRatio được sử dụng để làm gì?

- AspectRatio buộc con cái của nó phải có một tỷ lệ khung hình cụ thể.

### 23. Làm thế nào để truy cập các thuộc tính của StatefulWidget từ State của nó?

- Sử dụng `widget.propertyName` để truy cập các thuộc tính của StatefulWidget từ State của nó.

### 24. Có giới hạn nào được đề xuất về số lượng FloatingActionButton mà một màn hình có thể có không? Đưa ra lý do (s) cho câu trả lời của bạn.

- Được đề xuất chỉ có một `FloatingActionButton` trên mỗi màn hình để tránh sự lộn xộn và duy trì sự tập trung.

### 25. Đề cập đến hai hoặc nhiều hoạt động mà bạn cần sử dụng hoặc trả về một Future.

- Các yêu cầu mạng và đọc từ cơ sở dữ liệu.

### 26. Mục đích của SafeArea là gì?

- SafeArea chèn padding để tránh bị xâm nhập bởi UI hệ thống, như notch và thanh trạng thái.

### 27. Khi nào sử dụng mainAxisSize?

- Sử dụng `mainAxisSize` để xác định bao nhiêu không gian mà Row hoặc Column nên chiếm theo trục chính.

### 28. SizedBox VS Container?

- **SizedBox**: Một hộp có kích thước cụ thể.
- **Container**: Một widget đa năng có thể chứa các widget khác và có các thuộc tính bổ sung như padding, margin, v.v.

### 29. Liệt kê các widget Visibility trong Flutter và sự khác biệt của chúng?

- **Visibility**: Điều khiển tính hiển thị của một widget.
- **Offstage**: Đặt widget ra ngoài màn hình.
- **Opacity**: Làm cho một widget trong suốt mà không loại bỏ nó khỏi bố cục.

### 30. Chúng ta có thể sử dụng thuộc tính Color và Decoration đồng thời trong Container không? Giải thích.

- Không, nếu `decoration` không null, thuộc tính `color` phải là null vì `decoration` bao gồm màu sắc.

### 31. Để CrossAxisAlignment.baseline hoạt động, thuộc tính nào khác cần được đặt?

- Đặt `textBaseline` thành `TextBaseline.alphabetic` hoặc `TextBaseline.ideographic`.

### 32. Khi nào chúng ta nên sử dụng resizeToAvoidBottomInset?

- Sử dụng `resizeToAvoidBottomInset` để điều chỉnh màn hình khi bàn phím trên màn hình xuất hiện để ngăn bàn phím che khuất các trường nhập liệu.

### 33. Sự khác biệt giữa 'as', 'show' và 'hide' trong câu lệnh import là gì?

- **as**: Tạo một bí danh cho thư viện.
- **show**: Nhập chỉ các thành viên được chỉ định.
- **hide**: Nhập tất cả các thành viên ngoại trừ các thành viên được chỉ định.

### 34. Tầm quan trọng của TextEditingController là gì?

- TextEditingController quản lý giá trị của trường văn bản và cho phép thao tác văn bản và lắng nghe các thay đổi.

### 35. Tại sao chúng ta sử dụng thuộc tính Reverse trong Listview?

- Để đảo ngược thứ tự các mục trong danh sách.

### 36. Sự khác biệt giữa Modal và Persistent BottomSheet với một ví dụ?

- **Modal BottomSheet**: Xuất hiện tạm thời và chặn tương tác với phần còn lại của ứng dụng.
- **Persistent BottomSheet**: Ở lại trên màn hình, che phủ một phần nội dung khác.

### 37. Inherited Widget khác với Provider như thế nào?

- **InheritedWidget**: Một phần của framework Flutter, được sử dụng để truyền dữ liệu xuống cây widget.
- **Provider**: Gói bên thứ ba, linh hoạt hơn và dễ sử dụng hơn cho quản lý trạng thái.

### 38. UnmodifiableListView là gì?

- `UnmodifiableListView` là một danh sách không thể thay đổi.

### 39. Sự khác biệt giữa các toán tử "?? và ?." là gì?

- **??**: Toán tử nhận dạng null; trả về toán tử bên phải nếu toán tử bên trái là null.
- **?.**: Truy cập nhận dạng null; gọi phương thức hoặc truy cập thuộc tính nếu đối tượng không phải là null.

### 40. Mục đích của ModalRoute.of() là gì?

- Truy cập thông tin và trạng thái của route hiện tại.

### 41. Sự khác biệt giữa Navigator.pushNamed và Navigator.pushReplacementNamed là gì?

- **Navigator.pushNamed**: Đẩy một route mới lên ngăn xếp.
- **Navigator.pushReplacementNamed**: Thay thế route hiện tại bằng một route mới.

### 42. Sự khác biệt giữa Single Instance và Scoped Instance?

- **Single Instance**: Một instance được sử dụng xuyên suốt ứng dụng.
- **Scoped Instance**: Các instance được tạo ra trong một phạm vi hoặc ngữ cảnh cụ thể.

### 43. vsync là gì?

- **vsync**: Đồng bộ hóa animation với tỷ lệ làm mới của màn hình để đảm bảo các animation mượt mà.

### 44. Khi nào animation đạt trạng thái completed hoặc dismissed?

- **Completed**: Khi animation đạt đến giá trị lớn nhất.
- **Dismissed**: Khi animation đạt đến giá trị nhỏ nhất.

### 45. Sự khác biệt giữa `AnimationController` và `Animation` là gì?

- **AnimationController**: Điều khiển animation và cung cấp các phương thức điều khiển.
- **Animation**: Mô tả các giá trị và trạng thái của animation.

### 46. Khi nào sử dụng SingleTickerProviderStateMixin và TickerProviderStateMixin?

- **SingleTickerProviderStateMixin**: Đối với một controller animation duy nhất.
- **TickerProviderStateMixin**: Đối với nhiều controller animation.

### 47. Định nghĩa TweenAnimation là gì?

- **TweenAnimation**: Nội suy giữa hai giá trị trong một khoảng thời gian bằng cách sử dụng Tween và AnimationController.

### 48. Tầm quan trọng của Ticker là gì?

- Ticker gọi một hàm callback ở mỗi khung hình để điều khiển các animation.

### 49. Tại sao chúng ta cần mixins?

- Mixins được sử dụng để tái sử dụng mã của một lớp trong nhiều cấu trúc lớp khác nhau.
