---
description: Hỗ trợ người dùng thao tác với các tính năng của GemLogin thông qua API.
---

# API

Để truy cập vào tài liệu trên tool, bạn có thể bấm vào nút API để hiển thị các request có thể thực hiện khi Gemlogin đang được mở.

**Servers**: Mặc định là `http://localhost:1010` – Đây là địa chỉ local mà API đang hoạt động.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

GemLogin hỗ trợ các request sau:

### versions <a href="#versions" id="versions"></a>

#### Lấy danh sách browser được cài <a href="#lay-danh-sach-browser-duoc-cai" id="lay-danh-sach-browser-duoc-cai"></a>

<pre class="language-json"><code class="lang-json"><strong>curl -X 'GET' \
</strong>  'http://localhost:1010/api/browser_versions' \
  -H 'accept: application/json'
</code></pre>

Request này sẽ trả về kết quả dưới dạng json như sau, dưới dạng json:

```json
{
  "success": true,
  "message": "OK",
  "data": [
    {
      "id": 1,
      "version": "128"
    }
  ]
}
```

### groups <a href="#groups" id="groups"></a>

#### Lấy danh sách groups <a href="#lay-danh-sach-groups" id="lay-danh-sach-groups"></a>

```json
curl -X 'GET' \
  'http://localhost:1010/api/groups' \
  -H 'accept: application/json'
```

Request này trả về kết quả có danh sách group như sau:

```json
{
  "success": true,
  "message": "OK",
  "data": [
    {
      "id": 1,
      "name": "Group1",
      "created_at": "2025-04-07 09:22:38.788 +00:00",
      "updated_at": "2025-04-07 09:22:38.788 +00:00",
      "sort": 1,
      "created_by": -1
    },
    {
      "id": 2,
      "name": "Group2",
      "created_at": "2025-04-07 09:22:45.503 +00:00",
      "updated_at": "2025-04-07 09:22:45.503 +00:00",
      "sort": 1,
      "created_by": -1
    }
  ]
}
```

### profiles <a href="#profiles" id="profiles"></a>

#### Lấy thông tin profile có id được chỉ định <a href="#lay-thong-tin-profile-co-id-duoc-chi-dinh" id="lay-thong-tin-profile-co-id-duoc-chi-dinh"></a>

Copy

```json
curl -X 'GET' \
  'http://localhost:1010/api/profiles/delete/{profileId}' \
  -H 'accept: application/json'
```

Request này yêu cầu chỉ định profile id cần xóa, sẽ trả về kết quả như sau nếu xóa thành công:

```json
{
  "success": true,
  "message": "Xóa thành công",
  "data": null
}
```

#### Mở profile được chỉ định <a href="#mo-profile-duoc-chi-dinh" id="mo-profile-duoc-chi-dinh"></a>

```json
curl -X 'GET' \
  'http://localhost:1010/api/profiles/start/{profileId}?addination_args={args}&win_pos={browserPosition}&win_size={browserSize}&win_scale={browserScale}' \
  -H 'accept: application/json'
```

Request này sẽ mở profile được chỉ định. Các tham số yêu cầu trong request như sau:

| Name             |  Description                                                      |
| ---------------- | ----------------------------------------------------------------- |
| id               | ID của profile cần start                                          |
| addination\_args | Tham số dùng để khởi động, tham số cần tách nhau bởi khoảng trống |
| win\_pos         | Vị trí của browser ở định dạng x,y                                |
| win\_size        | Kích thước của cửa sổ theo định dạng chiều rộng, chiều cao        |
| win\_scale       | Tỉ lệ scale của cửa sổ trình duyệt                                |

Request trả về kết quả như sau:

```json
{
  "success": true,
  "message": "OK",
  "data": {
    "success": true,
    "profile_id": 23,
    "browser_location": "C:\\Users\\dell\\.gemlogin\\browser\\133\\Chrome-bin\\chrome.exe",
    "remote_debugging_address": "127.0.0.1:56170",
    "driver_path": "C:\\Users\\dell\\.gemlogin\\browser\\133\\Chrome-bin\\gemlogindriver.exe"
  }
}
```

#### Đóng profile được chỉ định <a href="#dong-profile-duoc-chi-dinh" id="dong-profile-duoc-chi-dinh"></a>

```json
curl -X 'GET' \
  'http://localhost:1010/api/profiles/close/1' \
  -H 'accept: application/json'
```

