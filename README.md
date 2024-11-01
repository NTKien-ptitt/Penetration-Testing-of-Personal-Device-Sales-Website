# Kiểm thử Xâm nhập Website Bán Thiết Bị Cá Nhân
Kiểm thử xâm nhập (penetration testing) là một phương pháp quan trọng trong an ninh thông tin, nhằm xác định và đánh giá các lỗ hổng bảo mật trong một ứng dụng hoặc hệ thống. Trong bối cảnh một website bán thiết bị cá nhân, việc thực hiện kiểm thử xâm nhập không chỉ giúp bảo vệ dữ liệu người dùng mà còn đảm bảo tính toàn vẹn và sẵn sàng của dịch vụ.

## Mục tiêu Kiểm thử Xâm nhập
- Xác định lỗ hổng bảo mật: Tìm kiếm các điểm yếu trong ứng dụng web có thể bị khai thác bởi kẻ tấn công.
- Đánh giá rủi ro: Xác định mức độ nghiêm trọng của từng lỗ hổng và khả năng bị khai thác.
- Cải thiện an ninh: Đề xuất các biện pháp khắc phục để giảm thiểu rủi ro.
### Công cụ sử dụng trong Kiểm thử Xâm nhập
- Burp Suite: Là một công cụ phổ biến trong kiểm thử xâm nhập, Burp Suite cho phép người dùng kiểm tra và sửa đổi các yêu cầu HTTP/HTTPS giữa trình duyệt và server. Nó cung cấp nhiều tính năng như quét lỗ hổng, phân tích traffic, và hỗ trợ tạo payload.

- OWASP ZAP (Zed Attack Proxy): Đây là một công cụ mã nguồn mở, giúp kiểm tra lỗ hổng bảo mật trên ứng dụng web. ZAP có thể tự động quét và phát hiện các vấn đề an ninh, cũng như cho phép người dùng thực hiện các tấn công thủ công.

- Nmap: Dùng để quét mạng và xác định các dịch vụ đang chạy trên server. Nmap giúp tìm ra các cổng mở và ứng dụng, từ đó có thể đánh giá các lỗ hổng liên quan.

- Metasploit: Là một framework mạnh mẽ cho phép khai thác các lỗ hổng bảo mật đã được xác định. Nó cung cấp nhiều module cho việc phát hiện và khai thác lỗ hổng.

- Nessus: Là một trong những công cụ quét lỗ hổng hàng đầu, Nessus cung cấp khả năng quét an ninh cho hệ thống và ứng dụng. Nó giúp phát hiện các lỗ hổng bảo mật, cấu hình sai lệch và các vấn đề liên quan đến bảo mật khác.

- Acunetix: Là một công cụ kiểm thử xâm nhập tự động giúp phát hiện các lỗ hổng bảo mật trong ứng dụng web. Acunetix quét các lỗ hổng như SQL Injection, XSS, và nhiều lỗ hổng khác một cách tự động và dễ dàng.

- Hydra: Là một công cụ brute-force mạnh mẽ, Hydra cho phép kiểm tra độ mạnh của các cơ chế xác thực bằng cách thử nhiều tên đăng nhập và mật khẩu khác nhau. Đây là công cụ hữu ích để kiểm tra sự bảo mật của các trang web có chức năng đăng nhập.
  
