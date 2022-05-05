# TUẦN 1: Giới thiệu & HTML cơ bản

## Tổng quan về phát triển trang web (Bình)

### Nhà phát triển Frontend là gì?

Phát triển web front-end, còn được gọi là phát triển phía máy khách là hoạt động tạo HTML, CSS và JavaScript cho một trang web hoặc Ứng dụng web để người dùng có thể nhìn thấy và tương tác trực tiếp với chúng.

### UI / UX là gì?

Thiết kế UX đề cập đến thuật ngữ “thiết kế trải nghiệm người dùng”, trong khi UI là viết tắt của “thiết kế giao diện người dùng”. Cả hai yếu tố đều rất quan trọng đối với một sản phẩm và phối hợp chặt chẽ với nhau. Nhưng bất chấp mối quan hệ nghề nghiệp của họ, bản thân các vai trò lại khá khác nhau, đề cập đến các khía cạnh rất khác nhau của quá trình phát triển sản phẩm và kỷ luật thiết kế.

- Thiết kế trải nghiệm người dùng (UX) là gì?

  Thiết kế trải nghiệm người dùng là cách thiết kế sản phẩm lấy con người làm đầu. Don Norman, một nhà khoa học nhận thức và là đồng sáng lập của Công ty Tư vấn Thiết kế Nielsen Norman, được cho là đã đặt ra thuật ngữ “trải nghiệm người dùng” vào cuối những năm 1990. Đây là cách anh ấy mô tả nó:

  > “Trải nghiệm người dùng bao gồm tất cả các khía cạnh tương tác của người dùng cuối với công ty, dịch vụ và sản phẩm của công ty.” - Don Norman

- Thiết kế giao diện người dùng (UI) là gì?

  Trong khi trải nghiệm người dùng là một tập hợp các nhiệm vụ tập trung vào việc tối ưu hóa sản phẩm để sử dụng hiệu quả và thú vị, thì thiết kế giao diện người dùng là phần bổ sung của nó; giao diện, cách trình bày và tính tương tác của sản phẩm.

#### Tóm lại cách hoạt động của các trang web

Khi bạn nhập địa chỉ web vào trình duyệt của mình (ví dụ của chúng tôi, giống như đi bộ đến cửa hàng):

1. Trình duyệt truy cập máy chủ DNS và tìm địa chỉ thực của máy chủ mà trang web đang sử dụng (bạn tìm địa chỉ của cửa hàng).

2. Trình duyệt gửi một thông báo yêu cầu HTTP đến máy chủ, yêu cầu nó gửi một bản sao của trang web cho khách hàng (bạn đến cửa hàng và đặt hàng của bạn). Thông báo này và tất cả các dữ liệu khác được gửi giữa máy khách và máy chủ, được gửi qua kết nối internet của bạn bằng TCP / IP.

3. Nếu máy chủ chấp thuận yêu cầu của khách hàng, máy chủ sẽ gửi cho khách hàng một thông báo "200 OK", có nghĩa là "Tất nhiên bạn có thể xem trang web đó! Đây là", và sau đó bắt đầu gửi tệp của trang web đến trình duyệt như một loạt các phần nhỏ gọi là gói dữ liệu (cửa hàng giao hàng cho bạn và bạn mang hàng về nhà).

4. Trình duyệt tập hợp các phần nhỏ thành một trang web hoàn chỉnh và hiển thị nó cho bạn (hàng đã đến cửa nhà bạn - thứ sáng bóng mới, thật tuyệt!).

#### Giao tiếp giữa phụ trợ và giao diện người dùng

Giao diện người dùng và phần phụ trợ giao tiếp với nhau - thông qua các yêu cầu Http. Ví dụ: giao diện người dùng sẽ gửi dữ liệu đã nhập đến phần phụ trợ. Sau đó, chương trình phụ trợ có thể xác thực lại dữ liệu đó (vì mã giao diện người dùng có thể bị lừa) và cuối cùng lưu trữ nó trong một số cơ sở dữ liệu.

Điều kỳ diệu nằm trong tải trọng yêu cầu / phản hồi HTTP. Phần phụ trợ thường phản hồi với một số nội dung nhất định của phần thân HTTP:

- Câu trả lời được định dạng HTML
- các tệp tĩnh khác (CSS, JS, hình ảnh,…)
- Dữ liệu định dạng JSON
- Không có xác gì cả. Chỉ là một mã trạng thái và các trường tiêu đề.

Giao diện người dùng gửi:

- Các yêu cầu HTTP đơn giản không có nội dung
- Dữ liệu biểu mẫu
- Dữ liệu định dạng JSON

## Terminal (Quán)

## Kiểm soát phiên bản (Git) (Quan)

### Gitflow

Quy trình tổng thể của Gitflow là:

1. Một nhánh `develop` được tạo từ `main`
2. Một nhánh `release` được tạo từ `develop`
3. Các nhánh của `feature` được tạo từ `develop`
4. Khi một tính năng hoàn tất, nó được hợp nhất vào nhánh `develop`
5. Khi nhánh `release` được thực hiện xong, nó được hợp nhất thành `develop` và `main`
6. Nếu sự cố trong `main` được phát hiện, một nhánh `hotfix` được tạo từ `main`
7. Sau khi hoàn tất `hotfix`, nó sẽ được hợp nhất thành cả `develop` và `main`

