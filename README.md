# Bài tập thực hành kiểm thử tự động End-to-End với Cypress
## 📌 Mục tiêu

Làm quen và thực hành kiểm thử tự động End-to-End (E2E) bằng Cypress

Xây dựng các kịch bản kiểm thử phổ biến cho một website thương mại điện tử mẫu

Kiểm tra các chức năng quan trọng: đăng nhập, giỏ hàng, sắp xếp sản phẩm và xóa sản phẩm

Website được sử dụng để kiểm thử:
👉 https://www.saucedemo.com

## 🛠️ Công nghệ & công cụ sử dụng

Node.js (>= 14)

Cypress v15

Visual Studio Code

Trình duyệt tích hợp của Cypress (Electron)

## 📚 File kịch bản kiểm thử
<img width="1875" height="962" alt="Screenshot 2026-02-14 174902" src="https://github.com/user-attachments/assets/eca13bc9-eaea-448a-9c0c-ad11c20c2377" />

<img width="1864" height="969" alt="Screenshot 2026-02-14 174914" src="https://github.com/user-attachments/assets/95ee73cc-c6b9-40be-85a4-5d00bea6647f" />

## ✅ Các kịch bản kiểm thử đã thực hiện
1️⃣ Kiểm tra đăng nhập thành công

File: login_spec.cy.js

Truy cập trang đăng nhập

Nhập tài khoản hợp lệ:

Username: standard_user

Password: secret_sauce

Nhấn Login

Xác minh:

<img width="1905" height="915" alt="Screenshot 2026-02-14 171838" src="https://github.com/user-attachments/assets/5c6b175b-1cff-4516-a145-e0878c28faeb" />

📷 Kết quả: Đăng nhập thành công và chuyển đến trang danh sách sản phẩm.


2️⃣ Kiểm tra đăng nhập thất bại

File: login_spec.cy.js

Nhập tài khoản không hợp lệ

Nhấn Login

Xác minh:

Hiển thị thông báo lỗi
"Username and password do not match any user in this service"

<img width="1899" height="917" alt="Screenshot 2026-02-14 171920" src="https://github.com/user-attachments/assets/75ad0775-8ae9-4326-9fff-f1665b02c34b" />

📷 Kết quả: Thông báo lỗi hiển thị đúng như mong đợi.


3️⃣ Thêm sản phẩm vào giỏ hàng

File: cart_spec.cy.js

Đăng nhập với tài khoản hợp lệ

Thêm sản phẩm đầu tiên vào giỏ hàng

Xác minh:

Biểu tượng giỏ hàng hiển thị số lượng 1

<img width="1913" height="920" alt="Screenshot 2026-02-14 172411" src="https://github.com/user-attachments/assets/d9f810cf-2bbc-4bde-aae8-30b79486f22d" />

📷 Kết quả: Sản phẩm được thêm thành công vào giỏ hàng.

4️⃣ Sắp xếp sản phẩm theo giá (Low → High)

File: cart_spec.cy.js

Đăng nhập

Chọn bộ lọc Price (low to high)

Xác minh:

Sản phẩm đầu tiên có giá $7.99

<img width="1903" height="905" alt="Screenshot 2026-02-14 172420" src="https://github.com/user-attachments/assets/3a0ef8d0-0bce-4da7-ae88-261cf6aaab2d" />

📷 Kết quả: Danh sách sản phẩm được sắp xếp đúng theo giá tăng dần.


5️⃣ Xóa sản phẩm khỏi giỏ hàng (kịch bản mở rộng)

File: cart_spec.cy.js

Đăng nhập

Thêm sản phẩm vào giỏ hàng

Nhấn nút Remove

Xác minh:

Biểu tượng giỏ hàng không còn hiển thị

Hoặc số lượng sản phẩm trở về 0

<img width="1898" height="909" alt="Screenshot 2026-02-14 172438" src="https://github.com/user-attachments/assets/5f7064ad-a066-4602-bb4f-929f3ae33a1e" />

📷 Kết quả: Sản phẩm được xóa thành công khỏi giỏ hàng.

## 📸 Kết quả chạy kiểm thử
-Tất cả các kịch bản đều chạy PASS
-Kết quả được minh họa bằng ảnh chụp màn hình trong Cypress Runner
-Các ảnh được đính kèm trực tiếp trong repo theo yêu cầu bài tập

## 📝 Kết luận
-Hoàn thành đầy đủ các yêu cầu của bài tập
-Làm quen với cách tổ chức test bằng describe, it, beforeEach
-Hiểu rõ cách Cypress phát hiện và chạy nhiều test case trong cùng một file
-Thực hành kiểm thử E2E cho các luồng nghiệp vụ quan trọng của một website bán hàng






# Kiểm thử hiệu năng với Apache JMeter

