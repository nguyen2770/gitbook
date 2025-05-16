---
description: >-
  Đợi tất cả các node kết nối với việc thực thi node này kết thúc trước khi tiếp
  tục node tiếp theo.
---

# Wait Connections

Sử dụng node này khi bạn có các node phân nhánh trong quy trình.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FqyGd0MC9saDNMdFfEk7J%252Fimage.png%3Falt%3Dmedia%26token%3D0b952fe7-c80f-4acb-b984-60aa6f0594cd&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=d075bf75&#x26;sv=2" alt=""><figcaption></figcaption></figure>

\- **Thời Gian Chờ (ms)** Đặt khoảng thời gian node chờ để tất cả luồng hoàn tất thực thi, mặc định là 10000 mili giây. Khi đạt đến thời gian chờ, quy trình sẽ tiếp tục thực thi node tiếp theo.

#### Chỉ tiếp tục một luồng cụ thể[​](https://docs.omnilog.in/blocks/wait-connections.html#chi-tiep-tuc-mot-luong-cu-the)​ <a href="#chi-tiep-tuc-mot-luong-cu-the" id="chi-tiep-tuc-mot-luong-cu-the"></a>

Liệu chỉ có tiếp tục một dòng chảy cụ thể hay không ? Khi bạn có một node được phân nhánh như trong hình trên, Automation sẽ tạo một "Luồng" mới cho mỗi nhánh mới có nhiệm vụ thực thi các node trên nhánh đó.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F9P1XFolcQxKyyQkwfUWk%252Fimage.png%3Falt%3Dmedia%26token%3D130abaaa-49a4-4854-ac17-fc9797184714&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=70f65e3&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Và khi bạn hợp nhất nhánh mà không bật tùy chọn này, mọi luồng sẽ thực thi cùng một node. Và các node sẽ thực thi nhiều lần.

Để ngăn chặn điều này, hãy chọn lựa chọn `Chỉ tiếp tục một quy trình cụ thể` và chọn 1 trong số các luồng hiện tại.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252F6NdyO9rzqXu4saeySWLP%252Fimage.png%3Falt%3Dmedia%26token%3D776f31de-e796-4ab2-9c1f-7087b9e4f09d&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=b8870a9a&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Khi chạy thì luồng Nhấp chuột được chọn sẽ chạy đến node tiếp theo sau Wait connections -> Open Url

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FPhJtkVghup1Vu0TsM8DR%252Fimage.png%3Falt%3Dmedia%26token%3D282ee70c-9bbf-4923-b5be-016ba15d42ba&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=9d014075&#x26;sv=2" alt=""><figcaption></figcaption></figure>
