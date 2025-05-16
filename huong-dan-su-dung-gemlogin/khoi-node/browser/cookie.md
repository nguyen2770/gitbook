---
description: Lấy, đặt hoặc xoá cookie
---

# Cookie

Lấy cookie

Bạn có thể lấy

* **Tất Cả Cookie**
  * **URL** URL mà cookie cần lấy
* **Cookie nhất định**: lấy một cookie chỉ định bằng
  * **Tên** Tên của cookie cần lấy. Trường này là tùy chọn khi bạn không chọn "Tất cả cookie"
  * **URL** URL mà cookie cần lấy
* **Gán cho biến** Ghi tên của biến mà bạn muốn gán cookie. Trường này là tuỳ chọn khi chọn "Gán cho biến"
* **Chèn vào bảng**
  * **Tên** Gán cookie cho một cột trong bảng. Trường này là tuỳ chọn khi chọn "Chèn vào bảng"

### Đặt Cookie <a href="#dat-cookie" id="dat-cookie"></a>

Bạn có thể đặt cookie bằng cách

* **Không sử dụng định dạng JSON**: Mặc định là bạn sẽ không chọn định dạng JSON thì bạn sẽ cần hoàn thiện các ô điền bên dưới
  * **URL** Đại diện cho URL yêu cầu để liên kết với cookie. Giá trị này có thể ảnh hưởng đến giá trị tên miền và đường dẫn mặc định của cookie đã tạo.
  * **Value** Giá trị cookie
  * **Path** Đường dẫn của cookie
  * **Value** Giá trị cookie
  * **Domain** Đại diện cho miền của cookie
  * **sameSite** Giá trị cho biết trạng thái SameSite của cookie. Các giá trị có thể `lax`, `strict` hoặc bạn có thể để trống.
  * **Expiration Date** Biểu thị ngày hết hạn của cookie dưới dạng số giây
  * **httpOnly** Đặt cookie dưới dạng [http](https://viblo.asia/p/tim-hieu-ve-http-hypertext-transfer-protocol-bJzKmgewl9N)
  * **secure** Đặt cookie dưới dạng [secure](https://filegi.com/tech-term/secure-cookie-7031/)
* **Sử dụng định dạng JSON**: Khi bạn chọn sử dụng định dạng JSON thì sẽ hiện một trình sửa, bạn có thể điền các dữ liệu dưới dạng [JSON](https://topdev.vn/blog/json-la-gi/)

### Xoá cookies <a href="#xoa-cookies" id="xoa-cookies"></a>

Bạn có thể xoá cookie bằng theo lựa chọn như

* **Không chọn Tất cả cookie**
  * **URL** Đại diện cho URL được liên kết với cookie
  * **Tên** Tên của cookie cần xóa
* **Tất cả cookie**: Xoá tất cả cookie

\


{% embed url="https://www.youtube.com/watch?v=uyjVKpbQwww" %}
