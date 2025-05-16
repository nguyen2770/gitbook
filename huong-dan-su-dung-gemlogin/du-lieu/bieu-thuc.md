# Biểu thức

### Miêu tả chung <a href="#mieu-ta-chung" id="mieu-ta-chung"></a>

Mặc định, mọi giá trị bạn nhập vào, chẳng hạn như XPath/CSS Selector trong block `input` hoặc `click`, hay giá trị cần nhập trong block `presskey`/`input`, đều được coi là chuỗi tĩnh – tức là giá trị cố định, không thay đổi.

Tuy nhiên, **biểu thức** là một công cụ giúp chuyển đổi giá trị tĩnh thành giá trị động, cho phép linh hoạt hơn trong quá trình thao tác. Biểu thức được xác định bằng cặp dấu ngoặc nhọn `{{ }}`. Khi gặp cặp dấu này trong giá trị nhập vào, **GemLogin** sẽ hiểu đó là một biểu thức, tính toán giá trị của nó và thay thế vào chuỗi ban đầu.

Điều này giúp bạn có thể sử dụng các biến, phép toán hoặc logic động ngay trong các giá trị nhập vào, thay vì chỉ sử dụng dữ liệu cố định.

### Cú pháp <a href="#cu-phap" id="cu-phap"></a>

Có thể chia biểu thức thành 2 thành phần chính: toán hạng và hàm

#### **Toán hạng** <a href="#toan-hang" id="toan-hang"></a>

Trong GemLogin, toán hạng là những thành phần cơ bản để tạo thành biểu thức và trả về một giá trị. Giá trị của toán hạng được lưu trữ trong các keyword sau:&#x20;

| Tên          | Miêu tả                                         | Truy cập đối tượng con    |
| ------------ | ----------------------------------------------- | ------------------------- |
| table        | Lấy dữ liệu từ Bảng                             | table.columnName          |
| variables    | Lấy dữ liệu từ Biến (khai báo trong script)     | variables.variableName    |
| loopData     | Lấy dữ liệu trong vòng lặp của node Lặp dữ liệu | loopData.loopId           |
| globalData   | Lấy dữ liệu chung của kịch bản (hằng)           | globalData.dataname       |
| googleSheets | Lấy dữ liệu từ Google Sheets hoặc từ Excel      | googleSheets.referenceKey |

_\*Note: GemLogin chia thành các nguồn dữ liệu khác nhau bởi dữ liệu của chúng được đặt/set theo cách khác nhau với mục đích khác nhau. Tham khảo tài liệu chi tiết về block liên quan để hiểu dữ liệu mà các nguồn cung cấp._

Để lấy dữ liệu từ nguồn trong GemLogin, bạn có thể viết như sau:

`{{variables.myGreeting}}` trong đó biểu thức này sẽ lấy dữ liệu từ nguồn là variables và lấy dữ liệu từ biến tên myGreeting

`{{variables.httpRequestResponse.isSuccess}}` trong đó biểu thức này sẽ lấy dữ liệu từ nguồn là variables, lấy dữ liệu của biến tên httpRequestResponse. Biểu thức này sẽ được coi là hợp lệ nếu biến httpRequestResponse có giá trị là json và có key là isSuccess, GemLogin sẽ tự động lấy giá trị từ key isSuccess và trả về giá trị từ key isSuccess này

#### Hàm <a href="#ham" id="ham"></a>

GemLogin cho phép sử dụng hàm trong một biểu thức. Hàm cho phép xử lý và biến đổi dữ liệu linh hoạt, tăng tính tự dộng trong workflow; cái sẽ giúp giảm thiểu lỗi và tăng tính bảo trì.

{% hint style="info" %}
_\*Note: Hàm trong gemlogin được đánh dấu bởi ký tự `$` trước tên hàm._
{% endhint %}

GemLogin hỗ trợ các hàm theo danh sách sau:

`$date() $date(format) $date(date, format)`

