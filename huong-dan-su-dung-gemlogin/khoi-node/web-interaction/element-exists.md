---
description: Kiểm tra một phần tử tồn tại trong tab hoạt động hay không
---

# Element Exists

Block element exist là công cụ phục vụ việc kiểm tra sự tồn tại của một phần tử bằng cách kiểm tra liệu css selector/xpath có thể tìm thấy phần tử trên trang web hiện tại hay không.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FOqT1uCy9YFsuOU1twMEq%252Fimage.png%3Falt%3Dmedia%26token%3Dc284e27d-73e4-48d2-8022-0d9f7380ede9&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=72d8ca4d&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Nếu phần tử tồn tại, GemLogin sẽ đi tiếp từ nhánh đúnđúng, ngược lại nếu không tìm thấy phần tử, GemLogin sẽ tiếp tục thực hiện từ nhánh sai - fallout.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F6rBBSIIKKS5bow3xUgFB%252Fimage.png%3Falt%3Dmedia%26token%3D6c6b2dfb-9eac-46ec-a688-32820598314c&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=502f88a0&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Phục vụ cho mục đích đó, trong thuộc tính của block element exist sẽ cung cấp các input với ý nghĩa như sau:

* Css selector/Xpath: Cho phép chỉ định phần tử cần tìm thấy dựa vào css selector/xpath được nhập

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F87IK8I400tVo6yNtlVdP%252Fimage.png%3Falt%3Dmedia%26token%3D9d38707c-c5da-4e90-a3f4-0f483bb7bae3&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8e5f8af1&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Try for/Timeout: Cho phép chỉ định số lần tìm kiếm nếu không tìm thấy phần tử. Block nếu không tìm thấy phần tử sẽ tìm thêm số lần được nhập trong try for, mỗi lần dừng khoảng thời gian timeout giữa mỗi lần kiểm tra

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FaGbSoZWAs7MCZ4nB3dZB%252Fimage.png%3Falt%3Dmedia%26token%3D86903935-5bb2-49ba-926a-3c7ce6b69e3d&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=9a70ba85&#x26;sv=2" alt=""><figcaption></figcaption></figure>

{% embed url="https://youtu.be/81HTSynD1Ws" %}
