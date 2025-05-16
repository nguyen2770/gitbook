---
description: >-
  Mô phỏng hành động nhấn phím/tổ hợp phím tới phần tử/tab đang được focus/điều
  khiển.
---

# Presskey

ideoBlock presskey được sử dụng với mục đích chính là mô phỏng hành động nhấn phím trên một phần tử (thường là input) đang được focus hoặc trên trang đang được điều khiển.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F1KdUn2hfwTUuvswcD7bd%252Fimage.png%3Falt%3Dmedia%26token%3Dd4682512-3603-41d1-9369-345b58310cc1&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=ff6e7d3b&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Trên GemLogin, block presskey hỗ trợ 2 chế độ: Press a key và Press multiple keys. Cả 2 chế độ sẽ đều mô phỏng hành động gõ phím tới phần tử và trang được điều khiển.

Để phục vụ mục đích đó, block presskey sẽ cho phép chỉ định các phần sau trong thuộc tính của mình:

* Css selector/Xpath input: Cho phép bạn chỉ định phần tử muốn focus (tùy chọn)

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FqdsXT7zTV8IeaBt1hNDS%252Fimage.png%3Falt%3Dmedia%26token%3D69919e6a-8a6a-4012-b54b-eb1c7c97711a&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=25f4da7&#x26;sv=2" alt=""><figcaption></figcaption></figure>

*   Action: Cho phép bạn chỉ định hành động cần thực hiện. GemLogin hỗ trợ 2 loại action như sau:

    * Nhấn một phím: Cho phép bạn chỉ định phím bấm lần lượt, đồng thời hỗ trợ phát hiện phím cần bấm và tự thêm vào danh sách phím cần bấm.



    * Nhấn nhiều phím: cho phép bạn nhập chuỗi là các phím cần nhấn.



    <figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FRdv8O1DXrYiuWk6es0we%252Fimage.png%3Falt%3Dmedia%26token%3D65dc28e8-dca0-4222-9ac2-a613b12b1d6b&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=aadbcd9e&#x26;sv=2" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F9xcMY9uHR18gD2SS50Sh%252Fimage.png%3Falt%3Dmedia%26token%3D515b51fa-a339-47a2-aa1b-f4c78ba3591b&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=ea176518&#x26;sv=2" alt=""><figcaption></figcaption></figure>

##

{% embed url="https://youtu.be/hZvI6FNOIDI" %}
