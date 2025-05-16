# Bảng và Biến

### Kiểu Dữ Liệu[​](https://docs.omnilog.in/workflow/table-or-variable.html#_1-kieu-du-lieu) <a href="#id-1-kieu-du-lieu" id="id-1-kieu-du-lieu"></a>

Mỗi cột của bảng là một kiểu dữ liệu nghiêm ngặt, ví dụ khi bạn lấy một đoạn văn bản muốn chèn vào cột `tên` có kiểu dữ liệu `text` thì đoạn văn bản đó sẽ được chuyển thành văn bản trước khi được chèn vào. Trong các biến, nó không liên kết với bất kỳ loại dữ liệu nào, nghĩa là bạn có thể lưu trữ văn bản, số, đối tượng hoặc mảng trong đó.

### Chèn Dữ Liệu[​](https://docs.omnilog.in/workflow/table-or-variable.html#_2-chen-du-lieu) <a href="#id-2-chen-du-lieu" id="id-2-chen-du-lieu"></a>

Bất cứ khi nào chèn một giá trị vào bảng, giá trị sẽ được đẩy đến hàng cuối cùng của cột được chọn.

Ví dụ:

Trước khi chèn giá trị:

| Name     | Price |
| -------- | ----- |
| Áo thun  | 1000  |
| Quần dài | 2000  |

Sau khi chèn giá trị 5500:

| Name     | Price |
| -------- | ----- |
| Áo thun  | 1000  |
| Quần dài | 2000  |
|          | 5500  |
