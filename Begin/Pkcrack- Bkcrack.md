# Pkcrack:
- [Tham khảo tại đây](https://github.com/keyunluo/pkcrack#readme).
- `Pkcrack` là thuật toán attack nhằm crack dữ liệu. Để làm được điều này bạn cần có 2 file:
    - File thứ nhất chứa file `zip` mà bạn muốn giải mã.
    - File thứ hai chứa ít nhất 1 trong các tệp được lưu trữ được mã hóa ở dạng `unencrypted`. File này cũng phải được nén bằng cùng 1 phương pháp với file thứ nhất.
- Ta sẽ demo attack file [Demo](https://github.com/Caycon/Forensics/blob/main/Begin/Demo.zip) dựa vào file [Public.zip](https://github.com/Caycon/Forensics/blob/main/Begin/Public.zip) sau.
- Ta sử dụng lệnh ` pkcrack -C encrypted-ZIP -c ciphertextname -P plaintext-ZIP -p plaintextname -d decrypted_file -a`. Với:
    - encrypted-ZIP: là tên (và đường dẫn) của kho lưu trữ ZIP được mã hóa.
    - ciphertextname: là tên của tệp trong kho lưu trữ mà bạn có - bản rõ
    - plaintext-ZIP: là tên (đường dẫn) của kho lưu trữ ZIP chứa bản rõ được nén.
    - plaintextname: là tên của tệp trong kho lưu trữ có chứa bản rõ đã biết.
    - decrypted_file: là tên của một tệp mà kho lưu trữ được giải mã sẽ được ghi.
- Vd: Ta có 2 file zip là `Demo.zip` và `Public.zip`, file chứa nd chung của 2 file zip là `pubilc.txt`. Lưu ý là file `public.txt` phải có nội dung đủ dài.
- Lệnh ta sử dụng như sau:
- ` ./pkcrack -C Demo.zip -c Public.txt -P Public.zip -p Public.txt -d decrypt.zip -a`. Hoặc: `../bin/./pkcrack -C /mnt/c/Users/nbcta/OneDrive/Desktop/NewTest/Demo.zip -c Public.txt -P /mnt/c/Users/nbcta/OneDrive/Desktop/Public.zip -p Public.txt -d output.zip -a`(Thay thế đường dẫn trên về file nơi bạn lưu trữ.)
![image](https://github.com/Caycon/Forensics/assets/97203151/11588a4d-fc10-48ff-ba38-01dda59a6bcc)
- Sau khi đã chạy thành công thì ta giải nén file `output.zip` như bình thường. Còn nếu muốn mở file zip ban đầu có mật khẩu thì ta sẽ tìm hiểu tiếp `bkcrack` ở phần tiếp theo.
-------
# Bkcrack:
- [Tham khảo tại đây](https://github.com/kimci86/bkcrack).
- `Bkcrack` là một công cụ dòng lệnh thực hiện cuộc tấn công văn bản thuần túy đã biết này. Các tính năng chính là:
    - Khôi phục trạng thái nội bộ từ bản mã và bản rõ.
    - Thay đổi mật khẩu của kho lưu trữ ZIP bằng trạng thái nội bộ.
    - Khôi phục mật khẩu ban đầu từ trạng thái nội bộ.
- Với `Bkcrack` ta cần biết ít nhất `12 bytes` có trong file.
- Ta sẽ thử demo với file demo của `bkcrack`:
- ![image](https://github.com/Caycon/Forensics/assets/97203151/45643685-929d-4395-b899-16b047cd0dfc)
- ![image](https://github.com/Caycon/Forensics/assets/97203151/6569bef1-061d-4d38-8be4-8464440e372d)
- ### Tiếp theo nếu chúng ta có thể đặt mật khẩu mới hoặc giải mã file hoặc khôi phục mật khẩu ban đầu:
    - #### Đặt mật khẩu mới:
        - ![image](https://github.com/Caycon/Forensics/assets/97203151/ee42eb41-e1b1-44bc-95c6-2086f9feb8c2)
        - Với Test.zip là tên file và pass là Test
    - #### Giải mã file:
        - Ta có thể giải mã từng file vd như:
        - ![image](https://github.com/Caycon/Forensics/assets/97203151/b4014848-46db-4025-8412-063968831754)
        - Với decrypt.svg là file ghi decrypt, spiral.svg là file trong zip.
    - #### Khôi phục mật khẩu:
        - ![image](https://github.com/Caycon/Forensics/assets/97203151/d6622d51-948d-4e21-baee-58f404da4d6d)
        - Đây là 1 số ký hiệu tương ứng với các loại kiểu dữ liệu có trong pass bạn cần chọn để crack hoặc có thể để all bytes:
        - ![image](https://github.com/Caycon/Forensics/assets/97203151/d26e36ec-5936-4072-9271-dba6a26ab034)
        - Tương tự ta có thể tim thấy pass của bài phần `Pkcrack`:
        - ![image](https://github.com/Caycon/Forensics/assets/97203151/f177602b-d42c-4056-9da7-559c89de4cf4)
# Demo:
- Ta sẽ demo crack thông tin [file](https://github.com/Caycon/Forensics/blob/main/Begin/Keep_Out.zip) sau.
- Sau khi tải về ta cần pass để giải nén và do không biết pass nhưng chúng ta cần phải biết 1 số thông tin của các tập tin có trong đó nên ta sẽ thử khai thác ở điểm này.
- ![image](https://github.com/Caycon/Forensics/assets/97203151/c8d94fe5-11e8-476e-b213-ddd4b82f067b)
- Theo theo ta sẽ hash pass bằng john:
- ![image](https://github.com/Caycon/Forensics/assets/97203151/9f77f6c7-0a5e-4f0a-a69a-9e7187332893)
- Do chờ quá lâu nên ta sẽ thử hash bằng `rockyou.txt`:
- ![image](https://github.com/Caycon/Forensics/assets/97203151/52ff46d8-d001-430e-adda-775268a64f49)
- Ngay lập tức ta thu được pass:)))))).
- Giải nén với pass là: `MANCHESTERUNITED`.
- Ta thu được 3 file trong đó có có 2 file .txt( 1 file có pass, 1 file không có pass), 1 file zip. Điều này giống với kịch bản chúng ta đã demo với `bkcrack` và `pkcrack` ta sẽ thử crack theo hướng này xem sao.
- Nhưng trước tiên ta cứ thử với `rockyou.txt` đã:
- ![image](https://github.com/Caycon/Forensics/assets/97203151/342cfa74-e2cd-4825-9879-b54e279a9e9e)
- Nhận thấy không dò được pass và trong file zip kia có 1 file trùng tên với file .txt bên ngoài đó là `bookmarks.txt`. Ta sẽ thử `pkcrack`.
- Sử dụng `pkcrack`:
- ![image](https://github.com/Caycon/Forensics/assets/97203151/9752bbcf-27b7-442e-b1d3-10e69a873a6f)
- Lưu ý là phải nén file dưới dạng `zipcrypto` nếu không kết quả sẽ ntn:
- ![image](https://github.com/Caycon/Forensics/assets/97203151/fb046a04-871c-4b56-933a-fb4b763a93ba)
- Ta thu được 5 file, lần lượt check thì ta thu được flag ngay tại file đầu tiên là file pdf:
- ![image](https://github.com/Caycon/Forensics/assets/97203151/18184524-1607-406d-ad67-19b917edccc9)



