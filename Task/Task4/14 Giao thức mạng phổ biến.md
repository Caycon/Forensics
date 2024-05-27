**1. TCP/IP**

* TCP/IP là một bộ giao thức truyền thông được sử dụng trên hầu hết các mạng máy tính hiện nay, bao gồm cả Internet. Bộ giao thức này được chia thành 4 tầng, mỗi tầng có một chức năng cụ thể:

    * Tầng vật lý (Physical Layer): Tầng này chịu trách nhiệm cho việc truyền tải dữ liệu ở dạng bit trên môi trường vật lý, chẳng hạn như cáp đồng trục, cáp xoắn đôi hoặc sóng vô tuyến.
    * Tầng liên kết dữ liệu (Data Link Layer): Tầng này chịu trách nhiệm cho việc tạo ra các khung dữ liệu (data frame) và truyền tải các khung dữ liệu đó trên mạng.
    * Tầng mạng (Network Layer): Tầng này chịu trách nhiệm cho việc định tuyến các gói tin (packet) đến đúng đích.
    * Tầng truyền vận (Transport Layer): Tầng này chịu trách nhiệm cho việc đảm bảo rằng dữ liệu được truyền tải một cách đáng tin cậy.

* **Hai giao thức quan trọng nhất trong bộ TCP/IP là TCP (Transmission Control Protocol) và IP (Internet Protocol)**.

    * **TCP** là một giao thức kết nối-định hướng (connection-oriented protocol), có nghĩa là nó tạo ra một kết nối giữa hai máy tính trước khi bắt đầu truyền tải dữ liệu. TCP đảm bảo rằng dữ liệu được truyền tải chính xác và không bị lỗi, đồng thời đảm bảo rằng dữ liệu được truyền tải đúng thứ tự.

    * TCP hoạt động như sau:

        1. Máy khách gửi một yêu cầu kết nối đến máy chủ.
        2. Máy chủ chấp nhận hoặc từ chối yêu cầu kết nối.
        3. Nếu máy chủ chấp nhận yêu cầu kết nối, thì hai máy tính sẽ bắt đầu truyền tải dữ liệu.
        4. Khi truyền tải dữ liệu kết thúc, thì hai máy tính sẽ ngắt kết nối.

    * TCP được sử dụng cho các ứng dụng yêu cầu độ tin cậy cao, chẳng hạn như truyền tải tệp, email và web.

    * **IP** là một giao thức phi kết nối-định hướng (connectionless protocol), có nghĩa là nó không tạo ra một kết nối giữa hai máy tính trước khi bắt đầu truyền tải dữ liệu. IP chỉ chịu trách nhiệm cho việc định tuyến các gói tin đến đúng đích.

    * IP hoạt động như sau:

        1. Máy khách tạo ra một gói tin.
        2. Máy khách gửi gói tin đến máy chủ.
        3. Máy chủ nhận gói tin và định tuyến gói tin đến đích cuối cùng.

    * IP được sử dụng cho tất cả các giao thức ứng dụng trong bộ TCP/IP, bao gồm TCP, UDP, HTTP, FTP, SMTP,...
-------
**2. UDP**

* **UDP (User Datagram Protocol)** là một giao thức không kết nối-định hướng tương tự như IP. UDP không đảm bảo rằng dữ liệu được truyền tải chính xác hoặc không bị lỗi, cũng không đảm bảo rằng dữ liệu được truyền tải đúng thứ tự. UDP thường được sử dụng cho các ứng dụng yêu cầu thời gian thực, chẳng hạn như VoIP hoặc trò chơi trực tuyến.

* UDP hoạt động như sau:
    1. Máy khách tạo ra một gói tin.
    2. Máy khách gửi gói tin đến máy chủ.
    3. Máy chủ nhận gói tin và xử lý gói tin.

* UDP không đảm bảo rằng dữ liệu được truyền tải đến đích cuối cùng. Nếu gói tin bị lỗi hoặc bị mất, thì máy chủ sẽ không biết.
-------
**3. HTTP**