Request này sẽ thực hiện việc đóng cửa sổ trình duyệt có profile id được chỉ định đang được mở. Request cần truyền vào id của profile cần được đóng. Kết quả trả về sẽ như sau:

```json
{
  "message": "Close profile success",
  "success": true
}
```

#### Cập nhật thông tin profile chỉ định <a href="#cap-nhat-thong-tin-profile-chi-dinh" id="cap-nhat-thong-tin-profile-chi-dinh"></a>

```json
curl -X 'POST' \
  'http://localhost:1010/api/profiles/update/23' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profile_name": "Demo23",
  "group_id": 1,
  "raw_proxy": "192.168.0.5:5050",
  "startup_url": "https://www.youtube.com",
  "note": "This is a sample note",
  "user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/127.0.0.0 Safari/537.36",
  "browser_version": "133",
  "web_rtc": "noise",
  "language": "vi,en",
  "time_zone": "Asia/Bangkok",
  "country": "Vietnam",
  "lat": 30.425078442292502,
  "long": 115.69026310963571,
  "os": {
    "type": "Windows",
    "version": "win10"
  }
}'
```

Request này thực hiện việc cập nhật thông tin của profile được chỉ định.

Request này yêu cầu chỉ định profile id cần được update thông tin:

| Name        | Description                 |
| ----------- | --------------------------- |
| profile\_id | ID của profile được update. |

Đồng thời, thông tin profile được update có thể được chỉ định dưới dạng json như sau:

```json
{
  "profile_name": "Demo23",
  "group_id": 1,
  "raw_proxy": "192.168.0.5:5050",
  "startup_url": "https://www.youtube.com",
  "note": "This is a sample note",
  "user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/127.0.0.0 Safari/537.36",
  "browser_version": "133",
  "web_rtc": "noise",
  "language": "vi,en",
  "time_zone": "Asia/Bangkok",
  "country": "Vietnam",
  "lat": 30.425078442292502,
  "long": 115.69026310963571,
  "os": {
    "type": "Windows",
    "version": "win10"
  }
}
```

Khi thành công, request sẽ trả về response như sau:

```json
{
  "success": true,
  "message": "Update profile success"
}
```

#### Tạo profile mới <a href="#tao-profile-moi" id="tao-profile-moi"></a>

```json
curl -X 'POST' \
  'http://localhost:1010/api/profiles/create' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profile_name": "Test profile 1",
  "group_name": "All",
  "raw_proxy": "",
  "startup_urls": "",
  "is_masked_font": true,
  "is_noise_canvas": false,
  "is_noise_webgl": false,
  "is_noise_client_rect": false,
  "is_noise_audio_context": true,
  "is_random_screen": false,
  "is_masked_webgl_data": true,
  "is_masked_media_device": true,
  "is_random_os": false,
  "os": {
    "type": "Windows",
    "version": "win10"
  },
  "webrtc_mode": 2,
  "browser_version": "133",
  "user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/133.0.0.0 Safari/537.36",
  "language": "vi,en",
  "time_zone": "Asia/Bangkok",
  "country": "Vietnam",
  "lat": 29.425078442292502,
  "long": 115.69026310963571
}'
```

Request này sẽ tạo profile mới theo thông số được chỉ định trong body của request. Phần body chứa thông tin được cung cấp có thể bao gồm các thông tin sau:

```json
{
  "profile_name": "Test profile 1",
  "group_name": "All",
  "raw_proxy": "",
  "startup_urls": "",
  "is_masked_font": true,
  "is_noise_canvas": false,
  "is_noise_webgl": false,
  "is_noise_client_rect": false,
  "is_noise_audio_context": true,
  "is_random_screen": false,
  "is_masked_webgl_data": true,
  "is_masked_media_device": true,
  "is_random_os": false,
  "os": {
    "type": "Windows",
    "version": "win10"
  },
  "webrtc_mode": 2,
  "browser_version": "133",
  "user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/133.0.0.0 Safari/537.36",
  "language": "vi,en",
  "time_zone": "Asia/Bangkok",
  "country": "Vietnam",
  "lat": 29.425078442292502,
  "long": 115.69026310963571
}
```

Khi thành công, request sẽ trả về kết quả như sau:

