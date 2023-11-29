# Mô hình OSI

Mô hình OSI (Open Systems Interconnection model) là một mô hình tham chiếu kết nối các hệ thống mở, được phát triển bởi Tổ chức Quốc tế về Tiêu chuẩn hóa (ISO). Mô hình này chia quá trình truyền thông mạng thành 7 lớp, mỗi lớp thực hiện một chức năng cụ thể.

## Lịch sử

Mô hình OSI được phát triển bởi ISO trong những năm 1970 để cung cấp một mô hình tham chiếu chung cho các hệ thống mạng. Mô hình này được thiết kế để giúp các nhà phát triển mạng hiểu rõ hơn về quá trình truyền thông mạng và đảm bảo rằng các hệ thống mạng khác nhau có thể giao tiếp với nhau.

## Khái niệm cơ bản

Mô hình OSI dựa trên nguyên tắc tầng cấp, trong đó quá trình truyền thông mạng được chia thành các lớp riêng biệt. Mỗi lớp thực hiện một chức năng cụ thể và giao tiếp với các lớp khác thông qua các giao diện.

## Các lớp của mô hình OSI

Mô hình OSI có 7 lớp, được phân chia từ trên xuống dưới như sau:

* **Lớp ứng dụng (Application layer)**: Cung cấp các dịch vụ cho các ứng dụng người dùng, chẳng hạn như gửi email, duyệt web hoặc chia sẻ tệp.
* **Lớp trình bày (Presentation layer)**: Chuyển đổi dữ liệu giữa các ứng dụng người dùng ở các định dạng khác nhau.
* **Lớp phiên (Session layer)**: Cung cấp các dịch vụ quản lý phiên, chẳng hạn như bắt đầu, tạm dừng và kết thúc các cuộc hội thoại giữa các ứng dụng.
* **Lớp vận chuyển (Transport layer)**: Đảm bảo rằng dữ liệu được truyền từ máy tính này sang máy tính khác một cách đáng tin cậy.
* **Lớp mạng (Network layer)**: Cung cấp các dịch vụ định tuyến dữ liệu qua mạng.
* **Lớp liên kết dữ liệu (Data link layer)**: Đảm bảo rằng dữ liệu được truyền từ máy tính này sang máy tính khác trên cùng một mạng vật lý.
* **Lớp vật lý (Physical layer)**: Cung cấp các dịch vụ giao tiếp dữ liệu trên mạng vật lý, chẳng hạn như cáp Ethernet hoặc cáp quang.

## Chức năng của các lớp trong mô hình OSI

Mỗi lớp của mô hình OSI thực hiện một chức năng cụ thể trong quá trình truyền thông mạng. Dưới đây là một số chức năng chính của các lớp:

* **Lớp ứng dụng:** Cung cấp các dịch vụ cho các ứng dụng người dùng, chẳng hạn như gửi email, duyệt web hoặc chia sẻ tệp. Các dịch vụ này có thể bao gồm:
    * Truy cập dữ liệu
    * Cấu hình mạng
    * Quản lý tài nguyên
* **Lớp trình bày:** Chuyển đổi dữ liệu giữa các ứng dụng người dùng ở các định dạng khác nhau. Ví dụ: nếu một ứng dụng gửi dữ liệu ở định dạng Unicode, lớp trình bày sẽ chuyển đổi dữ liệu đó sang định dạng ASCII để nó có thể được truyền qua mạng. Các dịch vụ này có thể bao gồm:
    * Mã hóa dữ liệu
    * Giải mã dữ liệu
    * Nén dữ liệu
    * Giải nén dữ liệu
* **Lớp phiên:** Cung cấp các dịch vụ quản lý phiên, chẳng hạn như bắt đầu, tạm dừng và kết thúc các cuộc hội thoại giữa các ứng dụng. Các dịch vụ này có thể bao gồm:
    * Tạo phiên
    * Quản lý phiên
    * Kết thúc phiên
