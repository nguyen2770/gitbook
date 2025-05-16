---
description: Thực hiện command prompt (cmd) và trả về kết quả trên cmd
---

# Cmd

CodeKhi node được thực thi, nó sẽ chạy lệnh CMD đã được bạn chỉ định. Kết quả của lệnh sẽ được trả về và có thể gán vào biến khi chọn assign to variable.

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FveZOU3iIOHwFKe3iszfp%252Fimage.png%3Falt%3Dmedia%26token%3Dfae06409-2dd6-4144-b489-d1da5929a636&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=41637159&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Block CMD cung cấp các thuộc tính sau:

* Command: Câu lệnh cần thực hiện
* Assign to variable: Gán kết quả trả về trong console vào biến. Lựa chọn này có 2 input: một để chỉ định tên biến lưu giá trị được gán, input còn lại dành cho biểu thức regex được dùng để chỉ lấy những phần tìm thấy bởi biểu thức regex.

_Note: Đảm bảo rằng lệnh CMD được chỉ định là chính xác và phù hợp với hệ thống của bạn để tránh lỗi trong quá trình thực thi._

#### Ví dụ <a href="#vi-du" id="vi-du"></a>

Một trường hợp thường thấy là cần lấy thông tin về đường dẫn file trong một thư mục chỉ định, ta có thể sử dụng code powershell như sau:

Copy

```
$folderPath = 'C:\Users\dell\Pictures\Saved Pictures';
if (![string]::IsNullOrEmpty($folderPath) -and (Test-Path -Path $folderPath -PathType Container))
{
    $imageFiles = Get-ChildItem -Path $folderPath -File | Where-Object { $_.Extension -match '\.(jpg|jpeg|png|gif|bmp|tiff|jfif)$' };
    if ($imageFiles.Count -gt 0)
    {
        $imagePaths = $imageFiles.FullName -join '|'
    };
    Write-Host $imagePaths
}
```

Đoạn code powershell này sẽ đọc đường dẫn được chỉ định tại biến folderPath, tìm các file thuộc dạng ảnh bằng cách check extension của chúng. Sau khi xác định được các file ảnh trong folder, đoạn code này sẽ lấy đường dẫn đầy đủ của chúng và ghi ra console đường dẫn file lần lượt cách nhau bởi dấu “|”. Kết quả có thể được thấy như ở hình sau:

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FZzNH4HxpBDwqkSeQ2POm%252Fimage.png%3Falt%3Dmedia%26token%3D5b83de23-040e-43df-90f1-3ded07383987&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=6faa63a1&#x26;sv=2" alt=""><figcaption></figcaption></figure>

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FMMkEweSYbbTPjnbjJfDg%252Fimage.png%3Falt%3Dmedia%26token%3Df3a3793d-f86f-49c7-a023-86c7aa154118&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=3bbc8b66&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Dựa vào đoạn code powershell này, ta có thể lấy được đường dẫn của các file ảnh với kết quả như hình.

Để thiết lập block cmd lấy được kết quả như này, ta có thể dùng block cmd như sau:

* Đầu tiên, chuyển đổi code powershell để toàn bộ code được viết trên 1 dòng (do cmd chỉ có thể thực hiện lệnh trên 1 dòng). Kết quả đoạn code powershell như sau:\`

Copy

```
$folderPath = 'C:\Users\dell\Pictures\Saved Pictures'; if (![string]::IsNullOrEmpty($folderPath) -and (Test-Path -Path $folderPath -PathType Container)) { $imageFiles = Get-ChildItem -Path $folderPath -File | Where-Object { $_.Extension -match '\.(jpg|jpeg|png|gif|bmp|tiff|jfif)$' }; if ($imageFiles.Count -gt 0) { $imagePaths = $imageFiles.FullName -join '|' }; Write-Host $imagePaths } 
```

* Tiếp theo ở block CMD, để ngắn gọn, ta có thể khai báo một biến mới là tên là psCode (tên có thể tùy ý tùy chỉnh) với giá trị là lệnh powershell sau khi đã loại bỏ các ký tự xuống dòng như sau:

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FvngA39eY4lzSwPOeTu6r%252Fimage.png%3Falt%3Dmedia%26token%3D7c984141-97c2-4f48-ae8a-1f8e1b73f1ce&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8b492cb6&#x26;sv=2" alt=""><figcaption></figcaption></figure>

• Tiếp đó, ta có thể điền vào block cmd với nội dung câu lệnh như sau: `powershell -ExecutionPolicy Bypass "{{variables.psCode}}"`. Câu lệnh này sẽ chạy code powershell và gán kết quả ghi ở console vào biến avatarPathvatarPaths, kết hợp với việc điền biểu thức regex để tách các đường dẫn thành mảng, ta sẽ có kết quả như sau:

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FNE6bXqqUvehxBe5BcyPh%252Fimage.png%3Falt%3Dmedia%26token%3Dc5a9653c-a706-4687-b243-44aad5c36fdf&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=e6e4f3a9&#x26;sv=2" alt=""><figcaption></figcaption></figure>

<figure><img src="https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FNdaH5wbibuQoJXZIBKNz%252Fimage.png%3Falt%3Dmedia%26token%3D9690c74d-064f-470d-85f4-b97de759fbe1&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=3fe77347&#x26;sv=2" alt=""><figcaption></figcaption></figure>
