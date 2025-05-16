---
description: >-
  Cho phép bạn thực hiện lặp lại các hành động tương tự và chỉ dừng lặp sau khi
  đã lặp tất cả các dữ liệu.
---

# Vòng lặp dữ liệu

Vòng lặp rất hữu ích khi bạn muốn xử lý nhiều mục tương tự, chẳng hạn như điền vào biểu mẫu có giá trị lấy từ Google Sheets. Có một số cách để thực hiện vòng lặp trong Automation:

1. Dùng Lặp Dữ Liệu để lặp qua cột dữ liệu, số đếm, Google Sheets, biến, bảng, dữ liệu tuỳ chỉnh, các phần tử.
2. Dùng Lặp Phần Tử node để lặp qua các phần tử trên trang.
3. Dùng Lặp Lại Số Lần để lặp lại các hành động với một số lần nhất định.

### Sử dụng node Lặp Dữ Liệu hoặc node Lặp Phần Tử[​](https://docs.omnilog.in/workflow/looping.html#su-dung-node-lap-du-lieu-hoac-node-lap-phan-tu) <a href="#su-dung-node-lap-du-lieu-hoac-node-lap-phan-tu" id="su-dung-node-lap-du-lieu-hoac-node-lap-phan-tu"></a>

Khi sử dụng Lặp Dữ Liệu hoặc Lặp Phần Tử, node Dừng Lặp phải bao gồm trong quy trình. Điểm dừng vòng lặp dùng để cho kịch bản công việc biết phạm vi của vòng lặp. Và bên trong Điểm dừng vòng lặp, bạn cũng phải nhập ID vòng lặp tương ứng với node vòng lặp đang sử dụng.

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FeVXkrUAjqIqI2lZqItAc%252Fimage.png%3Falt%3Dmedia%26token%3D2160f444-d48a-44c8-b263-fe61a723f23d\&width=768\&dpr=4\&quality=100\&sign=f01b1b3c\&sv=2)

Quy trình ở trên sẽ thực thi node `Click chuột` và `Tải nội dung` trong mỗi lần lặp dữ liệu và số lần lặp sẽ phụ thuộc vào số lần người dùng muốn lặp. Sau khi lặp qua tất cả dữ liệu đầu vào thì kịch bản sẽ thực hiện node `Cuộn chuột`

Và khi bạn không xác định phạm vi vòng lặp bằng node `Dừng lặp`, vòng lặp sẽ không hoạt động.

### Truy Cập Một Phần Tử Khi Lặp[​](https://docs.omnilog.in/workflow/looping.html#truy-cap-mot-phan-tu-khi-lap) <a href="#truy-cap-mot-phan-tu-khi-lap" id="truy-cap-mot-phan-tu-khi-lap"></a>

Bạn có thể sử dụng biểu thức `{{loopData.loopId}}` để truy cập dữ liệu từ lần lặp hiện tại bên trong phạm vi vòng lặp.

Ví dụ: thay thế `loopId` bằng ID vòng lặp là `loop` mà bạn đã nhập bên trong node `Lặp dữ liệu`để lấy giá trị của `name` trong vòng lặp và sử dụng dữ liệu đó trong node `Nhấn phím`

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252Fq4JGzprDrpPxmHkSbgbP%252Fimage.png%3Falt%3Dmedia%26token%3D37e32b3b-f0dd-4964-b56d-7fe592905db4\&width=768\&dpr=4\&quality=100\&sign=9b2f24af\&sv=2)

Biểu thức `{{loopData.loop}}` sẽ trả về dạng như sau:

Copy

```
{
  "data": ...,
  "$index": 1
}
```

Vì vậy, nếu bạn muốn truy cập vào thứ tự một lần lặp của vòng lặp, bạn có thể sử dụng [biểu thức](https://docs.omnilog.in/workflow/expressions.html) như `{{loopData.loopId.$index}}` Và để có được giá trị vòng lặp, bạn không cần phải viết `data` kiểu như `{{loopId.loopId.data}}` Automation sẽ tự động gán nó cho các biểu thức. Nhưng nếu bạn sử dụng biểu thức JavaScript, bạn phải bao gồm thuộc tính `data` kiểu như `!!{{loopData.loopId.data}}`

### Sử dụng node Repeat Task-Lặp lại số lần[​](https://docs.omnilog.in/workflow/looping.html#su-dung-node-lap-lai-so-lan) <a href="#su-dung-node-lap-lai-so-lan" id="su-dung-node-lap-lai-so-lan"></a>

Sử dụng node Lặp Lại Số Lần là cách dễ nhất để lặp lại, bạn chỉ cần xác định số lần lặp lại các hành động và bắt đầu lựa chọn vị trí mà bạn muốn lặp lại chúng.

Ví dụ: Quy trình bên dưới sẽ thực hiện node `Click` sau đó lặp lại node đó thêm 2 lần nữa rồi mới thực hiện các node tiếp theo

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FcQedlTMZY2VbHvOu5t0e%252Fimage.png%3Falt%3Dmedia%26token%3De070aab3-1784-483a-a253-bbe32150b86c\&width=768\&dpr=4\&quality=100\&sign=5bc7d17c\&sv=2)