## HTML5 (Tuấn)

### Cách cấu trúc HTML

Mỗi và mọi tài liệu HTML 5 sử dụng sự kết hợp duy nhất của các phần tử và nội dung để xác định một trang. Cấu trúc của tất cả các trang tài liệu thuộc tính đều giống nhau và chứa:

1. Một khai báo ở trên cùng, cho biết rằng đó là tài liệu HTML 5
2. Tiêu đề tài liệu
3. Một nội dung tài liệu

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset = "utf-8" />
    <title> Cấu trúc trang cơ bản </title>
  </head>
  <body>
    <!-- <! - Phần tử HTML -> -->
  </body>
</html>
```

`<!DOCTYPE>` thông báo cho các trình duyệt rằng nó thực sự là một tài liệu HTML 5. Mặc dù có các loại DOC Loại khác, nhưng đây là loại khai báo được sử dụng phổ biến nhất.

Khai báo DOCType được theo sau bởi thẻ mở và thẻ đóng `<html> </html>`. Các thẻ này chứa mọi thứ bên trong tài liệu, bao gồm Head và Body

Thẻ mở và đóng `<head> </head>`, hãy làm theo thẻ Html mở. Các thẻ này chứa thông tin về nội dung, tiêu đề của trang, định nghĩa, nhãn, v.v. Bạn chỉ có thể sử dụng các phần tử đánh dấu nhất định trong phần đầu HTML 5. Một số yếu tố này bao gồm phong cách, tiêu đề, cơ sở, liên kết, tập lệnh và meta. Trong HTML 5, các phần tử này được gọi chung là Phần tử đầu HTML.

Sau thẻ head đóng là thẻ mở và đóng body `<body> </body>`. Chúng chứa tất cả nội dung xuất hiện trên trình duyệt, cũng như các mã HTML 5 liên quan

### Nhập tập lệnh, kiểu vào trang web

- Nhập kịch bản

  Thẻ `<script> </script>` là những gì chúng tôi sử dụng để bao gồm JavaScript của mình.

  ```html
  <script type="text/javascript">
    alert('This alert box was called with the onload event');
  </script>
  ```

  Sử dụng thẻ script để bao gồm một tệp JavaScript bên ngoài.

  Để bao gồm một tệp JavaScript bên ngoài, chúng ta có thể sử dụng thẻ script với thuộc tính src. Bạn đã sử dụng thuộc tính src khi sử dụng hình ảnh. Giá trị cho thuộc tính src phải là đường dẫn đến tệp JavaScript của bạn.

  ```html
  <script type="text/javascript" src="path-to-javascript-file.js"></script>
  ```

  Thẻ script này nên được bao gồm giữa các thẻ `<head>` trong tài liệu HTML của bạn.

- Kiểu dáng nhập khẩu

    CSS có thể được đính kèm dưới dạng một tài liệu riêng biệt hoặc được nhúng vào chính tài liệu HTML. Có ba phương pháp bao gồm CSS trong tài liệu HTML:

  - Kiểu nội tuyến - Sử dụng thuộc tính style trong thẻ bắt đầu HTML.

  ```html
  <h1 style="color:red; font-size:30px;">This is a heading</h1>
  <p style="color:green; font-size:22px;">This is a paragraph.</p>
  <div div style="color:blue; font-size:14px;">This is some text content.</div>
  ```

  - Kiểu nhúng - Sử dụng phần tử `<style>` trong phần đầu của tài liệu

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>My HTML Document</title>
      <style>
        body {
          background-color: YellowGreen;
        }
        p {
          color: #fff;
        }
      </style>
    </head>
    <body>
      <h1>This is a heading</h1>
      <p>This is a paragraph of text.</p>
    </body>
  </html>
  ```

  - Các biểu định kiểu bên ngoài - Sử dụng phần tử `<link>`, trỏ đến tệp CSS bên ngoài.

    Một bảng kiểu bên ngoài là lý tưởng khi kiểu được áp dụng cho nhiều trang của trang web.
    Biểu định kiểu bên ngoài giữ tất cả các quy tắc kiểu trong một tài liệu riêng biệt mà bạn có thể liên kết từ bất kỳ tệp HTML nào trên trang web của mình. Bảng định kiểu bên ngoài là linh hoạt nhất vì với bảng định kiểu bên ngoài, bạn có thể thay đổi giao diện của toàn bộ trang web chỉ bằng cách thay đổi một tệp.

    Bạn có thể đính kèm các biểu định kiểu bên ngoài theo hai cách - liên kết và nhập.

    - Liên kết các trang tính kiểu bên ngoài

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>My HTML Document</title>
        <link rel="stylesheet" href="css/style.css">
    </head>
    <body>
        <h1>This is a heading</h1>
        <p>This is a paragraph of text.</p>
    </body>
    </html>
    ```

    - Nhập trang tính kiểu bên ngoài

    ```css
    @import url("css/layout.css");
    @import url("css/color.css");
    body {
        color: blue;
        font-size: 14px;
    }
    ```
