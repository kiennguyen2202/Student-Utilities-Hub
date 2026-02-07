# HƯỚNG DẪN QUY TRÌNH GIT & PHÂN CÔNG (Student Utilities Hub)

**Chào cả nhóm,**
Core layout đã xong và nằm trên nhánh main/develop. Bây giờ mọi người hãy làm theo chính xác từng bước dưới đây để code tính năng của mình mà không bị conflict nhé.

---

## 1. BẢNG PHÂN CÔNG NHIỆM VỤ

Mỗi bạn sẽ chịu trách nhiệm **tạo mới một file HTML** trong thư mục `tools/`. Tuyệt đối không sửa file của người khác để tránh xung đột code.

| Thành Viên | Tính Năng (Feature) | Tên Nhánh (Branch Name) | File Cần Tạo |
| :--- | :--- | :--- | :--- |
| **Vari** | Tính điểm GPA | `feature/gpa-calculator` | `tools/gpa.html` |
| **Kiệt** | To-Do List | `feature/todo-list` | `tools/todo.html` |
| **An** | Đồng hồ Pomodoro | `feature/pomodoro-timer` | `tools/timer.html` |
| **Thanh** | Máy tính bỏ túi | `feature/simple-calculator` | `tools/calc.html` |
| **Quân** | Random Picker | `feature/random-picker` | `tools/random.html` |
| **Quỳnh** | Ghi chú nhanh (Note) | `feature/quick-note` | `tools/note.html` |

---

## 2. QUY TRÌNH THỰC HIỆN CHI TIẾT

### BƯỚC 1: Lấy code mới nhất (Clone & Pull)
Mở Terminal (VS Code hoặc Git Bash) và chạy lệnh:

```bash
# 1. Clone dự án (Nếu máy chưa có dự án) - Chỉ làm 1 lần đầu
git clone <LINK_GITHUB_CUA_LEAD>

# 2. Di chuyển vào thư mục dự án
cd Student-Utilities-Hub

# 3. Chuyển sang nhánh develop (Nhánh phát triển chung)
git checkout develop

# 4. Cập nhật code mới nhất từ Lead về máy (BẮT BUỘC trước khi code)
git pull origin develop
```

### BƯỚC 2: Tạo nhánh làm việc riêng (Feature Branch)
**Tuyệt đối không code trực tiếp trên nhánh `develop` hoặc `main`.**
Hãy tạo nhánh riêng theo tên đã phân công ở bảng trên.

*Ví dụ (Nếu bạn là **Vari**):*
```bash
git checkout -b feature/gpa-calculator
```
*(Lệnh này nghĩa là: Tạo nhánh mới tên là ... và chuyển sang đó luôn)*

### BƯỚC 3: Code và Commit (Yêu cầu tối thiểu 2 Commits)

1.  Vào thư mục `tools/`, tạo file HTML tương ứng của bạn (ví dụ Vari tạo `gpa.html`).
2.  Viết code HTML/CSS/JS cho tính năng đó. Tham khảo cách đặt class CSS từ file `style.css` gốc để đồng bộ giao diện.
3.  **Commit Lần 1 (Code sườn):**
    ```bash
    git add .
    git commit -m "Create initial UI for [Ten_Tinh_Nang]"
    ```
4.  Tiếp tục chỉnh sửa, thêm JS, sửa lỗi...
5.  **Commit Lần 2 (Hoàn thiện):**
    ```bash
    git add .
    git commit -m "Finish logic for [Ten_Tinh_Nang]"
    ```

### BƯỚC 4: Đẩy code lên GitHub (Push)
Sau khi đã code xong và commit đủ, hãy đẩy nhánh của bạn lên server:

```bash
git push origin feature/[ten-nhanh-cua-ban]
```
*Ví dụ:* `git push origin feature/gpa-calculator`

### BƯỚC 5: Tạo Pull Request (PR) để nộp bài
Đây là bước quan trọng để merge code vào dự án chung.

1.  Truy cập vào trang GitHub/GitLab của dự án.
2.  Bạn sẽ thấy thông báo *"feature/... had recent pushes"*. Bấm nút **Compare & pull request** màu xanh lá.
3.  **Cấu hình PR (Rất quan trọng):**
    *   **Base branch (Mũi tên hướng vào):** `develop` (⚠️ KHÔNG chọn main).
    *   **Compare branch (Mũi tên đi ra):** `feature/[nhanh-cua-ban]`.
4.  Tiêu đề PR: `[Feature] Tên tính năng - Tên thành viên`.
5.  Bấm **Create Pull Request**.
6.  Copy link PR và gửi vào nhóm chat.

---

## 3. LƯU Ý FINAL
*   **Conflict:** Nếu làm đúng quy trình trên (mỗi người 1 file riêng, 1 nhánh riêng), sẽ không bao giờ bị conflict.
*   **Merge:** **Chỉ Team Lead mới được bấm nút Merge Pull Request**. Các thành viên khác chỉ tạo PR và chờ duyệt.
*   **Hotfix (Nếu có):** Nếu phát hiện lỗi sau khi merge, hãy báo Lead để tạo nhánh `hotfix/` sửa lỗi.

**Chúc nhóm mình 10 điểm! 🚀**
