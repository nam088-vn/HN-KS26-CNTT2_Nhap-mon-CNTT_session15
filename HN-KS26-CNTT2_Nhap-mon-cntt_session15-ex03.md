**Bài 3 : Ngăn chặn quá tải lưu trữ khi đồng bộ mã nguồn**

### **1: Báo cáo phân tích I/O** 

### **Ghi Local:** Nhấn Ctrl \+ S →→ IDE ghi dữ liệu trực tiếp lên Local SSD (tốc độ tối đa, không độ trễ).

1. **Bộ lọc đồng bộ :** Phần mềm Cloud Sync quét thay đổi nhưng bị chặn bởi file .gitignore / .syncignore →→ **Loại trừ hoàn toàn** thư mục node\_modules và file rác (dist/, .env), tránh treo hệ thống và tràn dung lượng.  
2. **Đẩy lên Cloud :** Chỉ các file source code thay đổi mới được đồng bộ lên Cloud. Các file ít dùng được giữ dạng đám mây.  
3. **Xác nhận:** Hoàn tất đồng bộ, icon chuyển sang **tích xanh**

**2\. Thiết kế thư mục Cloud chuẩn cho Lập trình viên**

 D:\\Project\_Root/ 

1.           src/ \# Source code chính (JS/TS, components) \- ĐỒNG BỘ CLOUD   
2.           docs/ \# Tài liệu kỹ thuật, SRS, thiết kế \- ĐỒNG BỘ CLOUD   
3.           assets/ \# Hình ảnh, icon, thiết kế UI/UX \- ĐỒNG BỘ CLOUD   
4.           package.json \# Khai báo thư viện (Không lưu node\_modules)   
5.           gitignore \# Chặn node\_modules, dist, .env đẩy lên Git/Cloud   
6.           syncignore \# Chặn phần mềm Cloud Sync quét node\_modules

