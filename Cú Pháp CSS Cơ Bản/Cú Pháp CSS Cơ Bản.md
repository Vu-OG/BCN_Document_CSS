# Cú Pháp CSS Cơ Bản

## 1. Giới Thiệu
CSS (Cascading Style Sheets) là ngôn ngữ dùng để mô tả cách trình bày của tài liệu HTML. Cú pháp CSS giúp định dạng màu sắc, kích thước, bố cục và nhiều yếu tố khác trên trang web.

## 2. Cấu Trúc Cú Pháp CSS
Một quy tắc CSS cơ bản gồm 3 phần chính:
```css
tagname {
  property: value;
}
```
### Giải thích:
- `tagname`: Selector dùng để chọn phần tử HTML cần định dạng.
- `property`: Thuộc tính cần thay đổi (ví dụ: màu sắc, kích thước, khoảng cách,...).
- `value`: Giá trị của thuộc tính đó.

Ví dụ:
```css
p {
  color: blue;
  font-size: 16px;
}
```
Quy tắc trên sẽ làm cho tất cả đoạn văn (`<p>`) có màu xanh và kích thước chữ là 16px.

## 3. Các Kiểu Selector Trong CSS

### 3.1. Selector Theo Thẻ
Chọn tất cả các phần tử có cùng tên thẻ.
```css
div {
  background-color: lightgray;
}
```

### 3.2. Selector Theo Class
Chọn tất cả các phần tử có class cụ thể.
```css
.box {
  width: 100px;
  height: 100px;
  background-color: yellow;
}
```
```html
<div class="box"></div>
```

### 3.3. Selector Theo ID
Chọn phần tử có ID cụ thể.
```css
#header {
  font-size: 24px;
}
```
```html
<h1 id="header">Tiêu đề</h1>
```

### 3.4. Selector Tổng Quát (`*`)
Chọn tất cả các phần tử trên trang.
```css
* {
  margin: 0;
  padding: 0;
}
```

## 4. Kết Luận
CSS là một phần quan trọng giúp trang web trở nên đẹp và chuyên nghiệp hơn. Việc hiểu rõ cú pháp CSS giúp bạn dễ dàng quản lý và chỉnh sửa giao diện trang web.

