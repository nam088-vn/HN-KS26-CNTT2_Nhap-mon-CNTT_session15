**Bài 1 : Hệ thống Quản lý Tài liệu Dự án Doanh nghiệp**

**Phần 1: Báo cáo phân tích** 

- **Sơ đồ luồng dữ liệu:** `Ctrl + S` → Ghi vào Local SSD → Google Drive for Desktop phát hiện thay đổi → Đẩy file lên Cloud → Tạo bản lưu trong Version History  
- **Xử lí bẫy dữ liệu và xung đột phiên bản:**  
+ **Trường hợp sập nguồn đột ngột / Mất mạng:**

  File được ghi tức thì vào ổ SSD cá nhân. Google Drive for Desktop duy trì hàng đợi ngoại tuyến (Offline Queue) và tự động nối lại tiến trình đẩy file lên đám mây ngay khi máy có mạng hoặc khởi động lại.

+ **Xử lý xung đột phiên bản :**

  Nếu 2 người cùng sửa 1 file offline hoặc nhấn `Ctrl + S` cùng lúc, Google Drive sẽ giữ bản ghi sau làm bản chính và tạo thêm file xung đột chứa tên người dùng/thời gian để không mất dữ liệu của ai.

+ **Khôi phục bản vẽ :**

  Click chuột phải vào file trong Google Drive →→ Chọn Quản lý các phiên bản (Manage versions) / Lịch sử phiên bản →→ Tải bản cũ ổn định xuống hoặc chọn Khôi phục (Restore).

## **Phần 2: Quy trình thực thi:**

## **3 bước thiết lập phần mềm đồng bộ chuẩn**

* **Bước 1:** Tạo thư mục dự án trên SSD   
* **Bước 2:** Chuột phải vào thư mục dự án → Chọn Always keep on this device để file luôn ở local, đảm bảo tốc độ `Ctrl + S` và làm việc mượt khi mất mạng.  
* **Bước 3 :** Vào App đồ họa bật Auto-Recovery 5-10 phút/lần và trỏ Scratch Disk về SSD tốc độ cao.

