# Aes-Decrypt

## Mã hóa, giải mã file bằng thuật toán mã hoá AES

Là một trang web giúp mọi người mã hoá dữ liệu và giải mã dữ liệu bằng thuật toán mã hoá AES.
* Mã hóa các file nhạy cảm trước khi lưu trữ hoặc chia sẻ.
* Giải mã các file đã được mã hóa bằng cùng một khóa bí mật.
* Sử dụng AES (Advanced Encryption Standard) ở chế độ ECB với khóa được tạo từ hàm băm SHA-256 của mật khẩu người dùng.
---
## Tính năng nổi bật

* **Giao diện Web thân thiện:** Dễ dàng tải file lên, nhập khóa và chọn chế độ (mã hóa/giải mã).
* **Mã hóa AES:** Sử dụng thuật toán mã hóa đối xứng mạnh mẽ AES.
* **Chuẩn hóa Khóa với SHA-256:** Khóa do người dùng cung cấp được băm bằng SHA-256 để tạo ra một khóa 32-byte (256-bit) phù hợp cho AES-256.
* **Tải file kết quả:** Sau khi xử lý, file đã mã hóa (thường có đuôi `.aes`) hoặc giải mã (thường có đuôi `.txt` hoặc phần mở rộng gốc nếu có thể xác định) sẽ tự động được tải xuống.
* **Triển khai nhanh với Ngrok:** Tích hợp `pyngrok` để tạo đường hầm công khai đến ứng dụng Flask chạy cục bộ, tiện lợi cho việc demo hoặc sử dụng tạm thời.
* **Xử lý lỗi cơ bản:** Hiển thị thông báo lỗi nếu quá trình mã hóa/giải mã gặp sự cố (ví dụ: sai khóa khi giải mã).

---

## Giao diện web

<p align="center">  
   <img src="Picture/Ảnh chụp màn hình (4).png" alt="Ảnh minh họa" width="850" height="480">  
</p>  

---

## Cách sử dụng

* Bấm "Chọn" dữ liệu muốn mã hoá vô.
* Nhập khoá mã cho file.
* Chọn "Mã Hoá" hoặc "Giải mã".
* Nhấn "Thực Hiện".
  → Đã thành công mã hoá file, file được tải tự động vào máy.

---

## Kỹ thuật sử dụng

* **Ngôn ngữ:** Python 3
* **Framework Web:** Flask
* **Thư viện mã hóa:** PyCryptodome (`Crypto.Cipher.AES`, `Crypto.Util.Padding`)
* **Thư viện băm:** hashlib (SHA-256)
* **Tạo đường hầm:** pyngrok
* **Giao diện:** HTML, CSS
