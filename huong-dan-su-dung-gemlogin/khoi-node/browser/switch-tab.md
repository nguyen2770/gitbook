---
description: Chuyển sang một tab khác và đặt tab đó làm tab hoạt động
---

# Switch Tab

Block này sẽ hỗ trợ việc tìm kiếm và chuyển tab được điều khiển. Trên trình duyệt, các tab sẽ được xác định bởi index, title và url mà nó đang mở tới, do đó GemLogin cung cấp lựa chọn để tìm kiếm theo các thông tin này của tab

Block switch tab hỗ trợ các cách tìm kiếm tab cần được chuyền như sau:

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FgUfxcsh0dj1434HfhDL9%252Fimage.png%3Falt%3Dmedia%26token%3D2d25b9ec-442b-47b2-b075-8166ffccad0d&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=285a1896&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Match patterns: Lựa chọn này cho phép tìm kiếm tab cần chuyển dựa vào url của tab đó. Bằng việc nhập vào một phần url của tab cần chuyển, block này sẽ tìm tab có url tương ứng và chuyển vào tab đó. Chế độ tìm này còn cho phép mở một tab mới nếu url cần tìm kiếm không được tìm thấy bởi tab nào.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FQ6wgeNiYoAMr6ozCwQAw%252Fimage.png%3Falt%3Dmedia%26token%3D760c4484-684d-4d2b-9bc8-9a3ef30e8fa1&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8edfeb8f&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Tab title: Lựa chọn này cho phép tìm kiém tab cần chuyển dựa vào title của tab. GemLogin sẽ tìm kiếm tab có title giống với title được chỉ định và chuyển tới tab đó nếu thấy.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FG0NHagS3AwQu5lrffA1W%252Fimage.png%3Falt%3Dmedia%26token%3Da1533f3f-672e-4598-aeda-de5f19ec8cb8&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=c680d115&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Tab index/Next tab/Previous tab: Lựa chọn này cho phép chuyển tab dựa vào index của tab. Tab index sẽ cho phép nhập index của tab cần chuyển, Next tab sẽ cho phép chuyển vào tab có index của active tab + 1; ngược lại vói Previous tab sẽ chuyển vào tab có index của active tab - 1.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FzBRnc8EqFN5GhqjTq8y5%252Fimage.png%3Falt%3Dmedia%26token%3D42e10e6f-f2c1-4df3-9a37-0a29a34d76a9&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=a8b6eee8&#x26;sv=2" alt=""><figcaption></figcaption></figure>