_date là hàm được dùng để trả về thời gian theo định dạng được chỉ định. Hàm sẽ trả về kết quả như sau:_

* $date(): date mặc định lấy là thời gian hiện tại, format mặc định là 'DD-MM-YYYY'.
* $date(format): tham số được truyền được coi như là format, giá trị thời gian vẫn là thời gian hiện tại.
* $date(date, format): tham số đầu tiên là thời gian cần định dạng theo format, tham số thứ hai là định dạng của thời gian.

**Tham số:**

* date: thời gian cần được định dạng.
* format: định dạng của thời gian.

`$randint(min, max)` randint là hàm được dùng để tạo ngẫu nhiên một số nguyên nằm trong khoảng min và max được chỉ định.

T**ham số:**

* min: giá trị tối thiểu trong khoảng.
* max: giá trị tối đa trong khoảng.



`$getLength(data)` getLength là hàm được dùng để tìm độ dài của data được truyền vào. Nếu data là một mảng, hàm sẽ trả về số lượng phần tử thuộc mảng. Nếu data là một chuỗi, hàm sẽ trả về độ dài của chuỗi được truyền vào. Nếu data là một object, trả về object này.

Tham số:

* data: dữ liệu được truyền



`$slice(string, start, end)`

slice là hàm được dùng để thực hiện việc cắt từ chuỗi lớn chuỗi con với điểm bắt đầu và điểm kết thúc được chỉ định.

Tham số:

* string: chuỗi cần được tách (chuỗi lớn).
* start: vị trí bắt đầu của chuỗi con cần tách trong chuỗi lớn.
* end: vị trí kết thúc của chuỗi còn cần tách trong chuỗi lớn.



`$increment(a, b)`

increment là hàm được dùng để thực hiện phép cộng với 2 giá trị được truyền vào.

Tham số:

* a, b: 2 toán hạng của phép cộng



`$subtract(a, b)`

substract là hàm được dùng để thực hiện phép trừ với 2 giá trị được truyền vào.

Tham số:

* a, b: 2 toán hạng của phép trừ, trong đó a sẽ trừ cho b. hàm sẽ trả về kết quả của phép trừ a cho b

`$multiply(a, b)`

multiple là hàm được dùng để thực hiện phép nhân với 2 giá trị được truyền vào.

Tham số:

* a, b: 2 toán hạng của phép nhân

`$devide(a, b)`

devide là hàm được dùng để thực hiện phép chia với 2 giá trị được truyền vào.

Tham số:

* a, b: 2 toán hạng, trong đó a sẽ chia cho b -> hàm sẽ trả về kết quả của phép chia a cho b

`$modulo(a, b)`

modulo là hàm được dùng để thực hiện phép chia dư với 2 giá trị được truyền vào.

Tham số:

* a, b: 2 toán hạng của phép chia dư, trong đó a sẽ chia dư cho b. hàm sẽ trả về kết quả của phép chia dư a cho b

`$randData(format)​`

randData(format) là hàm được dùng để tạo ngẫu nhiên một chuỗi dưa theo định đạng được yêu cầu.

Tham số:

