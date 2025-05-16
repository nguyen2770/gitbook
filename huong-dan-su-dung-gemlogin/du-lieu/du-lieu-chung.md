---
description: >-
  Dữ liệu được lưu trữ trong quy trình và có thể sử dụng ở mọi nơi trong phạm vi
  kịch bản. Bạn có thể dùng dữ liệu được lưu trữ trong Dữ liệu chung để sử dụng
  ở loại kiểu kịch bản
---

# Dữ liệu chung

#### Dữ liệu đơn <a href="#du-lieu-don" id="du-lieu-don"></a>

Ví dụ: bạn có nhiều node Mở liên kết trong đó đầu vào URL có cùng một miền: "[https://www.etsy.com/](https://www.etsy.com/)". Thay vì chỉnh sửa từng node một để thay đổi miền URL, bạn có thể xác định miền URL trong dữ liệu chung như:

```json
{
  "url": "https://www.etsy.com/"
}
```

Và truy cập dữ liệu chung bên trong trường văn bản URL của node Mở liên kết bằng cách sử dụng biểu thức.

Ví dụ: `{{globalData.url}}`

### Dữ liệu phức tạp <a href="#du-lieu-phuc-tap" id="du-lieu-phuc-tap"></a>

Ví dụ: bạn có một dữ liệu gồm danh sách user, pass của hàng loạt tài khoản Google và muốn đăng nhập mỗi tài khoản khác nhau với một profile khác nhau. Để làm được điều đó bạn hãy làm theo các bước sau.

Đầu tiên bạn cần chuẩn bị một file dữ liệu Googlesheet or Excel gồm các cột `ProfileId`, `User` , `Pass` như sau:

\
![](<../../.gitbook/assets/image (36).png>)

Sau đó các bạn sử dụng cú pháp

`{{`googleSheets. Data1`.[profileId].User}}` khi nhập User của tài khoản

`{{`googleSheets Data1`.[profileId].Pass}}`khi muốn nhập Pass của tài khoản

( Data1: là Reference key của file Googlesheet )

`[profileId] là id mặc định của profile`

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

⇒ Kết quả trả về: Dữ liệu User/ Pass tương ứng với profile id sẽ được nhập vào các tài khoản tự động.

Ví dụ: Ghi xuất dữ liệu theo profileid hàng loạt trên file Excel

Ví dụ: Ghi xuất dữ liệu hàng theo profileid hàng loạt trên file txt

{% embed url="https://www.youtube.com/watch?v=WunMqIUCbno" %}
