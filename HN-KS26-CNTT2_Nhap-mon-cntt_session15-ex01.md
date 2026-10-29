**Bài 1 : Loại bỏ rủi ro lưu trữ cục bộ trong dự án nhóm**

### **Phần 1: 3 hậu quả thảm họa dữ liệu**

1. **Mất code vĩnh viễn:** Nhấn `Ctrl + S` khi lỡ xóa code trên file đơn lẻ khiến dữ liệu biến mất hoàn toàn, không có thùng rác để khôi phục.  
2. **Loạn phiên bản qua Zalo:** Đặt tên file thủ công như: `v1`, `v2_final` dễ khiến nhóm lấy nhầm bản cũ, gây xung đột mã nguồn.  
3. **Mất dữ liệu khi máy hỏng:** Chỉ lưu file trên máy cá nhân mà không dùng Cloud nghĩa là toàn bộ dự án sẽ mất nếu máy gặp sự cố.

### **Phần 2: Quy trình Hybrid Workflow**

1. **Dùng Local History của IDE:**  
   * Khi lỡ tay xóa code, chỉ cần chuột phải vào file → Chọn **Local History: Show Previous Revisions** → Bấm **Restore** để lấy lại code cũ ngay lập tức.  
2. **Sử dụng Git và GitHub:**  
   * Dùng lệnh `git commit` để lưu các mốc code an toàn và `git push` lên GitHub.  
   * Khi cần quay lại bản cũ, chỉ mất 1 lệnh thay vì gửi file qua Zalo.  
3. **Quy tắc làm việc nhóm:**  
   * Dừng hẳn việc gửi file code qua Zalo. Mỗi người code một nhánh riêng trên GitHub để tránh đè code của nhau.