## 1. Giới thiệu
Bài tập này nhằm mục đích giúp sinh viên:
- Làm quen với công cụ **Apache JMeter** trong kiểm thử hiệu năng
- Thiết kế và thực thi các kịch bản kiểm thử với nhiều mức tải khác nhau
- Phân tích kết quả kiểm thử dựa trên các chỉ số hiệu năng cơ bản

Công cụ được sử dụng:
- Apache JMeter
- Java
- Trình duyệt JMeter GUI
- GitHub để quản lý và nộp bài


## 2. Website được kiểm thử

- https://vnexpress.net
- https://www.example.com/
- https://shop.mixigaming.com
- https://truyenqqno.com/

## 3. Cấu trúc thư mục
<img width="271" height="126" alt="image" src="https://github.com/user-attachments/assets/2da97339-24c7-4598-ae90-a2176515ef3e" />


## 4. Mô tả Test Plan

Test Plan bao gồm 3 Thread Group, tương ứng với 3 kịch bản kiểm thử khác nhau.

## 5. Thread Group 1 – Kịch bản cơ bản

Mục tiêu:
Kiểm tra phản hồi của website với số lượng người dùng nhỏ.

Cấu hình:

Number of Threads (Users): 10

Loop Count: 5

Ramp-up Period: 10 giây

Phương thức: HTTP GET

URL: https://www.example.com/
<img width="1522" height="861" alt="image" src="https://github.com/user-attachments/assets/e1b49c1d-5c9b-4e94-8640-76f16ef3dcc7" />

Kết quả mong đợi:

Website phản hồi ổn định

Không xuất hiện lỗi (Error Rate = 0%)

<img width="1507" height="847" alt="image" src="https://github.com/user-attachments/assets/b9adeb3a-1fbc-4136-86b1-663a304717d0" />

<!-- Chèn ảnh kết quả Thread Group 1 tại đây -->
## 6. Thread Group 2 – Kịch bản tải nặng

Mục tiêu:
Đánh giá khả năng chịu tải của website khi số lượng người dùng tăng cao.

Cấu hình:

Number of Threads (Users): 50

Ramp-up Period: 30 giây

Loop Count: 1

Phương thức: HTTP GET

URL:https://shop.mixigaming.com/
<img width="1517" height="852" alt="image" src="https://github.com/user-attachments/assets/43da8c1d-d370-443d-ad92-847ecf6ab7da" />

Trang chủ

Một trang con (bài viết hoặc danh mục)

Kết quả mong đợi:

Thời gian phản hồi tăng so với Thread Group 1

Website vẫn hoạt động, không bị sập

<img width="1507" height="843" alt="image" src="https://github.com/user-attachments/assets/0daf7e37-f6ab-4697-b5de-15244cf7488f" />

<!-- Chèn ảnh Summary Report Thread Group 2 tại đây -->
## 7. Thread Group 3 – Kịch bản tùy chỉnh

Mục tiêu:
Mô phỏng hành vi người dùng thực tế với thời gian chạy dài hơn.

Cấu hình:

Number of Threads (Users): 15

Ramp-up Period: 60 giây

Thời gian chạy: ~60 giây
<img width="1516" height="860" alt="image" src="https://github.com/user-attachments/assets/e6d00758-82e5-4c44-9f0c-e4296087120a" />

Phương thức:

HTTP GET đến 2 trang con khác nhau

Có cấu hình HTTP Header Manager:

User-Agent

Accept

Accept-Language

Lý do cấu hình User-Agent:
Một số website (như Wikipedia) yêu cầu User-Agent hợp lệ để phân biệt bot và người dùng thật.

<img width="1513" height="848" alt="image" src="https://github.com/user-attachments/assets/62fc264c-bc6c-41d0-af79-e31505ef73b9" />

<!-- Chèn ảnh View Results Tree Thread Group 3 tại đây -->
## 8. Phân tích kết quả kiểm thử

Các chỉ số được sử dụng để đánh giá:

Response Time: Thời gian phản hồi trung bình

Throughput: Số request xử lý mỗi giây

Error Rate: Tỷ lệ lỗi

Nhận xét chung:

Khi số lượng người dùng tăng, Response Time có xu hướng tăng

Website vẫn hoạt động ổn định với tải trung bình

Không ghi nhận lỗi nghiêm trọng trong quá trình kiểm thử

📸 Ảnh minh họa Summary Report tổng hợp:

<!-- Chèn ảnh Summary Report tổng hợp tại đây -->
## 9. Kết luận

Hoàn thành đầy đủ yêu cầu bài tập kiểm thử hiệu năng với JMeter

Hiểu cách tạo Test Plan, Thread Group và Listener

Biết cách xử lý các vấn đề phổ biến như:

Website chặn bot

Cấu hình User-Agent

Điều chỉnh Ramp-up để tránh quá tải

Có thể áp dụng JMeter để kiểm thử hiệu năng cho các dự án web thực tế