## kế hoạch kiểm thử xâm nhập cho website bán thiết bị cá nhân dựa trên OWASP Testing Guide
1. Thu thập thông tin
- Quét cấu trúc trang web
- Thu thập thông tin từ robots.txt
- Thu thập thông tin từ sơ đồ trang web
- Xác định công nghệ sử dụng
- Kiểm tra mã nhận xét và siêu dữ liệu
- Quét các tên miền phụ
2. Kiểm tra xác thực
- Thử bỏ qua xác thực
- Kiểm tra cơ chế đăng nhập/đăng ký
- Kiểm tra chính sách mật khẩu
- Kiểm tra chức năng quên mật khẩu
- Kiểm tra thời gian chờ và xử lý phiên
- Kiểm tra tấn công vũ phu
3. Kiểm tra ủy quyền
- Kiểm tra phân quyền
- Kiểm tra leo thang đặc quyền dọc
- Kiểm tra leo thang đặc quyền ngang
- Kiểm tra truyền tải thư mục
- Bỏ qua lược đồ ủy quyền
- Kiểm tra kiểm soát truy cập
- Kiểm tra quản lý phiên
- Kiểm tra thời gian chờ của phiên
- Cố định phiên kiểm tra
4. Kiểm tra bảo mật CSRF
- Kiểm tra thuộc tính cookie
- Kiểm tra phiên khó hiểu
- Kiểm tra xác thực đầu vào
5. Kiểm tra lỗ hổng
- Kiểm tra XSS
Được phản ánh
Lưu trữ
DOM
- Kiểm tra tiêm SQL
- Kiểm tra tiêm LDAP
- Kiểm tra tiêm XML
- Kiểm tra tiêm XML SSI
- ...
6. Kiểm tra tải lên tệp
- Kiểm tra giả mạo tham số
- Kiểm tra logic
- Kiểm tra logic giao dịch
- Kiểm tra các tham số số
- Kiểm tra bỏ qua quy trình làm việc
- Kiểm tra xác thực dữ liệu
- Kiểm tra khả năng forge requests
7. Kiểm tra phía máy khách
- Kiểm tra các điều khiển phía máy khách
- Kiểm tra chia sẻ tài nguyên nguồn gốc chéo (CORS)
- Kiểm tra các tính năng HTML5
- Kiểm tra lưu trữ máy khách
- Kiểm tra chính sách miền chéo
8. Kiểm tra API
- Kiểm tra xác thực API
- Kiểm tra đầu vào API
- Kiểm tra giới hạn tốc độ
- Kiểm tra xử lý lỗi
- Kiểm tra phiên bản

# Các lổ hổng OWASP
## 1. Injection
Mô tả: Lỗi Injection xảy ra khi kẻ tấn công có thể chèn mã độc vào các truy vấn hoặc lệnh mà ứng dụng thực thi. Điều này cho phép họ thực hiện các lệnh không mong muốn trong hệ thống.

Ví dụ:

SQL Injection: Kẻ tấn công chèn mã SQL độc hại vào các trường nhập liệu.
Payload:
sql
Sao chép mã
' OR '1'='1
Khi mã này được chèn vào một trường tìm kiếm, nó có thể biến một truy vấn hợp lệ thành một truy vấn trả về tất cả các bản ghi, do đó cho phép kẻ tấn công xem dữ liệu nhạy cảm.
## 2. Cross-Site Scripting (XSS)
Mô tả: XSS xảy ra khi ứng dụng web cho phép người dùng chèn mã JavaScript độc hại vào trang web. Mã này sẽ được thực thi trong trình duyệt của người dùng khác, cho phép kẻ tấn công đánh cắp thông tin nhạy cảm hoặc thực hiện hành động thay mặt người dùng.

Ví dụ:

Kẻ tấn công có thể gửi một liên kết chứa mã JavaScript đến một người dùng khác.
Payload:
javascript
Sao chép mã
<script>alert('XSS Attack!');</script>
Khi người dùng nhấp vào liên kết, đoạn mã JavaScript này sẽ hiển thị một hộp thoại cảnh báo, nhưng cũng có thể được sử dụng để đánh cắp cookie của người dùng.
## 3. Broken Authentication
Mô tả: Đây là lỗ hổng xảy ra khi hệ thống xác thực không đủ mạnh, cho phép kẻ tấn công chiếm đoạt tài khoản người dùng.

Ví dụ:

Sử dụng mật khẩu yếu hoặc không khóa tài khoản sau một số lần đăng nhập thất bại.
Kẻ tấn công có thể dùng công cụ brute-force như Hydra để thử nhiều tên đăng nhập và mật khẩu.
Payload:
bash
Sao chép mã
hydra -l admin -P passwords.txt http-get://example.com/login
## 4. Sensitive Data Exposure
Mô tả: Lỗi này xảy ra khi thông tin nhạy cảm như mật khẩu, thông tin thẻ tín dụng, hoặc dữ liệu cá nhân không được mã hóa hoặc bảo vệ đúng cách.

Ví dụ:

Một trang web gửi thông tin thẻ tín dụng qua HTTP thay vì HTTPS, cho phép kẻ tấn công chặn và xem thông tin này.
Kẻ tấn công có thể sử dụng công cụ như Wireshark để theo dõi và phân tích lưu lượng mạng.
## 5. Cross-Site Request Forgery (CSRF)
Mô tả: CSRF cho phép kẻ tấn công gửi yêu cầu giả mạo từ một người dùng đã đăng nhập đến ứng dụng web mà không có sự đồng ý của họ.

