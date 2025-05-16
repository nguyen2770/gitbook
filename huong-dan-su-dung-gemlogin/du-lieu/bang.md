---
description: >-
  Bảng trong kịch bản công việc được sử dụng để lưu trữ dữ liệu được lấy từ
  ​​một trang web hoặc dữ liệu sinh ra trong khi quá trình chạy kịch bản tự
  động. Trong bảng, mỗi cột là một kiểu dữ liệu nghiêm
---

# Bảng

### Tạo bảng <a href="#tao-bang" id="tao-bang"></a>

Trước khi chèn dữ liệu vào bảng, bạn phải tạo các cột trong bảng. Có tất cả 5 loại dữ liệu mà bạn có thể chọn cho cột `Text`, `Number`, `Boolean`, `Array`, and `Any`.

### Chèn dữ liệu <a href="#chen-du-lieu" id="chen-du-lieu"></a>

Bạn có thể chèn dữ liệu vào bảng bằng cách sử dụng các node được sử dụng để trích xuất dữ liệu từ một trang web, chẳng hạn như Trích Văn Bản và Lấy Thuộc Tính. Để chèn dữ liệu bằng các node đó, hãy nhấn vào node đó, chọn tùy chọn "Chèn vào bảng" và chọn một trong các cột

Ví dụ ở dưới thể hiện một thao tác xuất dữ liệu từ cột `cot1` trong bảng bằng node Xuất dữ liệu. Dữ liệu xuất ra sẽ được chèn vào file `test` với lựa chọn `Thêm vào cuối` khi gặp file đã tồn tại và dữ liệu được lưu dưới dạng `CSV`

VD: Mỗi khi bạn chèn dữ liệu vào bảng, dữ liệu sẽ được đẩy xuống hàng cuối cùng của cột, ví dụ như khi bạn chèn dữ liệu vào bảng như thế này.

| Name | Age | Address   |
| ---- | --- | --------- |
| Anh  | 20  | Hà Nội    |
| Tuấn | 30  | Thái Bình |

Và khi quá trình thực thi diễn ra, node Chèn dữ liệu sẽ chèn dữ liệu vào cột `cot1`. Bảng sẽ như thế này.

| Name | Age | Address   |
| ---- | --- | --------- |
| Anh  | 20  | Hà Nội    |
| Lâm  | 30  | Thái Bình |
| Nam  |     |           |



```json
[
  {
    "name": "Anh",
    "age": 20,
    "address": "Hà Nội", 
  },
  {
    "name": "Lâm",
    "age": 30,
    "address": "Thái Bình", 
  },
  {
    "name": "Hải"
  }
]
```

Ví dụ 2: Chèn dữ liệu bảng vào

Profileid = id profile

Status = Chưa Login

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FV5QiZeZTxIz1EPHLVR67%252Fimage.png%3Falt%3Dmedia%26token%3Dbb0f0b33-6018-4d39-8e44-74e1264730f6\&width=768\&dpr=4\&quality=100\&sign=4ec16edb\&sv=2)

### Xuất Dữ Liệu Trong Bảng <a href="#xuat-du-lieu-trong-bang" id="xuat-du-lieu-trong-bang"></a>

Sử dụng Xuất Dữ Liệu để xuất bảng thành file. Bạn có thể chọn xuất bảng dưới dạng file "Văn bản", "CSV" hoặc "JSON".
