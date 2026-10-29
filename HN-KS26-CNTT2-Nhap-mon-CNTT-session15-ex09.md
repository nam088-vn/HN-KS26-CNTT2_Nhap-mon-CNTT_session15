**Bài 9: Tự Thiết Kế Hệ Thống Lưu Trữ và Phân Quyền Cho Dự Án CampusPay**

## PHẦN 1: Phân tích bài toán và thiết kế hệ thống 

## 1\. Xác định Đầu vào và Đầu ra

* Đầu vào :

  * Vai trò (4 nhóm): Ban Kỹ thuật (3 người), Ban Thiết kế (2 người), Ban Kinh doanh (2 người), Nhà đầu tư (1 người bên ngoài).

  * Tài liệu (5 loại): Mã nguồn/API Keys, Asset Thiết kế, Business Plan, Slide Pitch, Log và Data sinh viên.

* Đầu ra (Output): Sơ đồ cấu trúc thư mục 2 cấp chuẩn và Bảng phân quyền 6 cột tuân thủ 5 nguyên tắc bảo mật.

### 2\. Cấu trúc Thư mục Google Drive 2 Cấp

 \[CampusPay\_Root\] (Owner: Trưởng nhóm)  
──  01\_Ky\_Thuat/        \--\> Code, API Keys, DB Schema, Log hệ thống   
──  02\_Thiet\_Ke/        \--\> Design System, UI/UX, Brand Assets  
──  03\_Kinh\_Doanh/      \--\> Business Plan, Báo cáo tài chính, Hợp đồng   
──  04\_Chung\_External/  \--\> Slide Pitch, Business Summary 

### 3\. Quy trình Triển khai Cấu hình Hệ thống

1. Tạo thư mục: Trưởng nhóm khởi tạo thư mục gốc \[CampusPay\_Root\] và 4 thư mục con.

2. Đặt tên: Định dạng chuẩn \[Mã\_Ban\]\_\[Tên\_Tài\_Liệu\]\_\[Version\].

3. Cấp quyền: Gán quyền Restricted theo Email cá nhân, tuyệt đối KHÔNG bật *Anyone with link*.

4. Kiểm tra: Dùng tài khoản phụ/Incognito test trực tiếp quyền truy cập trên từng thư mục.

5. Thu hồi/Cập nhật: Cài Set Expiration Date cho tài khoản ngoài và thiết lập quy trình Offboarding.

## PHẦN 2: TRIỂN KHAI PHÂN QUYỀN & XỬ LÝ BẪY DỮ LIỆU

### 1\. Bảng Phân Quyền Hoàn Chỉnh (6 Cột)

| Loại tài liệu | Ban KT | Ban TK | Ban KD | Nhà đầu tư | Ghi chú bảo mật |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Source Code & API Keys | Editor | Không | Không | Không | Restricted; Tối mật nội bộ Dev. |
| Thiết kế UI & Assets | Viewer | Editor | Viewer | Không | Dev/KD chỉ xem/tải asset. |
| Business Plan (Chi tiết) | Viewer | Không | Editor | Không | Dev Viewer để nắm context; Không sửa. |
| Slide Pitch & Pitch Deck | Viewer | Viewer | Editor | Viewer (14d) | Cài *Set Expiration Date* 14 ngày. |
| Log & Data Sinh viên Beta | Editor | Không | Không | Không | Chứa PII nhạy cảm; Giới hạn tối đa. |

### 2\. Giải Quyết 3 Bẫy Dữ Liệu

* Bẫy 1 :

  * Quyền cấp: Viewer .

  * Cấu hình thêm: Tắt tính năng *"Editors can change permissions and share"*.

  * Lý do: Dev đọc hiểu context để code đúng nghiệp vụ nhưng không thể sửa nội dung hoặc tự ý chia sẻ tiếp ra ngoài.

* Bẫy 2 :

  * Quyền cấp: Viewer \+ Cài Set Expiration Date (14 ngày).

  * Tính năng 'Viewers can download': Bật.

  * Lý do: NĐT cần tải PDF về thuyết trình offline. File PDF không thể chỉnh sửa trực tiếp slide gốc trên Drive.

* Bẫy 3 :

  * Thao tác: (1) Xóa Email cá nhân khỏi danh sách chia sẻ của Folder/File. (2) Revoke Google Workspace Account (nếu dùng email doanh nghiệp). (3) Đổi API Keys/Secret Keys nếu là Dev.

  * Lý do: Vì hệ thống dùng quyền Restricted theo Email (không dùng Link Public), xóa Email sẽ lập tức cắt hoàn toàn quyền truy cập.

