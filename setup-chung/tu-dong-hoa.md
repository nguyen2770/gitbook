---
description: Cài đặt các thông số chạy
icon: '2'
---

# Tự động hóa

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>Cài đặt quy trình</p></figcaption></figure>

**Các mục cài đặt chính:**

1. **Workflow Logs**
   * **60 ngày**: Thời gian lưu trữ nhật ký quy trình làm việc.
   * **Giới hạn logs: 1**: Số lượng nhật ký tối đa được giữ lại.
2. **Số luồng đồng thời**
   * Giá trị **20**: Xác định số lượng quy trình tự động chạy cùng lúc.
3.  **Tỉ lệ**

    * Giá trị **0.768**: Xác định tỷ lệ kích thước cửa sổ trình duyệt khi mở.

    ( Thường để auto scale để phần mềm tự động chia theo kích thước màn hình )
4. **Kích thước cửa sổ**
   * **Row = 4**, **Column = 5**: Quy định số hàng và cột khi mở nhiều cửa sổ trình duyệt cùng lúc.
5. **Thời gian mở giữa các hồ sơ (ms)**
   * Giá trị **500**: Nghĩa là mỗi hồ sơ sẽ mở cách nhau 0,5 giây (1000ms = 1s).
6. **Đổi IP**
   * Giá trị **Không đổi IP**: Không tự động thay đổi IP khi mở trình duyệt.
   * Proxy: Sử dụng proxy người dùng gán vào profile thay đổi IP khi mở trình duyệt.
   * Proxy xoay: Sử dụng proxy xoay đổi IP khi mở trình duyệt.
7. **Số lần lặp lại**
   * Giá trị **0**: Quy trình không tự động lặp lại.
8. **Tùy chọn bổ sung**
   * ✅ **Kiểm tra IP khi bắt đầu**: Hệ thống kiểm tra IP trước khi chạy quy trình.
   * ✅ **Tự động đóng trình duyệt sau khi hoàn thành**: Trình duyệt sẽ tự động đóng sau khi tác vụ kết thúc.
