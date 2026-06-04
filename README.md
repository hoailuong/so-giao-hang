# so-giao-hang

Tuyệt vời! Việc đưa ứng dụng lên GitHub Pages là cách chuyên nghiệp nhất, hoàn toàn miễn phí, và nó sẽ biến "Sổ Giao Hàng" thành một trang web có đường link riêng (ten-cua-ban.github.io).

​Bạn không cần cài đặt phần mềm phức tạp trên máy tính đâu, làm ngay trên điện thoại được hết!
​Các bước thực hiện:

​Bước 1: Tạo tài khoản GitHub (Nếu chưa có)
​Truy cập vào github.com trên trình duyệt điện thoại.

​Bấm Sign up và làm theo hướng dẫn để tạo một tài khoản (Dùng Gmail của bạn).

​Bước 2: Tạo một "Kho chứa" (Repository)
​Sau khi đăng nhập, tại trang chủ GitHub, bấm vào dấu + ở góc trên bên phải > Chọn New repository.

​Repository name: Đặt tên là so-giao-hang (không dấu, cách nhau bằng dấu gạch ngang).

​Chọn chế độ Public (Để trang web có thể truy cập được).

​Đánh dấu vào ô Add a README file.

​Bấm nút Create repository.

​Bước 3: Đưa mã nguồn của bạn lên
​Trong kho chứa vừa tạo, bạn sẽ thấy nút Add file > Chọn Create new file.

​Ở ô đặt tên file, hãy gõ chính xác: index.html
​Quay lại giao diện Canvas bên phải của chúng ta, Copy toàn bộ đoạn mã.

​Dán vào khung soạn thảo trên GitHub.

​Kéo xuống dưới, bấm nút xanh Commit changes... > Bấm Commit changes lần nữa để xác nhận.

​Bước 4: Kích hoạt đường link web (GitHub Pages)
​Trong kho chứa của bạn, nhìn lên thanh menu (phía dưới tên repository), bấm vào tab Settings.

​Trong menu bên trái (hoặc cuộn xuống), tìm mục Pages.

​Tại mục Build and deployment > Source, chọn là Deploy from a branch.

​Tại mục Branch, chọn nhánh là main và thư mục là /(root) > Bấm Save.

​Đợi khoảng 1-2 phút, GitHub sẽ hiển thị đường link của bạn (dạng: https://ten-tai-khoan.github.io/so-giao-hang/).

​Mẹo quan trọng cho bạn:

​Sau khi có link: Hãy mở link đó trên trình duyệt điện thoại, rồi bấm "Thêm vào màn hình chính" như mình đã hướng dẫn trước đó. Từ nay nó sẽ là một ứng dụng web thực thụ.

​Cập nhật mã: Sau này nếu mình có chỉnh sửa gì cho bạn, bạn chỉ cần vào GitHub, mở file index.html đó ra, bấm biểu tượng cây bút (Edit) để dán mã mới vào và lưu lại là xong. Không bao giờ phải tải lại file hay cài lại app.
​Đừng quên chìa khóa AI (API Key)!
​Khi bạn đã đưa lên GitHub Pages thành công, hãy nhớ dán API Key của bạn vào dòng 349 (như mình đã hướng dẫn ở câu trước) thì các tính năng AI (Trộn Misa, Khớp Excel) mới hoạt động được.

## Huong dan tao chia khoa AI (API Key)

Bạn phát hiện vấn đề cực kỳ chính xác! Đây là nhược điểm của việc lưu thành file .html nội bộ trên máy so với việc chạy trên một trang web thực sự.

​Khi bạn chạy ứng dụng từ file cục bộ (offline) và không có mạng, hoặc chạy file nội bộ có mạng nhưng thiếu cấu hình, ứng dụng sẽ gặp một số vấn đề. Dưới đây là phân tích các lỗi và cách xử lý triệt để cho bạn:

​1. Vấn đề với AI Khớp Excel & Trộn Misa

​Tính năng này bị lỗi do 2 nguyên nhân:
​Thiếu chìa khóa AI (API Key): Trong mã nguồn hiện tại, dòng const apiKey = ""; đang để trống. AI của Google cần một "chìa khóa" cá nhân để nhận diện bạn là ai và cho phép quét ảnh.

​Cần Internet: AI là một hệ thống khổng lồ nằm trên máy chủ của Google, điện thoại của bạn không thể tự xử lý ảnh offline được. Khi bấm nút quét ảnh, điện thoại bắt buộc phải có mạng (4G/Wifi).

​👉 Cách xử lý (Lấy chìa khóa AI miễn phí):
​Bạn truy cập vào trang web: Google AI Studio (Đăng nhập bằng Gmail của bạn).

​Bấm nút Create API key (Tạo khóa API) -> Chọn Create API key in new project.

​Bạn sẽ nhận được một đoạn mã dài ngoằng (ví dụ: AIzaSyB...). Hãy copy đoạn mã đó.

​Quay lại đoạn mã nguồn ứng dụng, tìm đến dòng thứ 349 (khoảng giữa mã):

Sửa const apiKey = ""; thành const apiKey = "DÁN_MÃ_CỦA_BẠN_VÀO_ĐÂY";
(Nhớ giữ nguyên 2 dấu ngoặc kép).

#Đây là mã nhé


​Sau khi dán mã này, chỉ cần điện thoại bạn đang bật 4G/Wifi, tính năng AI sẽ hoạt động trơn tru dù bạn mở từ file .html trên máy!

​Bạn có muốn mình hỗ trợ thêm về cách "dọn dẹp" mã nguồn để tối ưu cho phiên bản web này không, hay bạn bắt tay vào làm thử nhé?
