---
description: Setup quy trình chạy tự động
---

# Tự động hóa - Automation

### 1. **Tùy chọn:**

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

* **Số lượng hồ sơ:** Hiển thị số lượng profile hiện tại (ở đây là **19**).
* **Quy trình:** Một danh sách thả xuống (**Select**) để chọn tên quy trình muốn chạy
* **Loại tác vụ:**
  * **Mặc định:** Chạy ngay theo quy trình đã chọn.
  * **Lịch trình:** Thiết lập thời gian chạy tự động theo lịch.

### 2. Cấu hình chạy:

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

* **Số lượng đồng thời:** 6 (Số profile chạy cùng lúc).
* **Tỉ lệ:** 0.6 (tỉ lệ hiển thị cửa sổ trình duyệt).
* **Kích thước cửa sổ:**
  * **Row = 2** (Số hàng hiển thị).
  * **Column = 3** (Số cột hiển thị).
* **Thời gian mở giữa các hồ sơ (ms):** 500ms (Thời gian chờ giữa mỗi lần mở profile, tức 0,5 giây).
* **Số lần lặp lại:** 1 (Số vòng lặp chạy quy trình).

### **3. Mạng:**

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

* **Do not change IP** (Không thay đổi IP) -> Sử dụng IP gốc của máy .
* **Proxy** (Sử dụng proxy tĩnh) -> Sử dụng IP được gán vào profile.
* **Rotation proxy** (Sử dụng proxy xoay, IP thay đổi liên tục).

⇒ Với proxy dạng xoay custom

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption><p>Proxy xoay dạng custom</p></figcaption></figure>

* Mục đổi IP => Chọn xoay proxy.&#x20;
* Cách xoay proxy => Custom.&#x20;
* Danh sách => Theo định dạng ip:port|api hoặc ip:port|Username|Password|api.&#x20;
* Thời gian chờ => Thời gian tối đa chờ xoay proxy.
