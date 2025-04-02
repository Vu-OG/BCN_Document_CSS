**Author:** Nguyễn Minh Vũ
# 🌟 **Các Phương Pháp Áp Dụng CSS Trong HTML** 🌟

## **Giới Thiệu**
- CSS (Cascading Style Sheets) là một ngôn ngữ dùng để định dạng các phần tử HTML trên trang web. Có nhiều cách khác nhau để áp dụng CSS vào HTML, mỗi phương pháp đều có ưu điểm và trường hợp sử dụng riêng. Trong tài liệu này, chúng ta sẽ tìm hiểu ba phương pháp chính để áp dụng CSS trong HTML: Inline, Internal, và External.

## **1. Style Nội Tuyến (Inline Style)**
### Định Nghĩa:
- Style nội tuyến cho phép bạn áp dụng CSS trực tiếp vào một phần tử HTML thông qua thuộc tính style.

### Cú Pháp:
```
<element style="property: value;">
```

### Ví Dụ:
```
<p style="color: red; font-size: 16px;">Đây là một đoạn văn bản màu đỏ.</p>
```

### Ưu điểm:
- Dễ dàng và nhanh chóng cho những thay đổi nhỏ.
- Hữu ích cho việc áp dụng kiểu dáng cho một phần tử duy nhất.

### Nhược Điểm:
- Không thể tái sử dụng.
- Làm cho HTML trở nên lộn xộn và khó bảo trì.

## **2. Bảng Kiểu Nội Bộ (Internal Style Sheet)**
### Định Nghĩa:
- Bảng kiểu nội bộ được viết trong thẻ `<style>` trong phần `<head>` của tài liệu HTML. Nó áp dụng kiểu dáng cho toàn bộ tài liệu.

### Cú pháp:
```
<head>
  <style>
    element { 
      property: value; 
    }
  </style>
</head>
```

### Ví dụ:
```
<!DOCTYPE html>
<html>
<head>
  <style>
    p {
      color: blue;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <p>Đây là một đoạn văn bản màu xanh.</p>
</body>
</html>
```

### Ưu điểm:
- Dễ quản lý hơn so với Inline CSS.
- Có thể áp dụng cho nhiều phần tử trên trang web.

### Nhược điểm:
- Chỉ áp dụng cho một tài liệu HTML cụ thể.
- Không thể tái sử dụng trên nhiều trang khác nhau.

## **3. Bảng Kiểu Ngoài (External Style Sheet)**
### Định Nghĩa:
- Bảng kiểu ngoài được lưu trong một tệp riêng có phần mở rộng `.css`. Tệp CSS này có thể liên kết với một hoặc nhiều tài liệu HTML bằng thẻ `<link>`.

### Cú pháp:
1. **Tạo file `style.css`**
```
p {
  color: green;
  font-size: 20px;
}
```

2. **Liên kết file CSS vào HTML**
```
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
```

### Ví dụ:
```
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <p>Đây là một đoạn văn bản màu xanh lá.</p>
</body>
</html>
```

### Ưu điểm:
- Tái sử dụng dễ dàng trên nhiều trang HTML khác nhau.
- Giúp mã HTML gọn gàng hơn.
- Dễ bảo trì và quản lý.

### Nhược điểm:
- Cần tải thêm một file CSS, có thể làm chậm tốc độ tải trang.
- Khi kết nối bị mất, CSS có thể không được áp dụng.

## **So Sánh Giữa Các Phương Pháp**
| Phương Pháp | Ưu Điểm | Nhược Điểm |
|-------------|---------|------------|
| Inline | Dễ dàng, nhanh chóng | Khó bảo trì, không tái sử dụng |
| Internal | Quản lý tốt hơn Inline, áp dụng cho toàn bộ trang | Không dùng lại được ở nhiều trang |
| External | Tái sử dụng, gọn gàng, dễ bảo trì | Cần tải thêm file, phụ thuộc vào kết nối |

## **Kết Luận**
- **Inline CSS** thích hợp cho các chỉnh sửa nhỏ hoặc thử nghiệm nhanh.
- **Internal CSS** phù hợp với các trang đơn lẻ cần nhiều quy tắc kiểu dáng.
- **External CSS** là phương pháp tối ưu khi xây dựng các trang web lớn với nhiều trang.

Lựa chọn phương pháp phù hợp sẽ giúp bạn quản lý dự án hiệu quả và cải thiện trải nghiệm người dùng trên trang web của mình.
