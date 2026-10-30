**Bài 3 : Xây dựng Không gian Cộng tác Doanh nghiệp**

## **Phần 1: Sơ đồ kiến trúc kênh**

|  Tên Channel | Loại kênh | Quy định nội dung & Quy tắc |
| :---- | ----- | ----- |
| **`#announcements`** | Read-only (Chỉ Admin đăng) | Báo cáo deadline, mốc dự án, lịch họp. Không chat linh tinh. |
| **`#tech-hardware`** | Discussion | Thảo luận chuyên sâu về cảm biến, mạch điều khiển, phần cứng bãi đỗ xe. |
| **`#tech-software`** | Discussion | Thảo luận backend, app, API, thuật toán xử lý chỗ trống. |
| **`#general`** | Public Chat | Thảo luận chung công việc, câu hỏi nhanh, vận hành dự án. |
| **`#random-offtopic`** | Casual | Chia sẻ meme, tán gẫu, ăn uống, giải trí ngoài giờ. |

## **2\. Giải pháp xử lý Bẫy dữ liệu**

* Chuyển từ giao tiếp đồng bộ (Synchronous) sang bất đồng bộ (Asynchronous): Quy định thời gian phản hồi tiêu chuẩn là trong vòng 1 – 2 giờ làm việc, không yêu cầu rep tức thì.  
* Sử dụng tính năng Status & Do Not Disturb (DND):  
  * Cài trạng thái Slack/Lark: `Focusing / Coding (No Ping)` hoặc bật chế độ DND để tắt thông báo.  
  * Chỉ liên hệ qua kênh khẩn cấp (Hotline/Call trực tiếp) nếu hệ thống bãi đỗ xe gặp sự cố nghiêm trọng (Critical Production Bug).  
* Bắt buộc dùng Reply in Thread: Mọi phản hồi, trao đổi phụ phải gõ trực tiếp trong Thread của tin nhắn gốc để không phát tiếng ting-ting nhảy thông báo cho cả kênh.

## **3\. Bản quy ước giao tiếp: 3 Quy tắc vàng**

1. **Nói không với "No-Hello Trap":**  
   * *Không nhắn:* "Chào bạn", "Admin ơi có đó không?" rồi ngồi đợi rep mới gõ tiếp.  
   * *Phải nhắn:* Chào \+ Nội dung cần hỏi \+ Context/File/Link liên quan trong **cùng 1 tin nhắn**   
2. **Triệt để dùng Reply in Thread:**  
   * Mọi thảo luận, câu hỏi nối tiếp phải click Reply in Thread dưới tin nhắn liên quan. Không gõ trực tiếp ra khung chat chính để tránh làm trôi tin nhắn và đè nát deadline.  
3. **Cấm Spam `@all` / `@channel` tùy tiện:**  
   * Chỉ `@all` / `@everyone` trong kênh `#announcements` cho các thông báo khẩn cấp hoặc mốc deadline quan trọng của toàn dự án.  
   * Trao đổi cá nhân hoặc nhóm nhỏ chỉ `@mentions` đúng tên người liên quan trong Thread.

