**Author:** _Mai Thế Hào_

# 🌟 **QUY TẮC TỔ CHỨC VÀ XÂY DỰNG DỰ ÁN** 🌟

---

## 📁 **1. CẤU TRÚC FOLDER VÀ FILE**

### 🗂️ **1.1. TỔ CHỨC FOLDER**

-   Mỗi folder cần có một file `README.md` (viết hoa toàn bộ):
    -   **Mục đích**:
        -   Mô tả sơ lược về mục đích và nội dung của folder.
        -   Đảm bảo người đọc dễ hình dung về vai trò của folder.
-   Mỗi repository cần có một file `folderStruct.md`:
    -   **Mục đích**:
        -   Tóm tắt cấu trúc thư mục của repository hiện tại.
    -   Cập nhật khi có thay đổi cấu trúc, giúp leader quản lý và người đọc dễ tìm kiếm.
    -   Sử dụng lệnh `git ls-tree -r HEAD --name-only` để lấy cấu trúc folder nhanh chóng.
        -   **Mục đích**:
            -   Nhanh chóng có được danh sách các file và folder trong repository.
            -   Dễ dàng cập nhật và chỉnh sửa cấu trúc folder.
        -   Sử dụng các trang web vẽ sơ đồ cây để chỉnh sửa cấu trúc folder hợp lý.
            -   Ví dụ: https://www.text-2-tree.com/
-   Mọi repository đều phải để file `rules.md` này vào thư mục gốc của repository:
    -   **Mục đích**:
        -   Đảm bảo tất cả thành viên đều nắm rõ quy tắc tổ chức và xây dựng dự án.
        -   Dễ dàng truy cập và tham khảo khi cần thiết.

### **1.2. QUY TẮC ĐẶT TÊN**

-   Sử dụng **snake_case** cho tên folder và file:
    -   Ví dụ: `javascript_asynchronous`, `js_async`.
    -   Ngoại trừ các trường hợp các từ viết tắt kỹ thuật như DOM, ES6, HTML, CSS, JS...
        -   **Trường hợp đặc biệt là README.md**
-   Tên folder và file:
    -   Đặt hợp lý, đúng trọng tâm.
    -   Tránh sử dụng tên chung chung, thiếu ý nghĩa.
    -   Không sử dụng ký tự đặc biệt, khoảng trắng hoặc chữ in hoa (ngoại trừ các từ viết tắt kỹ thuật).
    -   Đảm bảo tên ngắn gọn nhưng đủ để mô tả nội dung.
    -   Sử dụng tiếng Anh cho tên file và folder để đảm bảo tính nhất quán và dễ hiểu cho tất cả thành viên.
-   Ví dụ:
    -   `project_overview.md`
    -   `user_guide.md`
    -   `api_reference.md`
    -   `css_styles`
    -   `html_templates`
-   Đối với các file tài liệu, tên file phải phản ánh đúng nội dung và chủ đề của tài liệu.
    -   Ví dụ:
        -   `installation_guide.md`
        -   `troubleshooting.md`
        -   `release_notes.md`
-   Đối với các folder, tên folder phải phản ánh đúng nội dung chứa bên trong.
    -   Ví dụ:
        -   `images`
        -   `scripts`
        -   `styles`
        -   `docs`
-   Đảm bảo tên file và folder không trùng lặp trong cùng một cấp thư mục để tránh nhầm lẫn.

### **1.3. CHIA NHỎ NỘI DUNG**

-   Phân tách nội dung thành nhiều file hoặc folder con thay vì lồng ghép:
    -   **Mục đích**:
        -   Dễ phân biệt, tìm kiếm.
        -   Dễ quản lý và chỉnh sửa.
    -   Ví dụ: Folder "javaScript" có thể chứa các file như:
        -   `basics.md`
        -   `DOM.md`
        -   `ES6.md`

### **1.4. QUY TẮC VIẾT TÀI LIỆU**

