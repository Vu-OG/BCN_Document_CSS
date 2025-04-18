**Author:** Nguyễn Minh Vũ

# Flex Shrink Trong CSS

## 1. Giới Thiệu
`flex-shrink` là một thuộc tính trong CSS Flexbox, dùng để xác định mức độ một phần tử con (flex item) có thể thu nhỏ lại khi tổng kích thước của các flex items vượt quá kích thước của flex container. Thuộc tính này rất hữu ích trong việc kiểm soát cách các phần tử co lại để vừa với không gian giới hạn, đặc biệt trong các thiết kế responsive.

## 2. Cú Pháp Và Cách Sử Dụng Flex Shrink
Thuộc tính `flex-shrink` được áp dụng cho các phần tử con trong một flex container (đã kích hoạt bằng `display: flex;`). Cú pháp cơ bản như sau:
```css
.item {
  flex-shrink: value;
}
```
### Giải thích:
- `.item`: Selector xác định phần tử con (flex item) trong flex container.
- `flex-shrink`: Thuộc tính xác định khả năng thu nhỏ của phần tử.
- `value`: Giá trị là một số không âm (thường là số nguyên như 0, 1, 2,...), biểu thị tỷ lệ thu nhỏ so với các phần tử khác.

Ví dụ:
```css
.container {
  display: flex;
  width: 300px; /* Container có giới hạn chiều rộng */
}
.item1 {
  flex-shrink: 1;
  width: 150px;
  background-color: lightblue;
}
.item2 {
  flex-shrink: 2;
  width: 150px;
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
- Tổng kích thước ban đầu của `item1` và `item2` là 300px (150px + 150px), bằng chiều rộng của container, nên không cần thu nhỏ.
- Nếu container nhỏ hơn (ví dụ: 200px), các item sẽ thu nhỏ. `item2` với `flex-shrink: 2` sẽ co lại nhiều hơn `item1` (có `flex-shrink: 1`), theo tỷ lệ 2:1.

### Cách Hoạt Động
- Giá trị mặc định của `flex-shrink` là `1`, nghĩa là flex item sẽ thu nhỏ đều khi cần thiết.
- Nếu `flex-shrink: 0`, phần tử sẽ không thu nhỏ, giữ nguyên kích thước ban đầu bất kể không gian container.
- Tỷ lệ thu nhỏ được tính dựa trên giá trị `flex-shrink` và kích thước ban đầu của flex item (thường là `width` hoặc `flex-basis`).

Ví dụ với `flex-shrink: 0`:
```css
.container {
  display: flex;
  width: 200px;
}
.item1 {
  flex-shrink: 0;
  width: 150px;
  background-color: lightcoral;
}
.item2 {
  flex-shrink: 1;
  width: 150px;
  background-color: lightyellow;
}
```
```html
<div class="container">
  <div class="item1">Item 1</div>
  <div class="item2">Item 2</div>
</div>
```
Ở đây, `item1` giữ nguyên 150px và tràn ra ngoài container (overflow), trong khi `item2` thu nhỏ để vừa với không gian còn lại.

### Kết Hợp Với Flex Basis Và Flex Grow
`flex-shrink` thường hoạt động cùng `flex-basis` và `flex-grow`:
```css
.container {
  display: flex;
  width: 400px;
}
.item1 {
  flex-basis: 200px;
  flex-shrink: 1;
  flex-grow: 1;
  background-color: lightblue;
}
.item2 {
  flex-basis: 300px;
  flex-shrink: 2;
  flex-grow: 1;
  background-color: lightgreen;
}
```
- `flex-basis` đặt kích thước ban đầu (200px và 300px).
- Nếu container nhỏ hơn 500px, `flex-shrink` quyết định mức độ thu nhỏ (2:1).
- Nếu container lớn hơn 500px, `flex-grow` quyết định mức độ mở rộng.

## 3. Ứng Dụng Thực Tế Của Flex Shrink
`flex-shrink` thường được sử dụng để:
- Đảm bảo các phần tử co lại hợp lý trong không gian hạn chế, tránh tràn nội dung.
- Tạo layout responsive, nơi các phần tử tự điều chỉnh khi kích thước màn hình thay đổi.
- Kiểm soát tỷ lệ thu nhỏ giữa các phần tử, ví dụ: giữ một phần tử cố định và để phần tử khác co lại.

Ví dụ thực tế - Thanh công cụ responsive:
```css
.container {
  display: flex;
  width: 100%;
  max-width: 300px;
}
.logo {
  flex-shrink: 0;
  width: 100px;
  background-color: #f0f0f0;
}
.content {
  flex-shrink: 1;
  width: 200px;
  background-color: #e0e0e0;
}
```
```html
<div class="container">
  <div class="logo">Logo</div>
  <div class="content">Content</div>
</div>
```
Trong ví dụ này, `.logo` không thu nhỏ (giữ 100px), còn `.content` co lại khi container nhỏ hơn 300px.

## 4. Kết Luận
`flex-shrink` là một thuộc tính quan trọng trong Flexbox, giúp bạn kiểm soát cách các flex items thu nhỏ khi không gian bị giới hạn. Với khả năng điều chỉnh tỷ lệ co lại, nó mang lại sự linh hoạt trong thiết kế bố cục, đặc biệt khi làm việc với các giao diện cần thích nghi trên nhiều thiết bị. Kết hợp với `flex-grow` và `flex-basis`, `flex-shrink` hoàn thiện bộ công cụ để tạo ra các layout hiện đại và hiệu quả.