# Johntheripper
-------
## Introduction:
- `John the Ripper` là phần mềm crack password free. Đây là một trong những chương trình kiểm tra và phá mật khẩu được sử dụng thường xuyên nhất vì nó kết hợp một số trình bẻ khóa mật khẩu vào một gói, tự động phát hiện các loại băm mật khẩu và bao gồm một trình bẻ khóa có thể tùy chỉnh. Nó có thể chạy trên các định dạng mật khẩu được mã hóa khác nhau bao gồm một số loại băm mật khẩu crypt thường thấy nhất.
- `John the Ripper` sử dụng phương pháp brute force để crack nên sẽ tốn khá nhiều thời gian vì thế nó chỉ thích hợp để crack các pass đơn giản.
-------
## Install:
- [Install tại đây](https://www.openwall.com/john/).
- Hoặc install qua `linux` với lệnh sau: `apt install John`.
-------
## Demo:
  - Ta sẽ thử crack 2 file sau: [Sceret.rar](https://github.com/Caycon/Forensics/blob/main/Begin/Sceret.rar) với pass là `DeMoDeMo` và [Sceret](https://github.com/Caycon/Forensics/blob/main/Begin/Sceret) với pass là `PASS`.
  - Đầu tiên ta cần học sử dụng các lệnh của `Johntheripper` tại [link sau](https://www.freecodecamp.org/news/crack-passwords-using-john-the-ripper-pentesting-tutorial/).
  - Sceret.rar:
    - Đầu tiên ta sử dụng lệnh `rar2john` để chuyển file về mã hash. Có thể sử dụng `zip2john` nếu đó là file zip.
    - ![image](https://github.com/Caycon/Forensics/assets/97203151/b92c341a-ed46-429c-afb3-1b113c70ffda)
    - Tiếp theo sử dụng lệnh `john` để brute force pass.
    - ![image](https://github.com/Caycon/Forensics/assets/97203151/832611a8-52c7-4627-bc17-56f73a5dbecb)
    - Do mình để pass hơi phức tạp nên brute force lâu nha mng:((.
  - Sceret:
    - Ta sử dụng lệnh `7z2john` để chuyển file về mã hash. Do tôi sử dụng `7zip` để nén file.
    - ![image](https://github.com/Caycon/Forensics/assets/97203151/00f62a2c-f545-4e91-9274-540dac4e372b)
    - Tiếp theo sử dụng lệnh `john` để brute force pass.
    - ![image](https://github.com/Caycon/Forensics/assets/97203151/5fb5b50d-2193-4348-8e90-90a1ca0eae49)
    - Sau khi có pass là: `PASS` thì ta thực hiện giải nén file và lấy được dữ liệu ở trong.
