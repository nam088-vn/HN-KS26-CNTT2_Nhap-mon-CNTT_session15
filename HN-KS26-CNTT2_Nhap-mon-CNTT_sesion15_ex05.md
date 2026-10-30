**Bài 5 : Giao tiếp Bất đồng bộ trong Doanh nghiệp**

## **1\. Tin nhắn mẫu chuẩn Asynchronous Communication**  Gửi trực tiếp đầy đủ ngữ cảnh trong 1 tin nhắn duy nhất, người ở múi giờ khác chỉ cần đọc là có thể bắt tay vào làm ngay mà không phải hỏi lại:

**\[BUG FIX NEEDED\] Lỗi 500 khi nhấn nút Thanh toán** 

* **Bối cảnh:** User báo lỗi không thể hoàn tất thanh toán từ 14h chiều nay.

* **Hiện trạng:** Đã check log, phát sinh lỗi NullPointerException tại service xử lý mã giảm giá.

* **Tài liệu và Log kèm theo:**

  * Screen record lỗi: \[Link Figma/Video\]

  * Full Error Log: \[Link Log File/Sentry\]

  * Branch Git liên quan: fix/checkout-discount-bug

* **Yêu cầu:** Nhờ **@Tuấn (Mỹ)** kiểm tra và hotfix hàm applyDiscount() trên branch nói trên, sau đó đẩy PR và tag **@Nam (Nhà)** review.

* **Mức độ ưu tiên:** High.

## **2\. Lịch trình gửi tin theo lệch múi giờ**

Đặt lịch gửi tin nhắn/email trùng với 08:30 \- 09:00 sáng tại múi giờ địa phương của từng người:

| Thành viên | Múi giờ | Giờ gửi đề xuất  | Giờ Việt Nam tương ứng  | Mục đích |
| :---- | :---- | :---- | :---- | :---- |
| **Nhóm Hà Nội** | UTC+7  | 08:30 AM  | **08:30 AM** | Giao việc đầu ngày tại VN. |
| **Đồng đội Nhật Bản** | UTC+9  | 08:30 AM  | **06:30 AM** | Đợi họ ngủ dậy và chuẩn bị làm việc mới nhận tin. |
| **Đồng đội Mỹ (Cali)** | UTC-7  | 08:30 AM  | **22:30 PM** | Gửi vào buổi tối VN . |

