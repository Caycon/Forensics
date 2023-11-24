# Pkcrack:
- [Tham khảo tại đây](https://github.com/keyunluo/pkcrack#readme).
- `Pkcrack` là thuật toán attack nhằm crack dữ liệu. Để làm được điều này bạn cần có 2 file:
    - File thứ nhất chứa file `zip` mà bạn muốn giải mã.
    - File thứ hai chứa ít nhất 1 trong các tệp được lưu trữ được mã hóa ở dạng `unencrypted`. File này cũng phải được nén bằng cùng 1 phương pháp với file thứ nhất.
- Ta sẽ demo attack [file](https://github.com/Caycon/Forensics/blob/main/Begin/pkcrack-1.2.2.tar.gz) sau.
- Ta sử dụng lệnh ` pkcrack -C encrypted-ZIP -c ciphertextname -P plaintext-ZIP -p plaintextname -d decrypted_file -a`. Với:
    - encrypted-ZIP: là tên (và đường dẫn) của kho lưu trữ ZIP được mã hóa.
    - ciphertextname: là tên của tệp trong kho lưu trữ mà bạn có - bản rõ
    - plaintext-ZIP: là tên (đường dẫn) của kho lưu trữ ZIP chứa bản rõ được nén.
    - plaintextname: là tên của tệp trong kho lưu trữ có chứa bản rõ đã biết.
    - decrypted_file: là tên của một tệp mà kho lưu trữ được giải mã sẽ được ghi.
- Vd: Ta có 2 file zip là `Demo.zip` và `Public.zip`, file chứa nd chung của 2 file zip là `pubilc.txt`. Lưu ý là file `public.txt` phải có nội dung đủ dài.
- Lệnh ta sử dụng như sau:
`../bin/./pkcrack -C /mnt/c/Users/nbcta/OneDrive/Desktop/NewTest/Demo.zip -c Public.txt -P /mnt/c/Users/nbcta/OneDrive/Desktop/Public.zip -p Public.txt -d output.zip -a`
- Hãy thay thế đường dẫn trên về file nơi bạn lưu trữ.
![image](https://github.com/Caycon/Forensics/assets/97203151/ba60a3b1-33fd-4aa7-87f3-6c631f7a3a8b)
- Sau khi đã chạy thành công thì ta giải nén file `output.zip` như bình thường. Còn nếu muốn mở file zip ban đầu có mật khẩu thì ta sẽ tìm hiểu tiếp `bkcrack` ở phần tiếp theo.
