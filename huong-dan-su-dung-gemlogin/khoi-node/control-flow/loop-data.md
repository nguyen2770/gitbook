---
description: >-
  Block này dùng để đánh dấu điểm bắt đầu của một vòng lặp, trong khi block loop
  breakpoint dùng để đánh dấu điểm kết thúc của vòng lặp.
---

# Loop Data

Block loop

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FIvMYw22gEDy4i7igPx88%252Fimage.png%3Falt%3Dmedia%26token%3D6da4a58b-629c-4d49-9f32-cae0bb41fbb2\&width=768\&dpr=4\&quality=100\&sign=b9c73f\&sv=2)

### ID vòng lặp[​](https://docs.omnilog.in/blocks/loop-data.html#id-vong-lap) <a href="#id-vong-lap" id="id-vong-lap"></a>

ID để xác định vòng lặp. Sử dụng Id này khi bạn muốn truy cập dữ liệu vòng lặp bên trong biểu thức hoặc khi dùng node Dừng lặp.

### Dữ liệu duyệt <a href="#lap-qua" id="lap-qua"></a>

Dữ liệu duyệt là dữ liệu mà block loop data được cung cấp để lặp qua - [​](https://docs.omnilog.in/blocks/loop-data.html#lap-qua)

* **Số**: lặp lại

Ví dụ: Lặp lại node `Nhấn phím` theo số đếm từ `1` đến `2` khi dùng vòng lặp `Lặp dữ liệu`

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FTG0MLodrh8naRqN3xFnS%252Fimage.png%3Falt%3Dmedia%26token%3D686fca0f-5a6c-471e-a6d1-eb0619e79eed\&width=768\&dpr=4\&quality=100\&sign=fd203dbf\&sv=2)

* **Biến**: lặp qua các giá trị của biến khi biến có kiểu giá trị mảng.
* **Google Sheets**: lặp qua các dữ liệu được lấy từ đường link của trang chứ dữ liệu trong Google Sheets
* **Dữ liệu tuỳ chỉnh**: Khi bạn chọn dữ liệu tuỳ chỉnh, đảm bảo bạn viết dưới dạng [mảng](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays) dữ liệu kiểu cú pháp [JSON](https://topdev.vn/blog/json-la-gi/).

### Số lần lặp tối đa[​](https://docs.omnilog.in/blocks/loop-data.html#so-lan-lap-toi-%C4%91a) <a href="#so-lan-lap-toi-da" id="so-lan-lap-toi-da"></a>

Tuỳ chỉnh số dữ liệu tối đa muốn lặp, mặc định là 0 sẽ lặp tất cả dữ liệu

### Bắt đầu từ vị trí[​](https://docs.omnilog.in/blocks/loop-data.html#bat-%C4%91au-tu-vi-tri) <a href="#bat-dau-tu-vi-tri" id="bat-dau-tu-vi-tri"></a>

Lặp từ vị trí số 0 tương ứng với vị trí đầu tiên của dữ liệu trong một danh sách

### Tiếp tục quy trình cuối cùng[​](https://docs.omnilog.in/blocks/loop-data.html#tiep-tuc-quy-trinh-cuoi-cung) <a href="#tiep-tuc-quy-trinh-cuoi-cung" id="tiep-tuc-quy-trinh-cuoi-cung"></a>

Khi chọn vào lựa chọn này, dữ liệu sẽ được lặp qua toàn bộ

### Đảo ngược thứ tự vòng lặp[​](https://docs.omnilog.in/blocks/loop-data.html#%C4%91ao-nguoc-thu-tu-vong-lap) <a href="#dao-nguoc-thu-tu-vong-lap" id="dao-nguoc-thu-tu-vong-lap"></a>

Lặp từ phần tử cuối cùng cho đến phần tử đầu tiên trong danh sách dữ liệu

1.