-   Tên file tài liệu `.md` phải được đặt bằng tiếng Anh và phải phản ánh đúng chủ đề của tài liệu.
    -   **Mục đích**:
        -   Giúp dễ dàng nhận diện và tìm kiếm tài liệu.
        -   Tạo sự nhất quán và chuyên nghiệp trong dự án.
-   🖋️ Trong phần nội dung của tài liệu, hãy viết bằng tiếng Việt. Các thuật ngữ kỹ thuật và từ khóa cần được viết bằng tiếng Anh hoặc sử dụng dấu `(` và `)` để chú thích.
    -   **Mục đích**:
        -   Đảm bảo tài liệu dễ đọc và hiểu cho người dùng nói tiếng Việt.
        -   Giúp người đọc dễ dàng nhận diện các thuật ngữ kỹ thuật chuẩn.
    -   Ví dụ:
        -   “Sử dụng `JavaScript` (JS) để xử lý dữ liệu...”
        -   “Ứng dụng `HTML` (Hypertext Markup Language) là nền tảng cơ bản cho việc xây dựng web...”

---

## 🛠️ **2. QUY TẮC SỬ DỤNG GIT**

### **2.1. QUẢN LÝ CẬP NHẬT**

-   **Luôn cập nhật dữ liệu trước khi tiếp tục làm việc**:
    -   Sử dụng lệnh `git pull` trước khi chỉnh sửa.
    -   Giảm thiểu khả năng xảy ra conflict.
-   **Xử lý conflict**:
    -   Hãy xử lý xung đột cẩn thận và thảo luận với team nếu cần.

### **2.2. COMMIT CHI TIẾT**

-   Viết commit rõ ràng, cụ thể:

    -   **Tiêu đề**: Tóm tắt hành động thực hiện (ví dụ: tạo, chỉnh sửa, cập nhật, xóa).
    -   **Nội dung chi tiết**: Liệt kê các file được thay đổi và lý do.
    -   Ví dụ:

        ```markdown
        create javaScriptSyntax.md in userManagement

        -   description. (có thể có)
        ```

### **2.3. SỬ DỤNG NHÁNH RIÊNG**

-   Tạo nhánh riêng ngoài `main` hoặc `master`:
    -   Phân chia công việc rõ ràng.
    -   Tránh xung đột không cần thiết.
-   Khi hoàn thành công việc, merge nhánh vào `main` sau khi kiểm tra cẩn thận.

---

## ⚡ **3. LƯU Ý BỔ SUNG**

-   **File `.gitignore`:**
    -   Quản lý dự án hiệu quả hơn.
    -   Loại trừ tất cả các file không phải `.md`.
-   **Chỉ commit khi file đã hoàn chỉnh**:
    -   Hạn chế việc chỉnh sửa nhiều lần không cần thiết.
    -   Đảm bảo file đủ nội dung và chất lượng.

---

## 🗂️ **4. MẪU CẤU TRÚC FOLDER**

### **4.1. VÍ DỤ:**

```plaintext
repositoryRoot/
│
├── folderStruct.md        # Sơ lược cấu trúc folder của repository
├── parentFolder/
│   ├── README.md          # Mô tả nội dung folder
│   ├── fatherDoc1.md      # Chi tiết nội dung chủ đề con
│   ├── fatherDoc2.md      # Chi tiết nội dung chủ đề con
│   └── childFolder/       # Folder con
│       ├── README.md      # Mô tả mục đích của folder childFolder
│       └── childDoc1.md
├── anotherFolder/
│   ├── README.md
│   └── example.md
└── .gitignore             # Loại bỏ file không cần thiết
```

### **4.2. QUY TẮC MỞ RỘNG**

-   **Cập nhật `folderStruct.md` khi có thay đổi cấu trúc**:
    -   Mục đích: Dễ quản lý và đồng bộ.
-   **Chia nhỏ nội dung vào folder và file con hợp lý**:
    -   Tránh đặt quá nhiều nội dung vào một file.

