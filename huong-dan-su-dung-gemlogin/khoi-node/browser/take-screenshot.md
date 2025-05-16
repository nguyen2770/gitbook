---
description: Chụp ảnh màn hình trên tab đang hoạt động
---

# Take Screenshot

Block Take Screenshot được sử dụng với mục đích là chụp lại ảnh thuộc tab đang hoạt động. Block cho phép người dùng lưu ảnh được chụp vào một thư mục được chỉ định hoặc lưu ảnh dưới dạng base64 vào biến/bảng tùy theo lựa chọn.

Trên GemLogin, block Take Screenshot hỗ trợ chụp ảnh trong các nguồn sau:

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FqnDXhOMAyrtL8ygwrLNw%252Fimage.png%3Falt%3Dmedia%26token%3D24f27c45-94c1-47ae-95e4-9340a2dfd39f&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=bfc95a6c&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Chụp nội dung đang được hiển thị hiện tại của trang (A page): Lựa chọn này sẽ chụp nội dung đang được hiển thị của trang vào trả về cho người dùng.
* Chụp nội dung đang được hiển thị của toàn bộ trang đang được mở (Full page): Lựa chọn này sẽ chụp nội dung đang được hiển thị của trang, kể cà những phần hiện tại đang không được hiển thị và cần phải cuộn xuống mới được hiển thị.
* Chụp nội dung đang được hiển thị của một phần tử (An element): Lựa chọn này sẽ chụp nội dung đang được hiển thị của phần tử và trả về ảnh cho người dùng.

Sau khi chỉ định nguồn của ảnh được chụp, bạn có thể chỉ định vị trí lưu ảnh hoặc gán nội dung ảnh vào biến/bảng dưới dạng base64:

* Save screenshot to computer: Lựa chọn này cho phép chỉ định thư mục lưu ảnh; đồng thời bạn có thể chỉ định định dạng của ảnh muốn lưu, GemLogin hỗ trợ 2 định dạng phổ biến là jpg (bạn có thể chỉ định chất lượng của ảnh muốn lưu với jpg) và png
* Insert screenshot to table/Assign to variable: Lựa chọn nà cho phép bạn chèn vào bảng/gán vào biến nội dung ảnh dưới dạng base64 để có thể sử dụng ở các phần khác của workflow.
