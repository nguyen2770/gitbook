---
description: Thực hiện đoạn mã Javascript
---

# JavaScript Code

Block js được sử dụng để thực hiện các đoạn mã js trên tab đang được active.

_Lưu ý rằng block sẽ chỉ kết thúc quá trình chạy khi hàm `NextBlock()` được thục hiện. Mặc định, hàm `NextBlock()` sẽ được chèn thêm ở cuối cùng nếu code javascript không gọi tới hàm này. Lưu ý rằng nếu code js trả về sớm (gọi return trước khi gọi `NextBlock()`), GemLogin sẽ không nhận được tín hiệu cần phải thực hiện block tiếp theo khi gọi hàm `NextBlock()` dẫn tới lỗi timeout._

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FsGpUrWV74k7FUjpHCDEc%252Fimage.png%3Falt%3Dmedia%26token%3Df98797ec-1932-4c69-87b5-48e416414205&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=24a4583e&#x26;sv=2" alt=""><figcaption></figcaption></figure>

### Thời gian chạy tối đa cho phép[​](https://docs.omnilog.in/blocks/javascript-code.html#thoi-gian-cho) <a href="#thoi-gian-cho" id="thoi-gian-cho"></a>

Timeout được sử dụng để chỉ định thời gian tối đa mà block javascript được phép thực hiện. Nếu thời gian thực hiện vượt qua thời gian chạy tối đa cho phép, mặc dù đoạn code js vẫn chạy trên console nhưng GemLogin sẽ ngừng chờ tín hiệu từ đoạn code js để thực hiện block tiếp theo.

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F8gBJVBqAf1p1iAdbt1vb%252Fimage.png%3Falt%3Dmedia%26token%3Dac1dec97-100c-47a4-8fe3-6e3f867fc4fb\&width=768\&dpr=4\&quality=100\&sign=6b61ddcf\&sv=2)

### Mã Javascript <a href="#ma-javascript" id="ma-javascript"></a>

Trên GemLogin, trong mã javascript, bạn có thể sử dụng các hàm sau để lấy/đặt giá trị của biến bên ngoài đoạn code js:

`RefData(source, path)`

RefData là được dùng để lấy dữ liệu trong đoạn mã javascript. Nó yêu cầu các tham số có ý nghĩa như sau:

* Source - Nguồn dữ liệu: Nguồn chứa dữ liệu cần lấy. Truy cập [biểu thức](https://manual-gemlogin-vn.gitbook.io/gemlogin/huong-dan-su-dung-gemlogin/du-lieu/bieu-thuc) để biết các nguồn bạn có thể lấy dữ liệu được.
* Path - Đường dẫn: Tham số này chỉ định đường dẫn tới giá trị mà bạn cần lấy.

`SetVariable(variableName, newValue)`

Hàm SetVariable được dùng để tạo/đặt giá trị cho biến. Hàm yêu cầu 2 tham số:

* variableName - tên biến: Chỉ định tên biến sẽ được dùng để tạo/đặt.
* newValue - giá trị mới: Chỉ định giá trị mới sẽ được dùng để gán cho biến.

`NextBlock()`

NextBlock được dùng để thông báo rằng code js đã được thực hiện xong và có thể tiếp thực hiện các block tiếp theo. Lưu ý gọi hàm này để đảm bảo script chạy ổn định.

### Thực thi trước khi trang tải xong[​](https://docs.omnilog.in/blocks/javascript-code.html#thuc-thi-moi-tab-moi) <a href="#thuc-thi-moi-tab-moi" id="thuc-thi-moi-tab-moi"></a>

Lựa chọn này cung cấp cho bạn một lựa chọn để thực hiện đoạn code js trước khi trang được tải hoàn thiện.

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FOAR60HnWYDFtrJsfndgg%252Fimage.png%3Falt%3Dmedia%26token%3D98cbfee9-0992-4b2c-95b3-e926e2cf3638\&width=768\&dpr=4\&quality=100\&sign=4ad75ed8\&sv=2)

{% embed url="https://youtu.be/a2Jicy-PNv4" %}