---

## 🎯 **5. KẾT LUẬN**

-   Quy tắc trên đảm bảo việc tổ chức file và folder chặt chẽ, dễ quản lý.
-   Hạn chế tối đa xung đột khi làm việc nhóm và cải thiện năng suất làm việc.
-   Mọi thành viên nên tuân thủ các quy tắc trên để đảm bảo sự thống nhất và hiệu quả trong dự án.

---

## ⚙️ **6. TỔNG HỢP CÁC LỆNH GIT QUAN TRỌNG TRONG DỰ ÁN**

### 🛠️ **6.1. CẬP NHẬT VÀ ĐỒNG BỘ HÓA**

-   `git pull`: Kéo dữ liệu từ repository gốc để cập nhật với thay đổi mới nhất.
-   `git fetch`: Lấy dữ liệu từ remote repository mà không tự động merge.

### 🚧 **6.2. QUẢN LÝ NHÁNH**

-   `git branch`: Liệt kê tất cả các nhánh hiện tại.
-   `git branch <tên-nhánh>`: Tạo nhánh mới.
-   `git checkout <tên-nhánh>`: Chuyển sang nhánh khác.
-   `git checkout -b <tên-nhánh>`: Tạo và chuyển sang nhánh mới.
-   `git merge <tên-nhánh>`: Gộp thay đổi từ nhánh khác vào nhánh hiện tại.
-   `git rebase <tên-nhánh>`: Đưa các thay đổi từ một nhánh lên trên một nhánh khác.

### 📝 **6.3. COMMIT VÀ QUẢN LÝ LỊCH SỬ**

-   `git add <file>`: Thêm file vào staging area.
-   `git commit -m "message"`: Lưu thay đổi với thông điệp commit.
-   `git commit -a -m "message"`: Tự động thêm và commit tất cả các file đã thay đổi.
-   `git log`: Xem lịch sử commit.
-   `git diff`: Xem sự khác biệt giữa các phiên bản.

### 🔄 **6.4. XỬ LÝ XUNG ĐỘT**

-   `git status`: Kiểm tra trạng thái của repository và file.
-   `git mergetool`: Sử dụng công cụ để giải quyết xung đột merge.

### 🗑️ **6.5. QUẢN LÝ FILE**

-   `git rm <file>`: Xóa file khỏi repository và staging area.
-   `git reset <file>`: Xóa file khỏi staging area nhưng giữ nguyên thay đổi trong working directory.
-   `git clean -f`: Xóa các file không được theo dõi.

### 🔧 **6.6. QUẢN LÝ REMOTE**

-   `git remote -v`: Hiển thị danh sách các remote repository.
-   `git remote add <tên> <url>`: Thêm remote repository mới.
-   `git push <remote> <branch>`: Đẩy thay đổi lên remote repository.
-   `git pull <remote> <branch>`: Kéo thay đổi từ remote repository.

### ⚠️ **6.7. KHÔI PHỤC VÀ SỬA ĐỔI**

-   `git revert <commit-hash>`: Tạo một commit mới để đảo ngược thay đổi từ commit cụ thể.
-   `git reset --hard <commit-hash>`: Khôi phục trạng thái working directory và staging area về một commit cụ thể (dùng cẩn thận, dữ liệu sẽ bị mất).
-   `git stash`: Tạm lưu thay đổi chưa commit để làm việc khác.
-   `git stash pop`: Khôi phục các thay đổi từ stash.

---

# 🌐 CÁC TIỆN ÍCH HỖ TRỢ VIẾT DOC

## 📎 Các icon trong ASCII: https://emojipedia.org/

## 🌲 Tạo cấu trúc cây: https://www.text-2-tree.com/

## ✍️ Hỗ trợ viết bằng file .md (Mark Down): https://dillinger.io/

---

# 🔗 LINK GIT TỔNG HỢP: https://github.com/MaiTheHao/MyDocument.git
