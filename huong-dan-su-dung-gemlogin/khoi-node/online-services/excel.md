# Excel

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252Ft3dpoVCfdoHfjaVeE5Ic%252Fimage.png%3Falt%3Dmedia%26token%3D13e655b5-cd81-4991-a55c-f59430ab6540\&width=768\&dpr=4\&quality=100\&sign=a0f168a6\&sv=2)

#### File[​](https://docs.omnilog.in/blocks/spreadsheet.html#file) <a href="#file" id="file"></a>

Chọn đường dẫn file excel trong máy tính

#### Phạm vi[​](https://docs.omnilog.in/blocks/spreadsheet.html#pham-vi) <a href="#pham-vi" id="pham-vi"></a>

Phạm vi giá trị của các ô mà bạn muốn lấy, cập nhật hoặc xoá. Bạn có thể xác định phạm vi ô bằng cách sử dụng Kí hiệu A1 like `Sheet1!A1:B2` hoặc `A1:B2` hoặc `A1` (viết ngắn gọn của `A1:A1`)

#### Lấy giá trị ô bảng tính[​](https://docs.omnilog.in/blocks/spreadsheet.html#lay-gia-tri-o-bang-tinh) <a href="#lay-gia-tri-o-bang-tinh" id="lay-gia-tri-o-bang-tinh"></a>

Lấy giá trị các ô của bảng tính của 1 file excel

* **Khoá Tham chiếu** Dùng để định danh dữ liệu đọc được. Tham chiếu từ các khối sử dụng như Lặp dữ liệu, Xuất dữ liệu, ...
* **Sử dụng hàng đầu tiên làm từ khoá** Sử dụng hàng đầu tiên của bảng tính làm khoá đối tượng.

Ví dụ khi bạn có một bảng tính như thế này.

Copy

```
// Khi tắt
[["name", "age"], ["foo", 22], ["bar", 23]]

// Khi bật
[{ "name": "foo", "age": 22 }, { "name": "bar", "age": 23 }]
```

#### **Tên cột dùng làm khoá chính** <a href="#ten-cot-dung-lam-khoa-chinh" id="ten-cot-dung-lam-khoa-chinh"></a>

Trong trường hợp bạn muốn dùng chính xác dữ liệu với profile đang chạy thì bạn chọn lựa chọn này

Ví dụ khi bạn có một bảng tính như thế này.

profileIdnameage

2

foo

22

3

bar

23

Bạn muốn khi chạy profile có id là 2 thì sẽ dùng giá trị là `foo` thì bạn dùng lựa chọn này, khi đó bạn có thể lấy ra giá trị `foo` bằng biểu thức `{{googleSheets.referenceKey.[profileId].name}}`, khi đó khi chạy profile có id là 2 sẽ lấy ra giá trị `foo`, profile có id là 3 sẽ lấy ra giá trị `bar`

#### Lấy phạm vi bảng tính[​](https://docs.omnilog.in/blocks/google-sheets.html#lay-pham-vi-bang-tinh) <a href="#lay-pham-vi-bang-tinh" id="lay-pham-vi-bang-tinh"></a>

Lấy giá trị phạm vi của bảng tính sau đó gán giá trị đó cho biến hoặc bảng mong muốn

* **Phạm vi bảng tính**
  * **Gán cho biến**: gán phạm vi của dữ liệu cho một biến
  * **Chèn vào bảng**: gán phạm vi của dữ liệu cho một cột

### Cập nhập giá trị ô bảng tính[​](https://docs.omnilog.in/blocks/google-sheets.html#cap-nhap-gia-tri-o-bang-tinh) <a href="#cap-nhap-gia-tri-o-bang-tinh" id="cap-nhap-gia-tri-o-bang-tinh"></a>

