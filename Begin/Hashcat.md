# Hashcat
-------
## Introduction:
- `Hashcat` là công cụ dò tìm pass dựa trên mã hash đã biết. Ưu điểm của hashcat là có thể crack khá là nhanh và ổn định.
- Cơ chế hoạt động: dò tìm pass dựa trên mà hash đã biết(brute force).
-------
## Install:
- [Install tại đây](https://hashcat.net/hashcat/).
- Hoặc install qua `linus` với lệnh sau: `sudo apt install hashcat`.
-------
## Demo:
- Ta sẽ crack file [Sceret](https://github.com/Caycon/Forensics/blob/main/Begin/Sceret) với pass là `PASS`.
- Đầu tiên ta sử dụng lệnh `7z2john` để chuyển file về mã hash. Do tôi sử dụng `7zip` để nén file.
- ![image](https://github.com/Caycon/Forensics/assets/97203151/00f62a2c-f545-4e91-9274-540dac4e372b)
- Tiếp theo ta sử dụng `hashcat` để dò pass dựa trên mã hash mà ta thu được sau khi chuyển file về mã hash.
- Lưu ý sử dụng lệnh `hashcat --hashes-example` để lấy mode file bạn cần hashcat hoặc có thể lên gg search. 
- Đây là [clip](https://www.bing.com/videos/riverview/relatedvideo?q=crack+pass+7zip+by+hashcat&mid=9C026E1EA480B9BF8F4A9C026E1EA480B9BF8F4A&FORM=VIRE) hướng dẫn mà các bạn có thể tham khảo.
