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
