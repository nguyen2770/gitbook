---
description: >-
  Biến được sử dụng để lưu trữ giá trị và bạn có thể truy cập giá trị này trong
  suốt luồng công việc. Khi lưu giá trị cho một biến bạn chỉ cần ghi tên biến mà
  bạn muốn nhận giá trị đó.
---

# Biến

### Tên biến[​](https://docs.omnilog.in/workflow/variables.html#ten-bien) <a href="#ten-bien" id="ten-bien"></a>

Bạn có thể đặt tên biến thành bất cứ thứ gì bạn muốn. Nhưng để truy cập biến dễ dàng hơn, không sử dụng dấu cách, ký tự như (@) và ngoặc vuông (\[]) trong tên biến.

### Truy cập biến[​](https://docs.omnilog.in/workflow/variables.html#truy-cap-bien) <a href="#truy-cap-bien" id="truy-cap-bien"></a>

**Cú pháp**[**​**](https://docs.omnilog.in/workflow/variables.html#cu-phap)

Bạn có thể truy cập giá trị của biến được tạo ra trong khi chạy một kịch bản bất kỳ.

### Chuyển kiểu dữ liệu của biến thành mảng[​](https://docs.omnilog.in/workflow/variables.html#chuyen-kieu-du-lieu-cua-bien-thanh-mang) <a href="#chuyen-kieu-du-lieu-cua-bien-thanh-mang" id="chuyen-kieu-du-lieu-cua-bien-thanh-mang"></a>

Khi bạn sử dụng tiền tố `$push`, Automation sẽ thay đổi kiểu dữ liệu của biến thành một mảng. Nếu biến đã có giá trị, giá trị đó sẽ trở thành phần tử đầu tiên của mảng. Và khi bạn gán giá trị cho biến, thay vì thay thế giá trị biến, Automation sẽ đẩy giá trị đó vào biến.

Giả sử bạn lặp qua các phần tử. Bạn muốn lấy văn bản của phần tử bằng cách sử dụng node Lấy văn bản và đặt văn bản của phần tử vào một biến với tiền tố `$push` như `$push:texts`. Ở lần lặp đầu tiên, giá trị của biến `texts` sẽ là `["Text 1"]` ở lần lặp thứ hai là `["Text 2"]` và cứ tiếp tục như vậy.

Ví dụ dưới đây sẽ giúp các bạn hiểu rõ hơn

Trường hợp 1 chúng ta sẽ chèn giá trị văn bản `bien1` và `bien2` vào biến `texts` trong node `Chèn dữ liệu`

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FRtyuz61C2ho2m1UE2lP0%252Fimage.png%3Falt%3Dmedia%26token%3D0a5a26a4-9dca-4f9c-b699-67c5419d96fc\&width=768\&dpr=4\&quality=100\&sign=a66a63d7\&sv=2)

Các biến được lưu trữ dưới dạng một đối tượng với tên biến là khóa đối tượng.

Ví dụ:

Copy

```
{
  "url": "https://google.com",
  "numbers": [100, 500, 300, 200, 400]
}
```

* Lấy giá trị của biến `url`

`->` Dùng biểu thức: `{{ variables.url }}`

`->` Kết quả đầu ra: `https://google.com`

* Lấy giá trị của biến `numbers`

`->` Dùng biểu thức: `{{ variables.numbers }}`

`->` Kết quả đầu ra: `[100, 500, 300, 200, 400]`

* Lấy giá trị đầu tiên của biến `numbers`.

`->` Dùng biểu thức: `{{ variables.numbers.0 }}`

`->` Kết quả đầu ra: `100`