* **Lớp vận chuyển:** Đảm bảo rằng dữ liệu được truyền từ máy tính này sang máy tính khác một cách đáng tin cậy. Lớp vận chuyển cung cấp các dịch vụ như phân mảnh và ghép lại dữ liệu, kiểm soát luồng dữ liệu và xác nhận dữ liệu. Các dịch vụ này có thể bao gồm:
    * Cung cấp dịch vụ giao tiếp đáng tin cậy
    * Phân mảnh và ghép lại dữ liệu
    * Kiểm soát luồng dữ liệu
    * Xác nhận dữ liệu
* **Lớp mạng:** Cung cấp các dịch vụ định tuyến dữ liệu qua mạng. Lớp mạng chịu trách nhiệm chọn đường tốt nhất để truyền dữ liệu từ một nguồn đến đích. Các dịch vụ này có thể bao gồm:
    * Định tuyến dữ liệu
    * Chuyển đổi địa chỉ mạng
    * Chuyển đổi giao thức
* **Lớp liên kết dữ liệu (Data link layer)**: Đảm bảo rằng dữ liệu được truyền từ máy tính này sang máy tính khác trên cùng một mạng vật lý. Lớp liên kết dữ liệu cung cấp các dịch vụ như kiểm soát lỗi, xác thực và định dạng dữ liệu. Các dịch vụ này có thể bao gồm:

* **Kiểm soát lỗi:** Đảm bảo rằng dữ liệu được truyền một cách chính xác, không bị lỗi.
* **Xác thực:** Đảm bảo rằng dữ liệu được truyền từ một nguồn đáng tin cậy.
* **Định dạng dữ liệu:** Chuyển đổi dữ liệu thành các đơn vị dữ liệu nhỏ hơn, dễ dàng truyền qua mạng vật lý.

* **Lớp vật lý (Physical layer)**: Cung cấp các dịch vụ giao tiếp dữ liệu trên mạng vật lý, chẳng hạn như cáp Ethernet hoặc cáp quang. Lớp vật lý chịu trách nhiệm chuyển đổi dữ liệu thành các tín hiệu điện hoặc quang học có thể được truyền qua mạng vật lý. Các dịch vụ này có thể bao gồm:

* **Giao tiếp dữ liệu:** Chuyển đổi dữ liệu thành các tín hiệu điện hoặc quang học.
* **Tốc độ truyền dữ liệu:** Xác định tốc độ truyền dữ liệu trên mạng vật lý.
* **Kênh truyền dữ liệu:** Xác định loại kênh truyền dữ liệu, chẳng hạn như cáp Ethernet hoặc cáp quang.

## Ứng dụng của mô hình OSI

Mô hình OSI được sử dụng trong nhiều lĩnh vực khác nhau, bao gồm:

* **Khoa học máy tính:** Mô hình OSI được sử dụng để dạy về truyền thông mạng và thiết kế mạng.
* **Kỹ thuật mạng:** Mô hình OSI được sử dụng để thiết kế và triển khai mạng.
* **Quản lý mạng:** Mô hình OSI được sử dụng để quản lý và bảo trì mạng.

## Ưu điểm của mô hình OSI

Mô hình OSI có một số ưu điểm sau:

* **Cung cấp một mô hình tham chiếu chung cho các hệ thống mạng.**
* **Giúp các nhà phát triển mạng hiểu rõ hơn về quá trình truyền thông mạng.**
* **Đảm bảo rằng các hệ thống mạng khác nhau có thể giao tiếp với nhau.**

## Nhược điểm của mô hình OSI

Mô hình OSI cũng có một số nhược điểm sau:

* **Quá phức tạp và khó triển khai.**
* **Không được sử dụng rộng rãi trong thực tế.**

## Nhìn chung

* Mô hình OSI là một mô hình tham chiếu quan trọng để hiểu cách thức hoạt động của truyền thông mạng. Mô hình này chia quá trình truyền thông mạng thành 7 lớp, mỗi lớp thực hiện một chức năng cụ thể.