Ví dụ:

Một trang web độc hại có thể gửi yêu cầu chuyển tiền đến tài khoản của kẻ tấn công.
Payload:
html
Sao chép mã
<form action="https://example.com/transfer" method="POST">
    <input type="hidden" name="amount" value="1000">
    <input type="submit" value="Send Money">
</form>
Nếu người dùng đã đăng nhập, khi họ mở trang này, yêu cầu sẽ được gửi đi mà không cần xác nhận.
## 6. Security Misconfiguration
Mô tả: Lỗi cấu hình bảo mật xảy ra khi các cài đặt không được thiết lập đúng cách, dẫn đến các điểm yếu trong hệ thống.

Ví dụ:

Để lại thông tin cấu hình mặc định (như username: admin, password: admin) trên ứng dụng.
Kẻ tấn công có thể dễ dàng truy cập vào tài khoản quản trị và chiếm quyền kiểm soát.
## 7. Insecure Direct Object References (IDOR)
Mô tả: IDOR cho phép kẻ tấn công truy cập vào các tài nguyên mà họ không nên được phép truy cập, bằng cách sửa đổi các tham số trong URL.

Ví dụ:

Một URL yêu cầu thông tin người dùng có thể trông như sau:
bash
Sao chép mã
https://example.com/profile?id=123
Kẻ tấn công có thể thay đổi ID thành một giá trị khác (ví dụ, id=124) để truy cập thông tin của người dùng khác.
## 8. Insufficient Logging & Monitoring
Mô tả: Thiếu việc ghi chép và theo dõi các hoạt động quan trọng có thể khiến việc phát hiện và ứng phó với các cuộc tấn công trở nên khó khăn.

Ví dụ:

Nếu một ứng dụng không ghi lại các lần đăng nhập thất bại hoặc không cảnh báo khi có nhiều lần truy cập không hợp lệ, kẻ tấn công có thể dễ dàng tấn công mà không bị phát hiện.
## 9. Remote Code Execution (RCE)
Mô tả: Lỗi RCE cho phép kẻ tấn công chạy mã độc trên server thông qua các yêu cầu không được kiểm tra.

Ví dụ:

Một trang web có chức năng tải lên tệp mà không kiểm tra loại tệp có thể cho phép kẻ tấn công tải lên một script PHP độc hại.
Payload:
php
Sao chép mã
<?php system($_GET['cmd']); ?>
Khi script này được chạy, kẻ tấn công có thể gửi yêu cầu để thực thi các lệnh trên server.
## 10. Directory Traversal
Mô tả: Lỗi này cho phép kẻ tấn công truy cập vào các file và thư mục trên server không được phép bằng cách thay đổi đường dẫn.

Ví dụ:

Một yêu cầu để tải về một file cụ thể có thể trông như sau:
arduino
Sao chép mã
https://example.com/download?file=report.pdf
Nếu ứng dụng không kiểm tra đúng cách, kẻ tấn công có thể thay đổi tham số thành ../../etc/passwd để truy cập vào file nhạy cảm của hệ thống.

# Một số biện pháp phòng thủ

