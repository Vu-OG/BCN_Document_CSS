**Author:** Nguyễn Minh Vũ

# Flex Basis Trong CSS

## 1. Giới Thiệu
`flex-basis` là một thuộc tính trong CSS Flexbox, dùng để xác định kích thước ban đầu của một phần tử con (flex item) trước khi không gian trống trong flex container được phân phối bởi các thuộc tính như `flex-grow` hoặc `flex-shrink`. Thuộc tính này đóng vai trò quan trọng trong việc thiết lập kích thước cơ sở của flex items, giúp kiểm soát bố cục một cách chính xác.

## 2. Cú Pháp Và Cách Sử Dụng Flex Basis
Thuộc tính `flex-basis` được áp dụng cho các phần tử con trong một flex container (đã kích hoạt bằng `display: flex;`). Cú pháp cơ bản như sau:
```css
.item {
  flex-basis: value;
}
```
### Giải thích:
- `.item`: Selector xác định phần tử con (flex item) trong flex container.
- `flex-basis`: Thuộc tính xác định kích thước ban đầu của phần tử theo trục chính (main axis).
- `value`: Giá trị có thể là một đơn vị độ dài (`px`, `%`, `em`, `rem`), từ khóa `auto`, hoặc `content`.

Ví dụ:
```css
.container {
  display: flex;
}
.item1 {
  flex-basis: 200px;
  background-color: lightblue;
}
.item2 {
  flex-basis: 100px;
  background-color: lightgreen;
}
```
```html
<div class="container">
  <div class="item1">Item 1</div>
  <div class="item2">Item 2</div>
</div>
```
Trong ví dụ trên:
- `item1` có kích thước ban đầu là 200px.
- `item2` có kích thước ban đầu là 100px.
- Kích thước này được áp dụng theo trục chính (mặc định là chiều ngang nếu `flex-direction` là `row`).

### Cách Hoạt Động
- Giá trị mặc định của `flex-basis` là `auto`, nghĩa là kích thước ban đầu của phần tử được lấy từ thuộc tính `width` (hoặc `height` nếu trục chính là dọc) hoặc dựa trên nội dung của nó.
- `flex-basis` xác định kích thước cơ sở trước khi `flex-grow` mở rộng hoặc `flex-shrink` thu nhỏ phần tử để phù hợp với không gian container.
- Nếu `flex-direction` là `row`, `flex-basis` ảnh hưởng đến chiều rộng; nếu là `column`, nó ảnh hưởng đến chiều cao.

Ví dụ với `auto`:
```css
.container {
  display: flex;
}
.item1 {
  flex-basis: auto;
  width: 150px;
  background-color: lightcoral;
}
.item2 {
  flex-basis: 50%;
  background-color: lightyellow;
}
```
```html
<div class="container">
  <div class="item1">Item 1</div>
  <div class="item2">Item 2</div>
</div>
```
Ở đây, `item1` lấy kích thước ban đầu từ `width: 150px`, trong khi `item2` chiếm 50% chiều rộng của container.

### Kết Hợp Với Flex Grow Và Flex Shrink
`flex-basis` thường hoạt động cùng `flex-grow` và `flex-shrink`:
```css
.container {
  display: flex;
}
.item1 {
  flex-basis: 100px;
  flex-grow: 1;
  background-color: lightblue;
}
.item2 {
  flex-basis: 200px;
  flex-grow: 2;
  background-color: lightgreen;
}
```
Trong trường hợp này:
- `item1` bắt đầu với 100px, sau đó mở rộng với tỷ lệ 1 phần không gian trống.
- `item2` bắt đầu với 200px, mở rộng với tỷ lệ 2 phần không gian trống.

## 3. Ứng Dụng Thực Tế Của Flex Basis
`flex-basis` thường được sử dụng để:
- Đặt kích thước ban đầu cố định cho các flex items trước khi phân phối không gian.
- Tạo bố cục với các phần tử có kích thước cơ sở khác nhau nhưng vẫn linh hoạt khi container thay đổi kích thước.
- Kết hợp với `flex-grow` để kiểm soát tỷ lệ mở rộng.

Ví dụ thực tế - Layout cột:
```css
.container {
  display: flex;
  width: 100%;
}
.sidebar {
  flex-basis: 300px;
  background-color: #f0f0f0;
}
.main {
  flex-basis: auto;
  flex-grow: 1;
  background-color: #e0e0e0;
}
```
```html
<div class="container">
  <div class="sidebar">Sidebar</div>
  <div class="main">Main Content</div>
</div>
```
Trong ví dụ này, `.sidebar` có kích thước ban đầu 300px, trong khi `.main` mở rộng để lấp đầy phần còn lại nhờ `flex-grow: 1`.

## 4. Kết Luận
`flex-basis` là một thuộc tính quan trọng trong Flexbox, cho phép bạn thiết lập kích thước ban đầu của các flex items một cách linh hoạt và chính xác. Khi kết hợp với các thuộc tính khác như `flex-grow` và `flex-shrink`, nó mang lại khả năng kiểm soát bố cục vượt trội, giúp tạo ra giao diện đẹp và responsive trong thiết kế web hiện đại.