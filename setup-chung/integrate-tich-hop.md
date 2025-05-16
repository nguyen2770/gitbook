---
description: Quản lý kết nối với các dịch vụ bên thứ ba
icon: '6'
---

# Integrate (Tích hợp)

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

### **Webhook là gì?** <a href="#webhook-la-gi" id="webhook-la-gi"></a>

Webhook là một cơ chế giúp hệ thống này có thể gửi dữ liệu theo thời gian thực đến hệ thống khác thông qua HTTP. Khi một sự kiện xảy ra trong hệ thống nguồn, webhook sẽ tự động kích hoạt và gửi một yêu cầu HTTP (thường là một POST request) đến một URL được cấu hình trước. Điều này giúp tự động hóa quy trình và tích hợp giữa nhiều dịch vụ mà không cần phải liên tục kiểm tra hoặc truy vấn dữ liệu.

### **Cấu hình Webhook:** <a href="#cau-hinh-webhook" id="cau-hinh-webhook"></a>

* **URL webhook**: `https://app.gemlogin.vn/api/execscript` – Đây là endpoint mà hệ thống sẽ gửi dữ liệu khi webhook được kích hoạt.
* **Định dạng body JSON**: Chứa các tham số quan trọng như:
  * `token`: Chuỗi mã xác thực để đảm bảo webhook hợp lệ.
  * `device_id`: ID của thiết bị đang thực thi.
  * `profile_id`: ID của profile trình duyệt cần chạy.
  * `workflow_id`: ID của workflow (quy trình tự động) cần thực hiện.
  * `parameter`: Các tham số bổ sung cho workflow.
  * `soft_id`: Giá trị xác định loại phần mềm hoặc dịch vụ sử dụng.
  * `close_browser`: `false` – Cho biết có đóng trình duyệt sau khi thực hiện tác vụ hay không.

Dưới cùng là hướng dẫn sử dụng webhook với **N8N** – một công cụ tự động hóa quy trình:

1. Sao chép URL và body của webhook.
2. Tạo một webhook mới trong N8N.
3. Cấu hình webhook trong N8N để nhận và xử lý dữ liệu theo yêu cầu.
4. Kiểm tra kết nối

Giao diện hiển thị webhook đang **"Đã bật"**, nghĩa là nó sẵn sàng hoạt động khi có sự kiện phù hợp được kích hoạt.

\


{% embed url="https://youtu.be/r3ItoLzsk_U?si=iwgxAGlcbod1roMX" %}