* **HTTP (Hypertext Transfer Protocol)** là một giao thức ứng dụng được sử dụng để truyền tải dữ liệu trên World Wide Web. HTTP được sử dụng để truyền tải các trang web, hình ảnh, âm thanh và video.

* HTTP hoạt động như sau:
    1. Máy khách gửi một yêu cầu HTTP đến máy chủ.
    2. Máy chủ trả lời yêu cầu HTTP.

* Yêu cầu HTTP có thể là một yêu cầu GET hoặc POST. Yêu cầu GET được sử dụng để truy cập một tài nguyên trên máy chủ, chẳng hạn như một trang web hoặc một hình ảnh. Yêu cầu POST được sử dụng để gửi dữ liệu đến máy chủ, chẳng hạn như dữ liệu đăng ký hoặc dữ liệu mua hàng.

* HTTP sử dụng TCP làm giao thức vận chuyển.
-------
**4. HTTPS**

* **HTTPS** là một phiên bản an toàn của HTTP. HTTPS sử dụng mã hóa để bảo vệ dữ liệu được truyền tải giữa máy khách và máy chủ.

* HTTPS sử dụng một giao thức mã hóa được gọi là TLS (Transport Layer Security) hoặc SSL (Secure Sockets Layer). TLS và SSL đều cung cấp tính bảo mật cho dữ liệu được truyền tải bằng cách mã hóa dữ liệu đó.

* HTTPS được sử dụng cho các ứng dụng yêu cầu bảo mật cao, chẳng hạn như các trang web thương mại điện tử, các trang web ngân hàng và các trang web cung cấp thông tin nhạy cảm.

* **Cách thức hoạt động của HTTPS**

* HTTPS hoạt động như sau:
    1. Máy khách gửi yêu cầu HTTP đến máy chủ.
    2. Máy chủ trả lời yêu cầu HTTP của máy khách bằng một chứng chỉ TLS/SSL.
    3. Máy khách sử dụng chứng chỉ TLS/SSL để xác thực máy chủ.
    4. Nếu máy khách tin cậy máy chủ, thì máy khách sẽ tạo một khóa mã hóa.
    5. Máy khách và máy chủ sử dụng khóa mã hóa để mã hóa và giải mã dữ liệu được truyền tải.

* **Các lợi ích của HTTPS**
    * HTTPS cung cấp một số lợi ích, bao gồm:
        * Bảo vệ dữ liệu khỏi bị đánh cắp hoặc thay đổi.
        * Bảo vệ quyền riêng tư của người dùng.
        * Tạo niềm tin cho người dùng.

* **Các nhược điểm của HTTPS**
    * HTTPS cũng có một số nhược điểm, bao gồm:
        * HTTPS có thể làm chậm tốc độ truyền tải dữ liệu.
        * HTTPS yêu cầu máy chủ có chứng chỉ TLS/SSL.

* HTTPS là một giao thức quan trọng giúp bảo vệ dữ liệu được truyền tải trên Internet. HTTPS được sử dụng cho nhiều ứng dụng quan trọng, chẳng hạn như thương mại điện tử và ngân hàng.
-------
**5. FTP**

* **FTP (File Transfer Protocol)** là một giao thức ứng dụng được sử dụng để truyền tải tệp giữa các máy tính trên mạng. FTP sử dụng TCP làm giao thức vận chuyển.

* FTP hoạt động như sau:
    1. Máy khách kết nối với máy chủ FTP.
    2. Máy khách gửi yêu cầu tải xuống hoặc tải lên tệp.
    3. Máy chủ đáp ứng yêu cầu của máy khách.

* FTP có hai chế độ hoạt động chính: chế độ thụ động và chế độ chủ động.
    * **Chế độ thụ động:** Máy khách sẽ yêu cầu máy chủ mở một cổng TCP để truyền tải dữ liệu.
    * **Chế độ chủ động:** Máy chủ sẽ mở một cổng TCP để truyền tải dữ liệu.
-------
**6. SMTP**

