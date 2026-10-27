# Tool Xử Lý Dữ Liệu Tự Động (Web ➔ Sheet)

Công cụ web đơn trang (Single-page Web App) giúp tự động phân tích dữ liệu thô hàng ngày, trích xuất thông tin ca dạy, giáo viên, cơ sở và chuẩn hóa dữ liệu để dán nhanh chóng vào Google Sheets hoặc Excel.

---

## ✨ Tính năng nổi bật

- **Tự động phân tích & bóc tách dữ liệu:** Nhận diện thông tin từ văn bản thô (Cơ sở, Tên giáo viên, Bậc giáo viên, Khung giờ dạy).
- **Xử lý thời gian thông minh:** Tự động sắp xếp các ca dạy, tính toán thời gian bắt đầu sớm nhất, thời gian kết thúc muộn nhất và tổng số ca dạy trong ngày của từng giáo viên.
- **Hỗ trợ định dạng ngày linh hoạt:** Dễ dàng chọn ngày đánh giá và tự động chuyển đổi sang chuẩn `DD/MM/YYYY`.
- **Tối ưu hóa thao tác Copy/Paste:** 
  - Hỗ trợ nút **Copy Bảng** chuyển đổi toàn bộ dữ liệu thành định dạng Tab-separated chuẩn xác.
  - Tích hợp sự kiện xử lý vùng bôi đen (Selection Copy) giúp copy linh hoạt một phần bảng dán thẳng vào Google Sheets mà không lo lỗi định dạng.
- **Giao diện thân thiện:** Thiết kế tối giản, trực quan, chạy trực tiếp trên trình duyệt mà không cần cài đặt phức tạp hay cấu hình backend.

---

## 💡 Ví dụ mô phỏng hoạt động

### 1. Dữ liệu thô đầu vào (`Raw Input`)
*Khi bạn dán dữ liệu báo cáo thô vào ô nhập liệu:*

```text
Cơ sở Quận 1
08:00 - 09:30 - Nguyễn Văn A - Bậc 1 - 10 HV
09:30 - 11:00 - Nguyễn Văn A - Bậc 1 - 8 HV
14:00 - 15:30 - Trần Thị B - Bậc 2 - 12 HV

Cơ sở Quận 7
08:30 - 10:00 - Lê Văn C - Bậc 1 - 9 HV
```

### 2. Kết quả sau khi xử lý (`Processed Table`)
*Sau khi chọn ngày và bấm nút **"🚀 Xử Lý & Tách Cột"**, bảng kết quả sẽ tự động tổng hợp như sau:*

| Cơ sở đánh giá | Họ và tên GV | Ngày đánh giá | Bậc GV | Bắt đầu | Kết thúc | Số ca |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Cơ sở Quận 1 | Nguyễn Văn A | 28/10/2026 | Bậc 1 | 08:00 | 11:00 | 2 |
| Cơ sở Quận 1 | Trần Thị B | 28/10/2026 | Bậc 2 | 14:00 | 15:30 | 1 |
| Cơ sở Quận 7 | Lê Văn C | 28/10/2026 | Bậc 1 | 08:30 | 10:00 | 1 |

---

## 🛠️ Công nghệ sử dụng

- **HTML5 / CSS3:** Xây dựng giao diện responsive, thanh cuộn bảng cố định tiêu đề (`sticky header`), hỗ trợ bôi đen văn bản giống bảng tính chuyên nghiệp.
- **JavaScript (Vanilla JS):** Xử lý chuỗi (String manipulation), biểu thức chính quy (Regex), quản lý trạng thái DOM và tương tác Clipboard API.

---

## 🚀 Hướng dẫn sử dụng

1. Mở file `index.html` trực tiếp trên bất kỳ trình duyệt web nào (Chrome, Edge, Firefox,...).
2. **Dán dữ liệu thô:** Copy dữ liệu báo cáo/chấm công hàng ngày và dán vào ô **"1. Dán dữ liệu thô vào đây"**.
3. **Chọn ngày đánh giá:** Chọn ngày tháng tương ứng tại mục **Ngày đánh giá**.
4. **Xử lý:** Bấm nút **"🚀 Xử Lý & Tách Cột"** để hệ thống bóc tách dữ liệu.
5. **Xuất dữ liệu:** 
   - Bấm **"📋 Copy Bảng"** để sao chép toàn bộ kết quả.
   - Hoặc bôi đen các ô cần thiết trực tiếp trên bảng kết quả.
6. Mở **Google Sheets** hoặc **Excel**, chọn ô đầu tiên và bấm `Ctrl + V` để dán dữ liệu đã phân cột hoàn chỉnh.

---

## 🔗 Liên kết nhanh
* [Mở Tool Phân Tích Zalo OA (Công cụ liên quan)](https://tool-phan-tich-zalo-oa.vercel.app/)