**Tuỳ chọn nhập giá trị**[**​**](https://docs.omnilog.in/blocks/google-sheets.html#tuy-chon-nhap-gia-tri)

Xác định cách diễn giải dữ liệu đầu vào, mặc định là `RAW`.

* **RAW**: Các giá trị người dùng đã nhập sẽ không được phân tích cú pháp và sẽ được lưu trữ nguyên trạng.
  * Ví dụ: Giá trị đầu vào là : `"123"` thì định dạng lưu trữ là: `"123"`
* **USER\_ENTERED**: Các giá trị sẽ được phân tích cú pháp như thể người dùng nhập chúng vào giao diện người dùng. Các số sẽ vẫn ở dạng số nhưng các chuỗi có thể được chuyển đổi thành số, ngày, v.v. theo các quy tắc tương tự được áp dụng khi nhập văn bản vào một ô thông qua Giao diện người dùng Google Sheet.
  * Ví dụ giá trị đầu vào là: `"123"` thì định dạng lưu trữ là: `123`

**Dữ liệu từ**[**​**](https://docs.omnilog.in/blocks/google-sheets.html#du-lieu-tu)

Nguồn dữ liệu để cập nhật bảng tính, mặc định là bảng

* **Bảng**: lấy dữ liệu đã được chèn vào bảng
  * **Ghi key vào hàng đầu**: Sử dụng các cột làm hàng đầu tiên trên bảng tính.
* **Tuỳ chỉnh**: dữ liệu được nhập phải là một mảng thuộc kiểu dữ liệu mảng 2 chiều/ma trận tương ứng với dữ liệu cần nhập trong file excel.

Copy

```
[
   ["1","2","3"]
]
```

### Chèn hoặc thêm các giá trị ô bảng tính[​](https://docs.omnilog.in/blocks/google-sheets.html#chen-hoac-them-cac-gia-tri-o-bang-tinh) <a href="#chen-hoac-them-cac-gia-tri-o-bang-tinh" id="chen-hoac-them-cac-gia-tri-o-bang-tinh"></a>

Lấy giá trị phạm vi của bảng tính sau đó gán giá trị đó cho biến hoặc bảng mong muốn

**Tuỳ chọn nhập giá trị**[**​**](https://docs.omnilog.in/blocks/google-sheets.html#tuy-chon-nhap-gia-tri-1)

Xác định cách diễn giải dữ liệu đầu vào, mặc định là `RAW`.

* **RAW**: Các giá trị người dùng đã nhập sẽ không được phân tích cú pháp và sẽ được lưu trữ nguyên trạng.
  * Ví dụ: Giá trị đầu vào là : `"123"` thì định dạng lưu trữ là: `"123"`
* **USER\_ENTERED**: Các giá trị sẽ được phân tích cú pháp như thể người dùng nhập chúng vào giao diện người dùng. Các số sẽ vẫn ở dạng số nhưng các chuỗi có thể được chuyển đổi thành số, ngày, v.v. theo các quy tắc tương tự được áp dụng khi nhập văn bản vào một ô thông qua Giao diện người dùng Google Sheet.
  * Ví dụ giá trị đầu vào là: `"123"` thì định dạng lưu trữ là: `123`

**Chèn tuỳ chọn dữ liệu**[**​**](https://docs.omnilog.in/blocks/google-sheets.html#chen-tuy-chon-du-lieu)

* **OVERWRITE**:
* **INSERT\_ROWS**:

**Dữ liệu từ**[**​**](https://docs.omnilog.in/blocks/google-sheets.html#du-lieu-tu-1)

Nguồn dữ liệu để cập nhật bảng tính, mặc định là bảng

* **Bảng**: lấy dữ liệu đã được chèn vào bảng
  * **Ghi key vào hàng đầu**: Sử dụng các cột làm hàng đầu tiên trên bảng tính.
* **Tuỳ chỉnh**: dữ liệu được nhập phải là một mảng thuộc kiểu dữ liệu mảng 2 chiều/ma trận tương ứng với dữ liệu cần nhập trong file excel.

json

Copy

```
[
    ["1","2","3"]
]
```

### Xoá giá trị ô bảng tính[​](https://docs.omnilog.in/blocks/google-sheets.html#xoa-gia-tri-o-bang-tinh) <a href="#xoa-gia-tri-o-bang-tinh" id="xoa-gia-tri-o-bang-tinh"></a>

Xoá giá trị của bảng tính theo phạm vi đã chọn

#### Truy cập dữ liệu trang tính[​](https://docs.omnilog.in/blocks/google-sheets.html#truy-cap-du-lieu-trang-tinh) <a href="#truy-cap-du-lieu-trang-tinh" id="truy-cap-du-lieu-trang-tinh"></a>

Để truy cập các giá trị bảng tính từ đầu vào của node, bạn có thể sử dụng các biểu thức như cú pháp `{{ googleSheets.referenceKey.path }}`.

* Ví dụ trường hợp lấy dữ liệu từ node Google Sheet với khoá tham chiếu là `data` và dữ liệu trong google sheet như bảng sau

nameage

An

18

Manh

23

Để lấy giá trị `name` của hàng đầu tiên (tương ứng phần tử đầu tiên thuộc mảng dữ liệu kết quả trả về)húng ta dùng cú pháp `{{googleSheets.data.0.name}}`