```json
{
  "success": true,
  "data": {
    "id": 56,
    "name": "Test profile 1",
    "raw_proxy": "",
    "profile_path": "C:\\Users\\dell\\.gemlogin/profile\\profiles\\56",
    "browser_type": "Chrome",
    "browser_version": "133",
    "note": null,
    "group_id": null,
    "created_at": "2025-04-07T11:07:59.575Z"
  },
  "message": "OK"
}
```

#### Lấy thông tin profile <a href="#lay-thong-tin-profile" id="lay-thong-tin-profile"></a>

```json
curl -X 'GET' \
  'http://localhost:1010/api/profile/{profileId}' \
  -H 'accept: application/json'
```

Request này sẽ trả về thông tin của profile có id chỉ định. Kết quả trả về sẽ ở dạng json như sau:

```json
{
  "success": true,
  "message": "OK",
  "data": {
    "id": "23",
    "name": "Demo23",
    "raw_proxy": "http://192.168.0.5:5050",
    "browser_type": "chromium",
    "browser_version": 133,
    "group_id": "1",
    "profile_path": "C:\\Users\\dell\\.gemlogin/profile\\profiles\\23",
    "note": "",
    "created_at": "2025-04-07 10:46:05.922 +00:00"
  }
}
```

#### Lấy danh sách profile <a href="#lay-danh-sach-profile" id="lay-danh-sach-profile"></a>

```json
curl -X 'GET' \
  'http://localhost:1010/api/profiles?group_id=1&page=1&per_page=50&sort=0' \
  -H 'accept: application/json'
```

Request này sẽ lấy danh sách profile phù hợp với tham số được truyền vào. Các tham số được liệt kê như sau:

| Name      |  Description                                                          |
| --------- | --------------------------------------------------------------------- |
| group\_id | Group id chứa profile                                                 |
| page      | Số phân trang                                                         |
| per\_page | Số lượng profile được hiển thị trên mỗi trang                         |
| sort      | Kiểu sắp xếp được chỉ định (0 = latest, 1 = oldest, 2 = A-Z, 3 = Z-A) |

Kết quả trả về sẽ như sau:

```json
{
  "success": true,
  "message": "success",
  "data": [
    {
      "id": 24,
      "name": "1",
      "raw_proxy": "http://146.19.196.101:40604",
      "browser_type": "chromium",
      "browser_version": 132,
      "group_id": "1",
      "profile_path": "C:\\Users\\dell\\.gemlogin/profile\\profiles\\24",
      "note": null,
      "created_at": "2025-04-07 09:22:54.956 +00:00"
    },
    {
      "id": 23,
      "name": "Demo23",
      "raw_proxy": "http://192.168.0.5:5050",
      "browser_type": "chromium",
      "browser_version": 133,
      "group_id": "1",
      "profile_path": "C:\\Users\\dell\\.gemlogin/profile\\profiles\\23",
      "note": "",
      "created_at": "2025-04-07 10:46:05.922 +00:00"
    }
  ]
}
```

#### Thay đổi fingerprint của profile <a href="#thay-doi-fingerprint-cua-profile" id="thay-doi-fingerprint-cua-profile"></a>

```json
curl -X 'GET' \
  'http://localhost:1010/api/profiles/changeFingerprint?profileIds=28%2C29' \
  -H 'accept: application/json'
```

Request này thực hiện việc cập nhật fingerprint của profile có id được chỉ định.

NameDescription

profileIds

Danh sách profile id (chuỗi, tách bởi dấu ",")

Khi request thành công, kết quả trả về sẽ như sau:

```json
{
  "success": true,
  "message": "Change fingerprint successfully"
}
```

### scripts <a href="#scripts" id="scripts"></a>

#### Lấy danh sách script <a href="#lay-danh-sach-script" id="lay-danh-sach-script"></a>

```json
curl -X 'GET' \
  'http://localhost:1010/api/scripts' \
  -H 'accept: application/json'
```

Request này sẽ trả về danh sách scripts đang có trong tool. Kết quả trả về sẽ như sau:

