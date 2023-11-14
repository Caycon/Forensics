# Forensics:
--------------------
## Introduction:
- `Forensics`: đây là tính từ có nghĩa là, pháp y, liên quan đến các phương pháp khoa học để giải quyết tội phạm, liên quan đến việc kiểm tra các đồ vật hoặc chất có liên quan đến tội phạm. Trong lĩnh vực an toàn thông tin, Forensics hay còn gọi là điều tra số là công việc phát hiện, bảo vệ và phân tích thông tin được lưu trữ, truyền tải hoặc được tạo ra bởi một máy tính hoặc mạng máy tính, nhằm đưa ra các suy luận hợp lý để tìm nguyên nhân, giải thích các hiện tượng trong quá trình điều tra.   
- `Forensics sciene`: là khoa học pháp y xuất phát từ lĩnh vực y tế từ thế kỷ 18 và liên quan đến điều tra pháp y.
- `Cyber Forensics`: là khoa học liên quan đến các kỹ thuật được sử dụng để theo dõi `footprints` được để lại sau một cuộc tấn công mạng. `Cyber forensics` được liên kết trực tiếp với tội phạm an ninh mạng nào bị mất và khôi phục dữ liệu. Một số vd như:
    - `Forged digital signatures`: Điều tra chữ ký số giả mạo.
    - `The authenticity of images`: Tính xác thực của hình ảnh.
    - `Analysis of malicious software`: Phân tích phân mềm độc hại.
- `Digital Forensics`: là một nhánh của khoa học điều tra, với mục đích truy tìm và phân tích các tài liệu chứa trong các thiết bị số, thường gọi là “tài liệu số”, để tìm ra các bằng chứng số. 
--------------------
## Phạm vi:
- `Forensics`: có thể bao gồm phân tích định dạng tập tin,  ẩn giấu thông tin (steganography), phân tích kết xuất bộ nhớ (memory dump), hoặc phân tích gói tin mạng bắt được (network forensics). Bất kỳ thử thách (challenge) nào để kiểm tra và xử lý một phần thông tin ẩn trong các tập tin dữ liệu.
- Ngoài ra, một số mảng Forensics có thể được kể đến như là:
    - `Memory forensics`: Điều tra bộ nhớ.
    - `Steganography`: Ẩn dấu thông tin.
    - `Hard Drive Forensics`: Điều tra bộ nhớ lưu trữ.
    - `Network forensics`: Điều tra mạng.
    - `Application forensics`: Điều tra ứng dụng.
    - `Malware forensics`: Điều tra lây nhiễm mã độc.
--------------------
## File format:
- Nhìn chung đây là định dạng của các loại file như:
    - File hình ảnh `png`, `tiff`, `jmg`,...
    - File âm thanh `mp3`,...
    - File cơ sở dữ liệu `sql`, `db`,....
--------------------
## Steganography:
- `Steganography`: Được gọi là kỹ thuật giấu tin hay kỹ thuật ẩn mã là nghệ thuật của khoa học về việc biểu diễn thông tin trong một thông điệp hoặc vật thể khác, sao chbo sự hiện diện của thông tin đó khong bị phát hiện bởi con người.
- Đối với ngữ cảnh thông tin được truyền đi bởi máy tính, thiết bị điện tử, một tập tin, thông điệp, hình ảnh, hoặc video có thể được ẩn trong một tập tin, thông điệp hình ảnh, video khác.
- Ưu điểm của `Steganography`:
    - Thông điệp bí mật không thu hút sự chú ý đến bản thân nó như một đối tượng để kiểm tra.
    - Tạo ra một lớp bảo mật thứ hai cho thông điệp bí mật bằng cách giấu nó vào một đối tượng khác.
    - Có thể kết hợp với `Cryptography` để tăng cường bảo mật.
    - Có nhiều phương pháp và kỹ thuật khác nhau để giấu tùy thược vào đặc tính và định dạng của đối tượng. Một số phương pháp cơ bản là `LSB (Least Significant Bit)`, `Masking and Filtering`, `Algorithms and Transformations`, `Parity Coding`, `Phase Coding`, `Spread Spectrum`, `Echo Hiding`,....
