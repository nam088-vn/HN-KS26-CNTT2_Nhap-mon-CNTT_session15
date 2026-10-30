**Bài 4 : Tối ưu hóa Lưu trữ Dữ liệu Doanh nghiệp**

## **1\. Giải pháp kỹ thuật: Thiết lập Files On-Demand** 

* **Bật tính năng Stream Files / Files On-Demand:**

  * Trên Google Drive for Desktop: Chọn **Stream files**   
      
  * Trên OneDrive: Bật **Files On-Demand**.

  * **Cơ chế:** File chỉ hiển thị dưới dạng biểu tượng con trỏ chiếm **0 KB** trên SSD. Dữ liệu thực chỉ được tải về bộ nhớ tạm khi double-click mở xem.

* **Xử lý Bẫy dữ liệu:**

  * **Giới hạn băng thông :** Đặt giới hạn Upload/Download trong cài đặt phần mềm đồng bộ ở mức 50–70% tốc độ mạng để không nghẽn Internet nhà trọ.

  * **Chống ngắt kết nối khi gập màn hình:** Trong Windows/macOS, chỉnh cài đặt nguồn: *Control Panel $\rightarrow$ Power Options $\rightarrow$ Choose what closing the lid does $\rightarrow$ Select "Do nothing"* khi cắm sạc.

## **2\. Báo cáo dung lượng và Chứng minh hiệu quả**

| Chỉ số dung lượng | Trước khi bật Files On-Demand | Sau khi bật Files On-Demand |
| :---- | :---- | :---- |
| **Tổng dữ liệu Video**  | 500 GB | 500 GB |
| **Dung lượng SSD sử dụng**  | \> 256 GB  | **\~ 2 – 5 GB**  |
| **Dung lượng SSD còn trống** | 0 GB  | **\~ 250 GB**  |

### **Chứng minh hiệu quả**

* **Hiệu quả lưu trữ:** Tiết kiệm **\> 99%** dung lượng ổ cứng cục bộ   
* **Tốc độ và An toàn:** Máy tính vận hành mượt mà, SSD không bị ghi nén dữ liệu liên tục gây giảm tuổi thọ, và 100% video vẫn truy xuất trực tiếp được từ ổ đĩa ảo bất cứ lúc nào có mạng.