```json
{
  "success": true,
  "message": "OK",
  "data": [
    {
      "id": "tIYyrsUWpgNyj2HurAu65",
      "name": "(Youtube) Watch video",
      "parameters": [
        {
          "name": "youtubeLink",
          "label": "label",
          "type": "string",
          "description": "",
          "defaultValue": "",
          "required": false
        }
      ]
    },
    {
      "id": "hRGThZTYLFs_mgbZjA-2W",
      "name": "(Google) Reg account (dailyOtp)",
      "parameters": [
        {
          "name": "lanOption",
          "label": "Tùy chọn ngôn ngữ cho thông tin của tài khoản mới",
          "type": "string",
          "description": "vi|en",
          "defaultValue": "en",
          "required": false
        },
        {
          "name": "dailyOtpToken",
          "label": "DailyOtpToken",
          "type": "string",
          "description": "",
          "defaultValue": "f3fd86cb7e8554542043f7a6e8b1735c0hoKZUZrEvkfbkWE9D0A",
          "required": false
        },
        {
          "name": "gemmmoToken",
          "label": "Gemmmo Token",
          "type": "string",
          "description": "",
          "defaultValue": "sckmsz9lbjcgtvlahtv87g6bcj7v8czot4vhmrt2vjx5ocnnaxaccirr12jbvxkry9keoo1740306129",
          "required": false
        },
        {
          "name": "resultTxtPath",
          "label": "Đường dẫn tới file txt chứa thông tin tài khoản sau reg",
          "type": "string",
          "description": "",
          "defaultValue": "D:\\Reg Gmail\\rg reg gmail acc.txt",
          "required": false
        }
      ]
    },
    {
      "id": "iXLjTLZdD_ghgWlj6U7NP",
      "name": "(hotmail) Reg account",
      "parameters": [
        {
          "name": "newAccountTxtPath",
          "label": "Đường dẫn tới file txt dùng để ghi thông tin account mới tạo",
          "type": "string",
          "description": "",
          "defaultValue": "E:\\gemlogin-scripts\\test-context\\MailX.txt",
          "required": true
        },
        {
          "name": "omoCaptchaApiKey",
          "label": "API Key của OmoCaptcha để giải captcha",
          "type": "string",
          "description": "",
          "defaultValue": "",
          "required": false
        }
      ]
    }
  ]
}
```

Thực hiện script chỉ định

```json
curl -X 'POST' \
  'http://localhost:1010/api/scripts/execute/tIYyrsUWpgNyj2HurAu65' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileId": 23,
  "closeBrowser": true,
  "parameters": {
    "youtubeLink": "https://www.youtube.com/watch?v=6R3isnB85ys"
  }
}'
```

Request này sẽ thực hiện script có id được chỉ định. Thông tin thực hiện script có thể được chỉ định trong body như sau:

```json
{
  "profileId": 23,
  "closeBrowser": true,
  "parameters": {
    "youtubeLink": "https://www.youtube.com/watch?v=6R3isnB85ys"
  }
}
```

Khi thành công, kết quả trả về sẽ như sau:

```json
{
    "success": true,
    "id": "tIYyrsUWpgNyj2HurAu65"
}
```

#### Lấy trạng thái thực hiện của script <a href="#lay-trang-thai-thuc-hien-cua-script" id="lay-trang-thai-thuc-hien-cua-script"></a>

```json
curl -X 'POST' \
  'http://localhost:1010/api/scripts/check-status/tIYyrsUWpgNyj2HurAu65' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileId": 23
}'
```

Request này sẽ trả về trạng thái của script có id được chỉ định với profile có id được chỉ định. Script id được chỉ định trong tham số, còn profile id cần được chỉ định trong body của request:

| Name | Description                |
| ---- | -------------------------- |
| id   | ID của script cần kiểm tra |

```json
{
  "profileId": 23
}
```

Kết quả trả về sẽ như sau nếu success:

```json5
{
  "is_running": true,
  "message": "Script is running"
}
```

#### Dừng chạy script đang được thực hiện <a href="#dung-chay-script-dang-duoc-thuc-hien" id="dung-chay-script-dang-duoc-thuc-hien"></a>

```json
curl -X 'POST' \
  'http://localhost:1010/api/scripts/kill-execute/tIYyrsUWpgNyj2HurAu65' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "profileId": 23,
  "closeBrowser": true
}'
```

Request này sẽ thực hiện dừng script đang được thực hiện trên profile có id được chỉ định.

| Name | Description                       |
| ---- | --------------------------------- |
| id   | ID của script đang được thực hiện |

```json
{
  "profileId": 23,
  "closeBrowser": true
}
```

Request sẽ trả về kết quả như sau:

```json5
{
  "success": true,
  "message": "Kill excute success"
}
```