* format: định dạng của chuỗi kết quả được sinh. Định dạng của chuỗi được quy định như sau:
  * l: Chữ cái thường (a-z)
  * u: Chữ cái hoa (A-Z)
  * d: Chữ số (0-9)
  * s: Ký tự đặc biệt (!@#$%^&\*()-\_+={}\[]|;:'"<>,./?")
  * f: Một chữ cái thường và một chữ cái hoa
  * n: Một chữ cái thường và một chữ số
  * m: Một chữ cái hoa và một chữ số
  * i: Một chữ cái thường, một chữ cái hoa và một chữ số
  * a: Một ký tự bất kỳ từ chữ cái thường, chữ cái hoa, chữ số và ký tự đặc biệt

`$randData(arr)`

randData(arr) là hàm được dùng để chọn ngẫu nhiên một phần tử thuộc mảng được truyền vào.

Tham số:

* arr: mảng được truyền.

`$filter(json, jsonPathExpression)`

filter là hàm được dùng để tính toán biểu thức jsonPath đối với dữ liệu json được truyền vào.

tham số:

* json: đối tượng json
* jsonPathExpression: biểu thức json path sử dụng để tính toán.

`$replace(bigString, beingReplacedSubString, replacementString)`

replace là hàm được dùng để thay thế chuỗi con cần thay thế bằng cách tìm trong chuỗi lớn (bigString) chuỗi con cần được thay thế (beingReplacedSubString). Khi tìm thấy, chuỗi con này sẽ được thay bởi chuỗi thay thế (replacementString). Hàm này sẽ chỉ thay thế chuỗi đầu tiên tì thấy.

Tham số:

* bigString: chuỗi lớn. Hoạt động thay thế diễn ra trong chuỗi này.
* beingReplacedSubString: chuỗi bị thay thế.
* replacementString: chuỗi dùng để thay thế.

`$replaceAll(bigString, beingReplacedSubString, replacementString)`

replaceAll là hàm được dùng để thay thế chuỗi con cần thay thế bằng cách tìm trong chuỗi lớn (bigString) chuỗi con cần được thay thế (beingReplacedSubString). Khi tìm thấy, chuỗi con này sẽ được thay bởi chuỗi thay thế (replacementString). Hàm này sẽ chỉ thay thế tất cả chuỗi tìm thấy.

Tham số:

1. bigString: chuỗi lớn. Hoạt động thay thế diễn ra trong chuỗi này.
2. beingReplacedSubString: chuỗi bị thay thế.
3. replacementString: chuỗi dùng để thay thế.

`$toLowerCase(string)`

toLowerCase là hàm được dùng để trả về dạng chữ in thường của chuỗi được truyền vào.

Tham số:

* string: chuỗi cần được chuyển thành in thường.

`$toUpperCase(string)`

toUpperCase là hàm được dùng để trả về dạng chữ in hoa của chuỗi được truyền vào.

Tham số:

* string: chuỗi cần được chuyển thành in hoa.

`$stringify(value)`

stringìy là hàm được dùng để ép chuỗi trả về thành json.

tham số:

1. value: giá trị cần được chuyển đổi

#### _Biểu thức lồng_ <a href="#bieu-thuc-long" id="bieu-thuc-long"></a>

_\*Note: Để lấy dữ liệu từ một biểu thức bên trong một biểu thức, cặp biểu thức con trong biểu thức cha bằng cặp ngoặc vuông `[]` . GemLogin sẽ tự động tìm và chuyển đổi chúng thành giá trị tương ứng._

_Ví dụ:_

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FYz6SXIxmp5KTu65W2bWU%252Fimage.png%3Falt%3Dmedia%26token%3D707cedf9-8542-42fb-aed0-6fbf3e0e9da2\&width=768\&dpr=4\&quality=100\&sign=27f380fa\&sv=2)

_Giả sử như hình, sử dụng block insert data để khai báo biến array với 4 phần tử từ 1 tới 4 như hình, để tìm tổng số phần tử của mảng chứ 6 phần tử từ 1->6 và mảng là giá trị của biến array, ta có thể nhập biểu thức như sau:_

Copy

```
{{$increment( [$getLength([1,2,3,4,5,6])] ,[$getLength([variables.array])] ) }}
```

_Khi được thực hiện, biến test sẽ có giá trị cuối cùng như sau:_

![](https://manual-gemlogin-vn.gitbook.io/~gitbook/image?url=https%3A%2F%2F1320481151-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fx9Jdg3uhoV9mD7ywwyVw%252Fuploads%252FGGx5t7xVUrYiifwvw8nF%252Fimage.png%3Falt%3Dmedia%26token%3Dd68eb6a1-f000-4628-8b20-4dc71f0fb3db\&width=768\&dpr=4\&quality=100\&sign=fd7ad763\&sv=2)