## 1. Injection
Mô tả: Lỗi Injection xảy ra khi kẻ tấn công có thể chèn mã độc vào truy vấn hoặc lệnh mà ứng dụng thực thi, dẫn đến thực hiện các hành động không mong muốn.
Biện pháp phòng ngừa:
Sử dụng Prepared Statements: Đây là phương pháp tốt nhất để ngăn chặn SQL Injection. Ví dụ trong PHP:
php
Sao chép mã
$stmt = $pdo->prepare("SELECT * FROM users WHERE email = :email");
$stmt->execute(['email' => $userInput]);
Kiểm tra và làm sạch dữ liệu đầu vào: Xác minh dữ liệu nhập vào có hợp lệ hay không và loại bỏ các ký tự không cần thiết.
## 2. Cross-Site Scripting (XSS)
Mô tả: Lỗi XSS cho phép kẻ tấn công chèn mã JavaScript vào trang web, mà mã này sẽ được thực thi trong trình duyệt của người dùng khác.
Biện pháp phòng ngừa:
Mã hóa đầu ra: Sử dụng htmlspecialchars() trong PHP để đảm bảo rằng các ký tự đặc biệt được mã hóa.
php
Sao chép mã
echo htmlspecialchars($userInput, ENT_QUOTES, 'UTF-8');
Sử dụng Content Security Policy (CSP): Thiết lập CSP trong header HTTP để chỉ cho phép tải mã từ các nguồn đáng tin cậy.
css
Sao chép mã
Content-Security-Policy: script-src 'self';
## 3. Broken Authentication
Mô tả: Hệ thống xác thực yếu có thể bị chiếm đoạt tài khoản người dùng.
Biện pháp phòng ngừa:
Sử dụng xác thực hai yếu tố (2FA): Đưa ra yêu cầu xác thực thứ hai (như mã gửi qua SMS).
Khóa tài khoản sau nhiều lần đăng nhập thất bại: Sau 5 lần đăng nhập không thành công, tài khoản sẽ bị khóa trong một khoảng thời gian.
## 4. Sensitive Data Exposure
Mô tả: Dữ liệu nhạy cảm không được bảo vệ có thể bị rò rỉ.
Biện pháp phòng ngừa:
Mã hóa dữ liệu nhạy cảm: Sử dụng HTTPS cho tất cả các giao tiếp và mã hóa thông tin nhạy cảm trước khi lưu vào cơ sở dữ liệu.
Hạn chế thu thập dữ liệu: Chỉ thu thập thông tin cần thiết và bảo vệ dữ liệu đó bằng cách mã hóa.
## 5. Cross-Site Request Forgery (CSRF)
Mô tả: CSRF cho phép kẻ tấn công gửi yêu cầu giả mạo từ người dùng đã đăng nhập.
Biện pháp phòng ngừa:
Sử dụng token CSRF: Mỗi form gửi dữ liệu đều phải có token CSRF.
html
Sao chép mã
<input type="hidden" name="csrf_token" value="<?= $_SESSION['csrf_token']; ?>">
Kiểm tra header HTTP Referer: Xác minh rằng yêu cầu đến từ trang của bạn.
## 6. Security Misconfiguration
Mô tả: Cấu hình bảo mật không đúng có thể dẫn đến lỗ hổng.
Biện pháp phòng ngừa:
Rà soát cấu hình thường xuyên: Kiểm tra các cài đặt và cập nhật chúng theo hướng dẫn an ninh.
Gỡ bỏ dịch vụ không cần thiết: Tắt các dịch vụ mà bạn không sử dụng.
## 7. Insecure Direct Object References (IDOR)
Mô tả: Kẻ tấn công có thể truy cập vào các đối tượng mà họ không có quyền truy cập bằng cách thay đổi tham số trong URL.
Biện pháp phòng ngừa:
Kiểm tra quyền truy cập: Trước khi cho phép người dùng truy cập vào tài nguyên, hãy kiểm tra xem họ có quyền hay không.
Sử dụng ID ngẫu nhiên: Sử dụng các giá trị ngẫu nhiên hoặc mã hóa cho các tham số trong URL.
## 8. Insufficient Logging & Monitoring
Mô tả: Thiếu ghi chép có thể khiến việc phát hiện các cuộc tấn công trở nên khó khăn.
Biện pháp phòng ngừa:
Ghi lại hoạt động quan trọng: Ghi lại tất cả các hoạt động như đăng nhập và truy cập dữ liệu nhạy cảm.
Thiết lập cảnh báo: Cảnh báo khi có các hoạt động đáng ngờ trong nhật ký, chẳng hạn như nhiều lần đăng nhập thất bại từ một địa chỉ IP.
## 9. Remote Code Execution (RCE)
Mô tả: Lỗi này cho phép kẻ tấn công chạy mã độc trên server.
Biện pháp phòng ngừa:
Kiểm tra loại tệp tải lên: Chỉ cho phép các loại tệp an toàn và không cho phép tải lên mã độc.
Cách ly môi trường thực thi: Sử dụng container hoặc môi trường ảo hóa để cách ly việc thực thi mã.
## 10. Directory Traversal
Mô tả: Kẻ tấn công có thể truy cập vào các tệp và thư mục không được phép bằng cách thay đổi đường dẫn.
Biện pháp phòng ngừa:
Kiểm tra và giới hạn đường dẫn: Xác minh rằng các đường dẫn chỉ đến các thư mục cho phép.
Sử dụng các hàm an toàn: Sử dụng các hàm như basename() để loại bỏ đường dẫn không hợp lệ.
