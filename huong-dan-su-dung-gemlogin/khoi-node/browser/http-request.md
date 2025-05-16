---
description: Hỗ trợ việc gửi HTTP request trên GemLogin
---

# HTTP Request

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FWkcR0WvMRVXySgn7BhLx%252Fimage.png%3Falt%3Dmedia%26token%3D6b5ae779-28da-4a54-89ed-acba3f9e32d2&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=64f54d77&#x26;sv=2" alt=""><figcaption></figcaption></figure>

HTTP là thuật ngữ ám chỉ phương thức để giao tiếp giữa client - server thông qua giao thức HTTP (giao thức ám chỉ các quy định mà client và server đều đồng thuận để phục vụ giao tiếp giữa 2 bên).

_Để đơn giản, hãy hình dung mọi thứ như khi bạn muốn gửi thư tới một người khác. Bạn sẽ cần phải viết thư, sau đó mang thứ tới bưu điên, người nhận sẽ nhận thư và nếu muốn họ sẽ viết một bức thư khác để trả lời cho bạn. Đó là miêu tả đơn giản về quá trình gửi - nhận thư. Bạn có thể hình dung cách mọi thứ hoạt động như việc bạn gửi đi một bức thư: Bức thứ là một request; bưu điện yêu cầu bạn điền rõ địa chỉ người nhận theo một định dạng - định dạng của địa chỉ người nhận có thể được hình dung như là cách giao thức HTTP hoạt động; người sẽ nhận thư và trả lời thư của bạn chính là server; thùng thư của người nhận sẽ là web api. Đó là một cách hiểu đơn giản mà bạn có thể dùng để tiếp cận mọi thứ._

Phục vụ cho mục đích này, block https request sẽ cung cấp các option sau để điền thông tin cần thực hiện request:

* Request method: cho phép bạn chỉ định [phương thức request](https://en.wikipedia.org/wiki/HTTP#Request_methods), GemLogin hõ trợ 6 phương thức request là GET, POST, PUT, PATCH, DELETE, HEAD.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F6sgqZ5HgbaxSDIgnZLWt%252Fimage.png%3Falt%3Dmedia%26token%3D0ee65917-69a6-4bca-a1b4-d3b27af5279e&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=3b76a1c9&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Request url: cho phép bạn chỉ định url mà request sẽ được gửi tới.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FPb8klDzgVbFySkdTxY7D%252Fimage.png%3Falt%3Dmedia%26token%3Dad62a9a4-ad3c-49ca-972f-857b170bea54&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=6d5b37ea&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Header: cho phép bạn chỉ định header của request dưới dạng json.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F0F0WjhOH0v6Ti3fS1zCg%252Fimage.png%3Falt%3Dmedia%26token%3D72bcb46d-6b16-45c7-9046-22c4365d48f9&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=bfc8ca43&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Response: Cho phép bạn chỉ định xử lý với response trả về. GemLogin hỗ trợ bạn chỉ định kiểu dữ liệu của response (bao gồm JSON, Text và Base64) để tự động ép kiểu response trả về, đồng thời cung cấp lựa chọn gán vào biến/chèn vào mảng để có thể sử dụng trong các phần khác của script.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FRmLH7p6J7BXT231AQrUu%252Fimage.png%3Falt%3Dmedia%26token%3D5ab43ea3-53b8-4213-ae0f-926a5a20880e&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8c2d2918&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* \*Body: Đối với phương thức request có yêu cầu body (như post/patch/...), bạn có thể chọn định dạng của body và nhập giá trị của body theo định dạng đã được đặt từ trước đó.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FLgzLf9oFEfMksSCREHHx%252Fimage.png%3Falt%3Dmedia%26token%3D0ea33e1f-7919-492a-be47-ec67bc1c49ab&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=4b4c339e&#x26;sv=2" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=DbPoFD5K1k8" %}

Video hướng dẫn dùng http Get Mail Domain và đọc nội dung mail & lấy mã xác thực OTP

{% embed url="https://www.youtube.com/watch?v=1NSgQ6SmGsc" %}
