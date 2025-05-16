---
description: Thêm logic của điều kiện vào quy trình
---

# Conditions

Khi node được thực thi, nó sẽ kiểm tra mỗi điều kiện được bạn thêm vào. Nếu nó khớp với điều kiện, quy trình sẽ thực hiện node được kết nối với đầu ra của điều kiện. Nếu nó không khớp, quy trình sẽ thực thi với node được kết nối với đầu ra

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FP6PS3Nda1LHz9nsi5slp%252Fimage.png%3Falt%3Dmedia%26token%3De029de67-6b86-4dbd-850d-7ea2dd72fea0\&width=768\&dpr=4\&quality=100\&sign=14321e0c\&sv=2)

Tạo điều kiện cho phép bạn xây dựng các câu lệnh điều kiện trong quy trình của mình. Nó có thể được sử dụng để kiểm soát luồng bằng cách sử dụng node `Điều kiện` hoặc `Lặp điều kiện`. Bạn có thể thêm node điều kiện bằng cách nhấn vào nút bấm `Thêm điều kiện`. Ngoài ra bạn còn có thể thêm nhiều điều kiện dưới dạng

* **Và**: Thoả mãn `tất cả` các điều kiện được đưa ra mới được thực hiện node nối với đường ra `Path 1`
* **Hoặc**: Thoả mãn `1 trong` các điều kiện được đưa ra mới được thực hiện node nối với đường ra `Path 1`

#### Kiểu dữ liệu so sánh[​](https://docs.omnilog.in/reference/condition-builder.html#kieu-du-lieu-so-sanh) <a href="#kieu-du-lieu-so-sanh" id="kieu-du-lieu-so-sanh"></a>

**Value**[**​**](https://docs.omnilog.in/reference/condition-builder.html#value)

Đối với giá trị bạn muốn so sánh, bạn có thể viết biểu thức bên trong trường văn bản.**Value**: các loại giá trị thông thường như chữ, số,...

*   Tiền tố giá trị: Tiền tố này là quy ước dùng để chỉ ra kiểu dữ liệu của một giá trị. Nó có thể được sử dụng để chuyển đổi một giá trị sang kiểu dữ liệu tương ứng. Ví dụ: tiền tố "string::" có thể được sử dụng để chuyển đổi một giá trị thành một loại chuỗi và "number::" có thể được sử dụng để chuyển đổi một giá trị thành loại số. Bạn có thể thêm các tiền tố sau:

    * `string::`: chuyển đổi giá trị thành chuỗi.
    * `json::`: chuyển đổi giá trị thành JSON.
    * `number::`: chuyển đổi giá trị thành số.
    * `boolean::`: chuyển đổi giá trị thành boolean.

    ![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FfPSLbtq5YTkHWVcAsz9C%252Fimage.png%3Falt%3Dmedia%26token%3D33de1d36-fdf6-4cd9-ad15-2a22e4aabeaf\&width=768\&dpr=4\&quality=100\&sign=7c85c633\&sv=2)

**Data exist**: Kiểm tra xem dữ liệu có tồn tại hay không.

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FdmJXGaKKcyjFWb6DOkdf%252Fimage.png%3Falt%3Dmedia%26token%3De89e8345-ca4b-4596-92c4-5666d59ddd6e\&width=768\&dpr=4\&quality=100\&sign=4d0a4fcd\&sv=2)

**Element**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element)

Sử dụng bộ chọn để lấy CSS selector hoặc XPath của phần tử

**Element text**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element-text)

* So sánh một phần tử văn bản dựa trên CSS selector hoặc XPath của phần tử đó
  * **So sánh với**: [value](https://manual-gemlogin-vn.gitbook.io/gemlogin/editor/5-control-flow/conditions#value), element text, [element attribute value](https://manual-gemlogin-vn.gitbook.io/gemlogin/editor/5-control-flow/conditions#value)

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FpfzceOaTiahtFblQMnOb%252Fimage.png%3Falt%3Dmedia%26token%3D9742e78f-112f-4193-97d4-3d27885e9b7d\&width=768\&dpr=4\&quality=100\&sign=ff3ebcbe\&sv=2)

**Element exist**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element-exist)

