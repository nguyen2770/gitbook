---
description: Sử dụng để đọc dữ liệu từ một file text.
---

# Read File Text

Block read file text được sử dụng với mục đích chính để lấy dữ liệu từ file text. GemLogin hỗ trợ 2 chế độ đọc: đọc từng dòng một và đọc toàn bộ file text.

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F9z1msScnGF4lxymwhRkv%252Fimage.png%3Falt%3Dmedia%26token%3D0856df0a-50c5-45a2-abff-b595c2e8607e\&width=768\&dpr=4\&quality=100\&sign=1e793f5c\&sv=2)

Để lấy dữ liệu từ file text, thuộc tính của block read file text có input như sau:

* File Path: để chỉ định đường dẫn tới file text cần đọc.

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FJ2bhNgRG9WQsW6zojm1P%252Fimage.png%3Falt%3Dmedia%26token%3Dd7c0fde8-6f04-465c-af90-5a23a5016aea\&width=768\&dpr=4\&quality=100\&sign=106ad1da\&sv=2)

* Assign to variable: cho phép chỉ định tên biến lưu dữ liệu đọc từ file text.

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FXnnQR1VUmMJ7BvgDW6Yy%252Fimage.png%3Falt%3Dmedia%26token%3D3704b847-ed76-44d0-8d9a-e45b9152ecfb\&width=768\&dpr=4\&quality=100\&sign=ee78c026\&sv=2)

*   Mode: cho phép chỉ định chế độ đọc: đọc từng dòng và đọc tất cả các dòndòng

    * Đọc từng dòng: block sẽ chỉ đọc 1 dòng duy nhất trong file text. Block hỗ trợ 2 option là đọc một dòng ngẫu nhiên và xóa dòng được đọc cũng như cho phép điền dấu phân cách để tự động tách kết quả đọc được.

    ![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FxRGRffnioyHHRy9jpjd5%252Fimage.png%3Falt%3Dmedia%26token%3D9df5f4a8-42c9-4dcf-b0dc-3ba0b6ec8908\&width=768\&dpr=4\&quality=100\&sign=ff30d7c3\&sv=2)

    * Đọc tất cả các dòng: tất cả các dòng trong file text sẽ được đọc và trả về dưới dạng mảng, mỗi phần tử trong mảng là một dòng dữ liệu trong file text.

