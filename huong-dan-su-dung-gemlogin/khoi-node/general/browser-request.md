---
description: >-
  Thực hiện một yêu cầu HTTP với cookie từ trình duyệt được tự động thêm vào
  header.
---

# Browser Request

Block Browser Request được dùng để thực hiện một yêu cầu HTTP với cookie từ trình duyệt được tự động thêm vào header. Cấu trúc node gồm các thành phần như:

Phương thức

* Phương pháp yêu cầu: Các phương pháp yêu cầu có thể sử dụng như GET, POST, PUT, DELETE, etc.

Địa chỉ đích

* Địa chỉ URL: Địa chỉ URL mà yêu cầu sẽ được gửi đến.

Chọn một loại nội dung

Có 4 loại nội dung mà bạn có thể lựa chọn:

1. Text/plain: Định dạng văn bản thuần túy, không có định dạng hay mã hóa đặc biệt.
2. Application/json: Định dạng dữ liệu JSON, thường được sử dụng trong việc truyền tải dữ liệu giữa server và client.
3. Multipart/form-data: Đại diện cho Multipart form, kiểu mã hóa này được sử dụng khi người dùng muốn tải tệp dữ liệu lên.
4. Application/x-www-form-urlencoded: Là kiểu mã hóa mặc định nếu thuộc tính enctype không có giá trị. Đại diện cho URL Encoded Form. Tất cả các ký tự được mã hóa trước khi gửi (khoảng trắng được chuyển đổi thành ký hiệu "+" hoặc "%20" và các ký tự đặc biệt được chuyển đổi thành giá trị ASCII HEX).

Thời gian chờ

* Thời gian chờ: Đặt thời gian chờ để thực hiện yêu cầu HTTP. Chọn 0 để không có thời gian chờ.

Headers

* Headers: Mục này thường được dùng để xác thực tài khoản sử dụng API của bạn bằng Header được yêu cầu. Ví dụ, bạn cần xác thực bằng Bearer token.

Nội dung

* Nội dung yêu cầu: Nội dung cần gửi trong yêu cầu HTTP.

Phản hồi

* Phản hồi: Nhận dữ liệu được trả về khi gọi API dưới các dạng: JSON, text, base64.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FEeW18Cn7EAUGpu6IRK0O%252Fimage.png%3Falt%3Dmedia%26token%3D7d73c736-cdd8-4e67-9cbd-6f597451d2c0&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=ebee9923&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Viết biểu thức bên trong Nội dung

Khi viết biểu thức bên trong nội dung để truy cập dữ liệu như biến, bảng, v.v., cần đảm bảo rằng kết quả cuối cùng là JSON hợp lệ. Để tránh lỗi "Nội dung không hợp lệ JSON", bạn cần đóng gói biểu thức bên trong hàm $stringify.

Giá trị chuỗi nhiều dòng

* Giá trị chuỗi nhiều dòng: Nếu giá trị của dữ liệu bạn tham chiếu là một chuỗi và có một dòng mới trong đó, bạn phải thêm dấu chấm than (!) trước khi viết từ khóa của dữ liệu. Ví dụ:

json

Copy

```
{
  "longText": {{!$stringify([variables.src])}}
}
```

Khác

* Đối tượng, mảng, v.v.: Nếu giá trị của dữ liệu bạn tham chiếu là đối tượng, mảng, v.v., bạn có thể viết trực tiếp {} vào bên trong phần thân. Ví dụ:

**json**

Copy

```
{
  "profile": {{$stringify([variables.userProfile])}}, // { name: 'John Doe', email: 'john@example.com' }
  "stats": {{$stringify([variables.stats])}} // stats:["10", "200", "87", "21"]
}
```

Phản hồi

Sau khi nhận dữ liệu trả về từ API, bạn cần xử lý chúng để sử dụng. Mục này bao gồm một số thông tin bạn cần chú ý như:

Kiểu phản hồi

* Kiểu phản hồi: Loại phản hồi, mặc định là JSON.

Đường dẫn dữ liệu

* Đường dẫn dữ liệu: Lấy đường dẫn của dữ liệu mong muốn. Ví dụ, khi phản hồi trả về dữ liệu:

json

Copy

```
{
  "status": 200,
  "data": {
    "name": "Prices",
    "values": [
      { "id": 1, "value": 4000 },
      { "id": 2, "value": 24000 }
    ]
  }
}
```

Trường hợp bạn muốn lấy giá trị của mảng values, sử dụng cú pháp data.values. Để lấy giá trị đầu tiên của mảng values, sử dụng cú pháp data.values.0. Nếu bạn muốn lấy tất cả giá trị được trả về như trên để dùng, để nguyên trường Data path.

Gán cho biến

* Gán cho biến: Có thể gán giá trị vào một biến.
* Tên biến: Tên biến để gán giá trị. Trường này xuất hiện khi bạn chọn gán cho biến.

Chèn vào bảng

{% embed url="https://www.youtube.com/watch?v=lQGtzQgZ5k4" %}

* Chèn vào bảng: Có thể chèn giá trị vào cột trong bảng.
* Chọn cột: Cột nơi giá trị được chèn. Trường này xuất hiện khi bạn chọn chèn vào bảng.
* Thêm hàng bổ sung: Chèn thêm một hàng vào cột trong bảng.