* Kiểm tra phần tử `có` tồn tại thông qua CSS selector hoặc XPath của phần tử đó.

**Element not exist**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element-not-exist)

* Kiểm tra phần tử `không` tồn tại thông qua CSS selector hoặc XPath của phần tử đó.

**Element visible**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element-visible)

* Kiểm tra phần tử `có hiển thị` thông qua CSS selector hoặc XPath của phần tử đó

**Element visible in screen**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element-visible-in-screen)

* Kiểm tra phần tử `có hiển thị trên màn hình` thông qua CSS selector hoặc XPath của phần tử đó

**Element hidden in screen**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element-hidden-in-screen)

* Kiểm tra phần tử `không hiển thị trên màn hình` thông qua CSS selector hoặc XPath của phần tử đó

**Element attribute value**[**​**](https://docs.omnilog.in/reference/condition-builder.html#element-attribute-value)

* So sánh giá trị thuộc tính với các giá trị value, element text, element attribute value.

#### Kiểu so sánh[​](https://docs.omnilog.in/reference/condition-builder.html#kieu-so-sanh) <a href="#kieu-so-sanh" id="kieu-so-sanh"></a>

**Basic**[**​**](https://docs.omnilog.in/reference/condition-builder.html#basic)

* **Equal**: so sánh `bằng` giữa hai vế phân biệt hoa, thường. Ví dụ: `Minh` không bằng `minh`
* **Equal(case insensitive)**: so sánh không phân biệt hoa, thường. Ví dụ: `Minh` bằng `minh`
* **Not equal**: so sánh sự khác nhau giữa hai vế.

**Number**[**​**](https://docs.omnilog.in/reference/condition-builder.html#number)

* **Greater than**: so sánh vế trên lớn hơn vế dưới
* **Greater than or equal**: so sánh vế trên lớn hơn hoặc bằng vế dưới
* **Less than**: so sánh vế trên nhỏ hơn vế dưới
* **Less than or equal**: so sánh vế trên nhỏ hơn hoặc bằng vế dưới

**Text**[**​**](https://docs.omnilog.in/reference/condition-builder.html#text)

* **Contains**: kiểm tra không phân biệt chữ hoa thường của vế trên chứa văn bản vế dưới.

-Ví dụ: `google.com` không nằm trong `goOgle.com/abc`

* **Contains (case insensitive)**: so sánh không phân biệt chữ hoa thường vế trên chứa vế dưới.

-Ví dụ: `goOgle.com` nằm trong `goOgle.com/abc`

* **Not contains**: so sánh phân biệt chữ hoa thường vế trên không nằm trong vế dưới.

-Ví dụ: `google.com` không nằm trong `goOgle.com/abc`

* **Not contains (case insensitive)**: so sánh phân biệt chữ hoa thường vế trên không nằm trong vế dưới.

-Ví dụ: `google.com` không nằm trong `goOgle2.com/abc`

* **Starts with**: so sánh phân biệt hoa thường văn bản ở vế trên có bắt đầu với cụm từ ở vế dưới không.

-Ví dụ: `gooleMe.com` bắt đầu bằng cụm từ `google`

* **Ends with**: so sánh phân biệt hoa thường văn bản ở vế trên có kết thúc với cụm từ ở vế dưới không.

-Ví dụ: `gooleMe.com` bắt đầu bằng cụm từ `com`

* **Match with RegEx**: so sánh phân biệt hoa thường văn bản ở vế trên có trùng khớp với RegEx bên dưới vế dưới không.

-Ví dụ: `123456` trùng khớp với đoạn RegEx `\b[0-9]{6}\b`

**Boolean**[**​**](https://docs.omnilog.in/reference/condition-builder.html#boolean)

* **Is truthy**: Giá trị nhập khi chuyển đổi sang giá trị boolean là true. Ví dụ: `abc` là giá trị Truthy
* **Is falsy**: Giá trị nhập khi chuyển đổi sang giá trị boolean là false. Ví dụ: `number::0` là giá trị Falsy

Chú ý

Để phân biệt đâu là các giá trị Truthy hay Falsy thì xem tại [đây](https://viblo.asia/p/boolean-trong-javascript-E375zPQ1ZGW#_2-tim-hieu-ve-truthy-va-falsy-1)
