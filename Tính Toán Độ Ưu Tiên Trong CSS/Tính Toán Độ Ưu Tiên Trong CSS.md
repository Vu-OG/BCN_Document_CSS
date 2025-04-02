# Tính Toán Độ Ưu Tiên (Specificity) Trong CSS

## 1. Độ Ưu Tiên Trong CSS Là Gì?
CSS Specificity (độ ưu tiên trong CSS) quyết định quy tắc CSS nào sẽ được áp dụng cho một phần tử khi có nhiều quy tắc khác nhau cùng tác động. 

## 2. Nguyên Tắc Tính Specificity
Specificity được tính dựa trên loại selector sử dụng, theo công thức:

```
inline styles > ID selectors > Class, attribute, pseudo-class selectors > Element selectors
```

- **Inline styles** (`style=""` trong HTML) có độ ưu tiên cao nhất (1000 điểm).
- **ID selectors** (`#id`) có độ ưu tiên tiếp theo (100 điểm).
- **Class, attribute, pseudo-class selectors** (`.class`, `[attribute]`, `:hover`, `:nth-child`) có độ ưu tiên trung bình (10 điểm).
- **Element selectors** (`div`, `p`, `h1`,...) có độ ưu tiên thấp nhất (1 điểm).
- **Universal selector (`*`)** và các thuộc tính kế thừa từ phần tử cha có độ ưu tiên thấp nhất (0 điểm).

## 3. Bảng Minh Họa Specificity

| Selector | Specificity Value | Cách tính |
|----------|------------------|-----------|
| `p` | 1 | 1 |
| `p.test` | 11 | 1 + 10 |
| `p#demo` | 101 | 1 + 100 |
| `#demo` | 100 | 100 |
| `.test` | 10 | 10 |
| `p.test1.test2` | 21 | 1 + 10 + 10 |
| `#navbar p#demo` | 201 | 100 + 1 + 100 |
| `*` | 0 | 0 (bị bỏ qua) |
| `style="color: pink;"` | 1000 | 1000 (inline styles) |

## 4. Ví Dụ Cụ Thể
Giả sử có các quy tắc CSS sau:
```css
h1 {
  color: blue;
}

h1.special {
  color: green;
}

#title {
  color: red;
}
```
Và HTML:
```html
<h1 id="title" class="special">Tiêu đề</h1>
```
Màu chữ của tiêu đề sẽ là **đỏ** vì `#title` có specificity cao hơn `.special` và `h1`.

## 5. Cách Giải Quyết Xung Đột Specificity
- Sử dụng selectors cụ thể hơn khi cần.
- Dùng `!important` để ghi đè quy tắc (nhưng tránh lạm dụng).
- Sắp xếp quy tắc CSS hợp lý để tránh xung đột không mong muốn.

## 6. Kết Luận
Hiểu về specificity giúp bạn kiểm soát cách CSS áp dụng vào phần tử một cách chính xác, tránh xung đột không mong muốn trong thiết kế web.

