**Bài 8: Kiểm Tra Vì Sao Dữ Liệu Khách Hàng CampusPay Bị Rò Rỉ Ra Ngoài**

## **Phần 1: Phân tích lỗ hổng**

### **1\. Nguồn gốc trực tiếp gây rò rỉ dữ liệu khách hàng**

* **Dòng gây rò rỉ trực tiếp:** Dòng **08:15 T2** (campuspay\_beta\_users.xlsx \| Thành viên A \| **Editor** \| **Anyone with the link**).

* **Giải thích kỹ thuật và Cơ chế:**

  * **Vi phạm cờ đỏ:** Kết hợp quyền Editor \+ phạm vi Anyone with the link.

  * **Cơ chế rò rỉ:** Bất kỳ ai có đường link URL đều có thể truy cập, xem toàn bộ thông tin cá nhân/số dư, tải file về hoặc chia sẻ tiếp link cho người khác mà không cần xác thực tài khoản. Link này sau đó bị phát tán lên hội nhóm Facebook công khai.

### **2\. Ba giả thuyết "Email người lạ" truy cập campuspay\_api\_keys.txt**

1. **Tài khoản B bị chiếm đoạt :** Email B bị hở mật khẩu hoặc trúng mã độc , kẻ tấn công dùng chính session/tài khoản của B để truy cập.

2. **Email B hoặc Trưởng nhóm chủ động chia sẻ tiếp/Ủy quyền:** Email B thêm email người lạ đó vào danh sách truy cập, hoặc dùng tính năng *Transfer Ownership* / đổi quyền file sang công khai sau mốc 09:30 T2.

3. **Lộ API Key hoặc Link ủy quyền phụ:** File bị tải về máy cá nhân của B rồi bị đẩy lên repo công khai, hoặc Email B cấp quyền cho một ứng dụng bên thứ 3 có quyền đọc Google Drive.

## **Phần 2: Sửa lỗi và Nghiệm thu**

### **3\. Bảng cấu hình quyền chia sẻ chuẩn**

| Tên file | Quyền đúng | Phạm vi đúng | Giải thích ngắn gọn |
| :---- | :---- | :---- | :---- |
| campuspay\_beta\_users.xlsx | **Viewer**(Editor) | **Restricted**  | Dữ liệu nhạy cảm PII/số dư; tuyệt đối không bật link công khai, chỉ mở cho nhân sự cần xử lý. |
| campuspay\_api\_keys.txt | **Viewer** | **Restricted**  | Quyền truy cập hệ thống tối mật; giới hạn đúng người, không cấp quyền Editor để tránh bị sửa/xóa key. |
| slide\_pitch\_v8.pptx | **Commenter**/ **Viewer** | **Anyone with the link**  | Slide thuyết trình cần gom góp ý/review, cấp Commenter để người xem không làm hỏng layout gốc. |

### **4\. Xử lý vô hiệu hóa link & Tính năng 'Set Expiration Date'**

* **Tính năng vô hiệu hóa nhanh nhất:** Chuyển phạm vi truy cập của file từ *Anyone with the link* về Restricted. Ngay lập tức toàn bộ URL cũ đã phát tán ra ngoài đều bị vô hiệu hóa hoàn toàn.

* **Khi nào dùng 'Set Expiration Date' :**

  * Dùng khi chia sẻ tài nguyên cho đối tác, CTV, Tester hoặc dự án ngắn hạn.

  * Thay vì phải đặt lịch để thu hồi thủ công (dễ bị quên), hệ thống sẽ tự động cắt quyền truy cập ngay khi hết hạn,đảm bảo nguyên tắc an toàn dữ liệu tự động.

