# Tính Toán Độ Ưu Tiên (Specificity) Trong CSS

## 1. Giới thiệu về Specificity
Specificity (độ ưu tiên) trong CSS là một thuật toán xác định quy tắc CSS nào sẽ được áp dụng cho một phần tử khi có nhiều quy tắc cùng nhắm đến phần tử đó. Độ ưu tiên cao hơn sẽ ghi đè độ ưu tiên thấp hơn.

## 2. Cách tính Specificity
Specificity được tính theo công thức:
- **Inline Styles**: 1000
- **ID selectors** (`#id`): 100
- **Class, Attribute & Pseudo-classes** (`.class`, `[attribute]`, `:hover`): 10
- **Element & Pseudo-elements** (`div`, `p`, `::before`): 1
- **Universal Selector (`*`)** không có độ ưu tiên.

## 3. Bảng Ví Dụ Tính Specificity
| Selector                 | Specificity Value | Calculation         |
|--------------------------|------------------|---------------------|
| `p`                      | 1                | 1                   |
| `p.test`                 | 11               | 1 + 10              |
| `p#demo`                 | 101              | 1 + 100             |
| `<p style="color: pink;">` | 1000             | 1000                |
| `#demo`                  | 100              | 100                 |
| `.test`                  | 10               | 10                  |
| `p.test1.test2`          | 21               | 1 + 10 + 10         |
| `#navbar p#demo`         | 201              | 100 + 1 + 100       |
| `*`                      | 0                | 0                   |

## 4. Quy Tắc Khi Áp Dụng Specificity
1. Nếu hai quy tắc có cùng độ ưu tiên, quy tắc nào xuất hiện sau sẽ được áp dụng.
2. Inline styles luôn có độ ưu tiên cao nhất (1000).
3. ID selector có độ ưu tiên cao hơn Class và Element.
4. Class, Attributes và Pseudo-classes có độ ưu tiên cao hơn Element và Pseudo-elements.
5. Universal selector (`*`) không ảnh hưởng đến độ ưu tiên.

## 5. Ví Dụ Cụ Thể
```css
/* Specificity: 1 */
p {
  color: blue;
}

/* Specificity: 10 */
.test {
  color: red;
}

/* Specificity: 100 */
#demo {
  color: green;
}

/* Specificity: 1000 (Inline Style) */
<p id="demo" class="test" style="color: pink;">Hello World</p>
```
**Kết quả:** Văn bản "Hello World" sẽ có màu hồng do inline style có specificity cao nhất.

## 6. Kết Luận
Hiểu rõ về specificity giúp bạn kiểm soát cách các quy tắc CSS áp dụng lên trang web một cách chính xác, tránh lỗi ghi đè không mong muốn. Hãy luôn kiểm tra độ ưu tiên khi viết CSS để đảm bảo trang web hiển thị đúng như mong đợi.