- Nhược điểm của `Steganography`: 
    - Không đảm bảo được tính bền vững của thông điệp bí mật trước những tấn công từ bên ngoài. Nếu đối tượng chứa thông điệp bị thay đổi (về nội dung, hình dạng, kích thước, …) thì thông điệp bí mật có thể bị mất hoặc bị biến dạng.
    - Không đảm bảo được khả năng không bị phát hiện của thông điệp bí mật. Nếu người tấn công nghi ngờ rằng đối tượng có chứa thông điệp bí mật, họ có thể sử dụng các phương pháp phân tích để tìm ra sự khác biệt giữa đối tượng bình thường và đối tượng đã được giấu tin. Một số phương pháp phân tích là Steganalysis, Visual Inspection, Statistical Analysis,...
    - Phụ thuộc vào dung lượng của đối tượng để giấu thông điệp. Nếu thông điệp quá lớn so với đối tượng, thì sẽ khó có thể giấu được mà không làm ảnh hưởng đến chất lượng của đối tượng.
---------------------
## Network Forensics:
- `Network Forensics`: hay điều tra mạng là một lĩnh vực tập trung vào việc thu thập, giải mã và phân tích dữ liệu mạng để tìm hiểu về các sự kiện, hành vi hoặc tấn công liên quan đến mạng máy tính. Mục tiêu của `network forensics` là tìm ra và hiểu rõ về các hoạt động bất thường hoặc có thể làm tổn thương hệ thống mạng.
- Các chủ đề chính trong `network forensics` bao gồm: 
    - Thu thập dữ liệu mạng: Ghi lại và lưu trữ thông tin về giao tiếp mạng, bao gồm dữ liệu từ các gói tin mạng, các sự kiện mạng, và các log hệ thống.
    - Phân tích gói tin mạng: Điều này bao gồm việc kiểm tra các gói tin truyền qua mạng để xác định thông tin quan trọng như nguồn và đích của gói tin, dữ liệu được truyền tải, và các thuật toán mật mã nếu có.
    - Phân tích dữ liệu log: Xem xét các log hệ thống để xác định các sự kiện quan trọng, như đăng nhập hệ thống, thay đổi cấu hình, và các hoạt động không bình thường.
    - Phát hiện tấn công mạng: Sử dụng các kỹ thuật phân tích để nhận biết các hành vi tấn công, malware, hoặc các hoạt động độc hại khác trên mạng.
    - Tạo bằng chứng: Xây dựng bằng chứng kỹ thuật số và lưu trữ thông tin để hỗ trợ quá trình điều tra và truy cứu trách nhiệm pháp lý.
---------------------
## Memory Forensics:
- `Memory Forensics`: tập trung vào việc thu thập và phân tích thông tin từ bộ nhớ hệ thống (RAM) của máy tính. Việc nghiên cứu bộ nhớ có thể cung cấp thông tin quan trọng về các hoạt động, quá trình, và dữ liệu mà không thể được thu thập từ lưu trữ trên đĩa cứng.
- Các quá trình chính trong memory forensics bao gồm:
    - `Acquisition` (Thu thập): Thu thập dữ liệu từ bộ nhớ hệ thống một cách an toàn để đảm bảo tính nguyên vẹn của thông tin. Các công cụ như LiME (Linux Memory Extractor) hoặc WinPmem (Windows Physical Memory) có thể được sử dụng để thực hiện quá trình này.
    - `Analysis` (Phân tích): Phân tích dữ liệu bộ nhớ để tìm ra thông tin quan trọng như quá trình đang chạy, tác vụ thực hiện, đối tượng đã được tạo ra và các hoạt động khác. Các mẫu mã độc hại, mã độc, hoặc các dấu hiệu của tấn công cũng có thể được xác định từ dữ liệu bộ nhớ.
    - `Reconstruction` (Tái tạo): Xây dựng lại chuỗi sự kiện từ dữ liệu bộ nhớ để hiểu rõ về hoạt động đã xảy ra trong hệ thống. Điều này có thể giúp xác định nguyên nhân của sự cố và tìm ra các tác nhân có thể liên quan.
---------------------
## Disk Forensics:
- `Disk Forensics`: tập trung vào việc thu thập, phân tích, và giải mã dữ liệu từ các thiết bị lưu trữ, chủ yếu là đĩa cứng và thiết bị lưu trữ khác. Mục tiêu của disk forensics là tìm hiểu về lịch sử sử dụng, hoạt động, và dữ liệu có trên các thiết bị lưu trữ này để hỗ trợ quá trình điều tra hoặc phục hồi thông tin quan trọng.
