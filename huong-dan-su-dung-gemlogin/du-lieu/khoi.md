# Khối

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FAl8js6ZVRXGvDU4X23so%252Fimage.png%3Falt%3Dmedia%26token%3Df71e8672-76d4-4933-8dee-56ef8f51a609\&width=768\&dpr=4\&quality=100\&sign=b8f383f5\&sv=2)

### Automation của Gemlogin bao gồm các khối: <a href="#automation-cua-gemlogin-bao-gom-cac-khoi" id="automation-cua-gemlogin-bao-gom-cac-khoi"></a>

* **General**: Thực hiện một hành động chung trong quy trình, như tạm dừng kịch bản hay xuất dữ liệu từ kịch bản ra file.
* **Browser**: Thực hiện các thao tác điều khiển trình duyệt như mở liên kết, đóng tab, lấy url tab...
* **Web interaction**: Để tương tác với tab đang hoạt động của quy trình, trước khi sử dụng các node trong danh mục này, bạn cần sử dụng Mở liên kết rồi thực hiện các thao tác như click chuột, cuộn chuột trên trang vừa được mở.
* **Control flow**: Thêm logic vào quy trình.
* **Online services**: Thao tác với các dịch vụ trực tuyến như Google Sheet, Email...
* **Data**: Sửa đổi hoặc thao tác các biến hoặc bảng trong quy trình.

#### Cài đặt <a href="#cai-dat" id="cai-dat"></a>

CommentCác node đi kèm với một menu và các cài đặt có thể được cấu hình.

#### Menu <a href="#menu" id="menu"></a>

CommentĐể tìm menu node, hãy di chuột qua một node trong khung soạn thảo và nó sẽ xuất hiện ở đầu node.

* **Xoá**: xoá node
* **Cài đặt node**: cài đặt cho phép bạn cấu hình thực thi node, xử lý lỗi và giao diện.
  * **Chung**
    * **Thời gian thực thi tối đa**: thời gian tối đa để thực thi một node
  * **Xử lí lỗi**
    * **Kích hoạt**: Kích hoạt các lựa chọn để xử lí khi có lỗi xảy ra
    * **Thử lại thành công**: thực hiện lại node với số lần thử lại cũng như khoảng thời gian thử giữa các lần thử lại, ngoài ra người dùng có thể lựa chọn các lựa chọn (ném lỗi, tiếp tục thực thi, thực thi dự phòng)
    * **Chèn dữ liệu**: chèn dữ liệu từ bảng hoặc biến
  * **Dòng**
    * **Chọn dòng**: chọn một kết nối với node khác để tuỳ chỉnh
    * **Nhãn dòng**: thêm nhãn dòng cho kết nối
    * **Hoạt hình**: làm kết nối trở nên sinh động
    * **Màu đường kẻ**: thay đổi màu sắc của kết nối(mặc định là đen)
* **Di chuyển node**: di chuyển node sang chỗ khác
* **Bật/Tắt node**: bật/tắt chạy node
* **Chạy node**: Chạy tiếp kịch bản từ node này.
* **Edit**: truy cập vào phần cài đặt node hoặc bạn có thể click chuột 2 lần sửa node này.

Bạn cũng có thể nhấn chuột phải vào mỗi node để khám phá các hành động khác

#### Chọn các node sau đó di chuyển vùng đó đến một chỗ bất kỳ <a href="#chon-cac-node-sau-do-di-chuyen-vung-do-den-mot-cho-bat-ky" id="chon-cac-node-sau-do-di-chuyen-vung-do-den-mot-cho-bat-ky"></a>

Để chọn nhiều node, bạn có thể giữ phím `ctrl` => nhấn vào các node muốn chọn hoặc giữ phím `shift` => tạo thành một vùng bao quanh các node, sau đó di chuyển vùng đó đến một chỗ bất kỳ.

#### Kết nối giữa các node <a href="#ket-noi-giua-cac-node" id="ket-noi-giua-cac-node"></a>

Có một số cách để kết nối một node với một node khác:

* **Thủ công**: kéo đầu ra node vào đầu vào của node.
* **Thả một node vào đầu ra node**: thả node vào đầu ra của node.
* **Bấm vào node đầu ra và đầu vào**: click vào đầu ra của một node sau đó click vào đầu vào của một node để nối hai không đó với nhau