* **SMTP (Simple Mail Transfer Protocol)** là một giao thức ứng dụng được sử dụng để gửi email. SMTP sử dụng TCP làm giao thức vận chuyển.

* SMTP hoạt động như sau:
    1. Máy chủ gửi một yêu cầu nhận email từ máy khách.
    2. Máy khách gửi email đến máy chủ.
    3. Máy chủ gửi email đến máy chủ nhận.
-------
**7. DNS**

* **DNS (Domain Name System)** là một hệ thống phân giải tên miền. DNS được sử dụng để ánh xạ tên miền sang địa chỉ IP.

* DNS hoạt động như sau:
    1. Máy khách gửi yêu cầu phân giải tên miền đến máy chủ DNS.
    2. Máy chủ DNS trả lời yêu cầu phân giải tên miền.
-------
**8. DHCP**

* **DHCP (Dynamic Host Configuration Protocol)** là một giao thức được sử dụng để cấp địa chỉ IP và các thông tin cấu hình mạng khác cho các máy tính trên mạng.

* DHCP hoạt động như sau:
    1. Máy khách gửi yêu cầu cấp địa chỉ IP đến máy chủ DHCP.
    2. Máy chủ DHCP cấp địa chỉ IP và các thông tin cấu hình mạng khác cho máy khách.
-------
**9. SSH**

* **SSH (Secure Shell)** là một giao thức ứng dụng được sử dụng để truy cập từ xa an toàn. SSH sử dụng mã hóa để bảo vệ dữ liệu được truyền tải giữa máy khách và máy chủ.

* SSH hoạt động như sau:
    1. Máy khách kết nối với máy chủ SSH.
    2. Máy khách và máy chủ sử dụng mã hóa để xác thực lẫn nhau.
    3. Máy khách và máy chủ bắt đầu truyền tải dữ liệu được mã hóa.
-------
**10. VPN**

* **VPN (Virtual Private Network)** là một mạng riêng ảo. VPN cho phép tạo một kết nối mạng an toàn giữa hai máy tính qua một mạng công cộng, chẳng hạn như Internet.

* VPN hoạt động như sau:
    1. Máy khách kết nối với máy chủ VPN.
    2. Máy khách và máy chủ sử dụng mã hóa để xác thực lẫn nhau.
    3. Máy khách và máy chủ bắt đầu truyền tải dữ liệu được mã hóa.
-------
**11. SNMP**

* **SNMP (Simple Network Management Protocol)** là một giao thức quản lý mạng. SNMP được sử dụng để giám sát và quản lý các thiết bị mạng.

* SNMP hoạt động như sau:
    1. Máy chủ quản lý gửi yêu cầu SNMP đến thiết bị mạng.
    2. Thiết bị mạng trả lời yêu cầu SNMP.
-------
**12. NTP**

* **NTP (Network Time Protocol)** là một giao thức đồng bộ hóa thời gian. NTP được sử dụng để đồng bộ hóa thời gian giữa các máy tính trên mạng.

* NTP hoạt động như sau:
    1. Máy khách gửi yêu cầu NTP đến máy chủ NTP.
    2. Máy chủ NTP trả lời yêu cầu NTP.
--------
**13. RIP**

* **RIP (Routing Information Protocol)** là một giao thức định tuyến. RIP được sử dụng để định tuyến các gói tin trên mạng IP.

* RIP hoạt động như sau:
    1. Máy chủ định tuyến gửi thông tin định tuyến đến các máy chủ định tuyến khác.
    2. Các máy chủ định tuyến cập nhật thông tin định tuyến của họ.
-------
**14. OSPF**

* **OSPF (Open Shortest Path First)** là một giao thức định tuyến nâng cao. OSPF được sử dụng để định tuyến các gói tin trên mạng IP.TCbn

* OSPF hoạt động như sau:
    1. Các máy chủ định tuyến trao đổi thông tin định tuyến với nhau.
    2. Các máy chủ định tuyến sử dụng thuật toán Shortest Path First (SPF) để tính toán đường đi ngắn nhất đến các đích.
