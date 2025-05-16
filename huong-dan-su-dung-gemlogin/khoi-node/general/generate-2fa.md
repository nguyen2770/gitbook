---
description: Tạo code 2FA từ secret key.
---

# Generate 2FA

Block Generate 2FA được sử dụng với mục đích chính là sinh ra code tương ứng với [2FA secret key](https://en.wikipedia.org/wiki/Universal_2nd_Factor) (Totp) tại thời điểm đó.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252Fsg9vfHrb8FYer8xyH0Yb%252Fimage.png%3Falt%3Dmedia%26token%3D82f31b8e-655d-40f7-9d6a-5add2fc85e92&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=b0c935b7&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Để lấy được code từ 2FA secret kekey, trong phần thuộc tính cần chỉ định thông tin sau:

* 2FA secret key input: cho phép bạn chỉ định 2fa secret key dùng để lấy code.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FaUjGVszHm27ZYWmZZde3%252Fimage.png%3Falt%3Dmedia%26token%3D1fbd4ac2-67f5-4092-b45c-ed41b44a166e&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=c8f7a820&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Assign to variable: cho phép bạn chỉ định tên biến được dùng để lưu code tương ứng với 2fa secret key tại thời điểm lấy.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FNS7ncVWCGr5YmzFrWlR3%252Fimage.png%3Falt%3Dmedia%26token%3D60aca765-9f54-41d7-a28e-c292cdf1d7e5&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=ab906391&#x26;sv=2" alt=""><figcaption></figcaption></figure>
