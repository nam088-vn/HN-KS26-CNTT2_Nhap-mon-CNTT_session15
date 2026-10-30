**Bài 2 : Quản lý Quyền truy cập Báo cáo Tài chính**

**Phần 1: Bản thiết kế phân quyền**

| Chức vụ | Quyền truy cập |
| :---: | :---: |
| **Trưởng phòng** | **Editor** |
| **Trưởng bộ phận** | **Commenter**  |
| **Ứng viên** | **Viewer**  |

**Phần 2: Xử lí sự cố và bẫy** 

- **Xử lí sự cố:**   
+ Bước 1: Chặn truy cập tức thì chuyển trạng thái file về Restricted và thu hồi ngay lập tức các email bị cấp sai quyền.  
+ Bước 2: Truy vết & Đánh giá thiệt hại Mở Version History và check Drive Audit Log kiểm tra xem file đã bị tải, copy hay chỉnh sửa chưa.  
+ Bước 3: Khắc phục và Cấu hình lại. Cấu hình lại bảng phân quyền chuẩn , bật lại các cờ bảo mật chặn Download/Copy, và gửi thông báo chấn chỉnh nội bộ  
- **Xử lý bẫy:** Vào nút Share → Tìm email ứng viên → Đổi quyền thành Remove access → Đổi phạm vi file từ "Anyone with the link" về Restricted.