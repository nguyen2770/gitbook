---
description: Thực hiện click chuột vào một phần tử/vị trí trong trình duyêt.
---

# Mouse Click

Block mouse click được dùng để mô phòng hành động click trong trình duyệt vào một phần tử hay vị trí trên trình duyệt. Cần lưu ý rằng phần tử cần được hiển thì trên màn hình thì mới có thể được click bởi block mouse click.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FmcHsCyyeNFNEPCKjLKYf%252Fimage.png%3Falt%3Dmedia%26token%3Ddb3311a8-7ef5-44cf-a058-f34f1ce19dc2&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=eda1c6ee&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Do đó block mouse click sẽ cung cấp các input trong phần thuộc tính như sau để mô phỏng hành động click trên trình duyêt:

* Element/Position input: bạn có thể chọn chế độ tìm phần tử với 1 trong 3 lựa chọn sau: theo css selector, theo xpath hoặc theo tọa độ:

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FZYywmgY4o69n3dLFYuoU%252Fimage.png%3Falt%3Dmedia%26token%3Db83e078e-b042-4bd4-8386-b0c29c6f97e4&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=d24431a2&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* Clicktype: Cho phép cho phép chỉ định kiểu click mà bạn muốn thực hiện trên trình duyệt. GemLogin hỗ trợ các kiểu click như sau: Left click - mô phỏng click bằng chuột trái, Right click - mô phỏng click với chuột phải, Right click - mô phỏng click bằng chuột phải, Double click - mô phỏng click đúp, Press and hold - mô phỏng click và giữ, Release - mô phỏng dừng giữ chuột

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FBZBuIIyBbdirNBgTWPCL%252Fimage.png%3Falt%3Dmedia%26token%3D28158728-a566-44a6-9262-ace274fcbd40&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=340b2368&#x26;sv=2" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=NdSW4oD3IY0" %}

* Human click: Khi lựa chọn này được bật, trước khi click, GemLogin sẽ thực hiện việc di chuyển chuột ngẫu nhiên trước rồi mới click vào phần tử/vị trí cần click

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FoXnfUmhVp9MKGNE23aHB%252Fimage.png%3Falt%3Dmedia%26token%3D3e7daf4d-b1c3-4ccf-a573-58db32591f05&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=a97265f&#x26;sv=2" alt=""><figcaption></figcaption></figure>
