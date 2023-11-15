# PNG
-------
## Khái niệm:
- `PNG` là từ viết tắt của `Portable Network Graphics` là một dạng hình ảnh sử dụng phương pháp nén dữ liệu mới - không làm mất đi dữ liệu gốc. PNG được tạo ra nhằm cải thiện và thay thế định dạng ảnh GIF với một định dạng hình ảnh không đòi hỏi phải có giấy phép sáng chế khi sử dụng. PNG được hỗ trợ bởi thư viện tham chiếu `libpng`, một thư viện nền tảng độc lập bao gồm các hàm của C để quản lý các hình ảnh PNG.

- Những tập tin `PNG` thường có phần mở rộng là `PNG` và `png` đã được gán kiểu chuẩn `MIME` là `image/png`
-------
## Thông tin kỹ thuật:
- Phần đầu của `png`:
    - Một tập tin PNG bao gồm 8-byte ký hiệu `89 50 4E 47 0D 0A 1A 0A` được viết trong hệ thống có cơ số 16, chứa các chữ "PNG" và 2 dấu xuống dòng [Tham khảo thêm tại đây](http://www.libpng.org/pub/png/spec/1.1/PNG-Rationale.html#R.PNG-file-signature).
    - 8-byte `89 50 4E 47 0D 0A 1A 0A` ở phần đầu chính là đại diện cho file `png` nên nếu 8-byte đầu này bị thay đổi sẽ dẫn đến việc mở file bị thất bại.

    ![image](https://github.com/Caycon/Forensics/assets/97203151/b0de0eff-4927-41f5-92a1-459d52224845)
- Thành phần cơ bản của `png` khi decode:
    - `IHDR`: phải là thành phần đầu tiên, nó chứa đựng header
    - `PLTE`: chứa đựng bảng màu (danh sách các màu)
    - `IDAT`: chứa đựng ảnh. Ảnh này có thể được chia nhỏ chứa trong nhiều phần IDAT. Điều này làm tăng kích cỡ của tệp lên một ít nhưng nó làm cho việc phát sinh ảnh PNG mượt hơn (streaming manner).
    - `IEND`: đánh dấu điểm kết thúc của ảnh.
-------
