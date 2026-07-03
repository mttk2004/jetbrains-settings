# Danh sách Phím tắt JetBrains (kiet keymap)

Tài liệu này liệt kê toàn bộ các phím tắt tùy chỉnh trong file cấu hình [keymaps/kiet.xml](file:///home/kiet/projects/settings/keymaps/kiet.xml), được phân chia theo nhóm chức năng để dễ tra cứu.

> [!NOTE]
> *   `F19` là phím **Caps Lock** đã được remapped trên hệ thống Linux.
> *   Các phím tắt dạng chuỗi (chord) yêu cầu gõ tuần tự (ví dụ: nhấn `Alt+K` trước, sau đó nhấn tiếp `Alt+N`).

---

## 1. General & UI Toggles (Cài đặt chung & Ẩn/Hiện UI)

| Action ID | Chức năng | Phím tắt 1 | Phím tắt 2 (F19 Layer) |
| :--- | :--- | :--- | :--- |
| `OpenInlineChatAction` | Mở khung chat AI (AI Assistant) | `Ctrl + Shift + G` | `F19 + C` |
| `ToggleFullScreen` | Bật/Tắt chế độ toàn màn hình | `Alt + F11` | |
| `EditorToggleShowLineNumbers` | Ẩn/Hiện số dòng | `Alt + K`, `Alt + N` | `F19 + N` |
| `ToggleInlayHintsGlobally` | Ẩn/Hiện gợi ý Inlay Hints | `Alt + K`, `Alt + I` | `F19 + I` |
| `ToggleRenderedDocAction` | Bật/Tắt chế độ render Javadoc/Docstring | `Alt + K`, `Alt + P` | `F19 + P` |

---

## 2. Search & Navigation (Tìm kiếm & Điều hướng nhanh)

| Action ID | Chức năng | Phím tắt |
| :--- | :--- | :--- |
| `SearchEverywhere` | Tìm kiếm tất cả mọi thứ (Search Everywhere) | `F19 + F` |
| `GotoDeclaration` | Đi tới định nghĩa (Go to Declaration/Definition) | `F19 + D` |
| `FindUsages` | Tìm các vị trí sử dụng (Find Usages) | `F19 + U` |

---

## 3. Workspace & Layout (Quản lý màn hình & Cửa sổ làm việc)

Nhóm này sử dụng tiền tố **`Alt + K`** hoặc phím tắt trực tiếp **`F19`**:

| Action ID | Chức năng | Phím tắt 1 | Phím tắt 2 (F19 Layer) |
| :--- | :--- | :--- | :--- |
| `ActivateProjectToolWindow` | Mở/Đóng cây thư mục dự án (Project View) | `Alt + K`, `Alt + B` | `F19 + B` |
| `ActivateTerminalToolWindow` | Mở/Đóng cửa sổ Terminal | `Alt + K`, `Alt + T` | `F19 + T` |
| `RecentFiles` | Mở danh sách các file vừa dùng (Recent Files) | `Alt + K`, `Alt + F` | `F19 + O` |
| `RecentLocations` | Mở các vị trí code vừa sửa (Recent Locations) | `Alt + K`, `Alt + E` | `F19 + E` |
| `SplitHorizontally` | Chia đôi màn hình theo chiều ngang | `Alt + K`, `Alt + H` | `F19 + H` |
| `SplitVertically` | Chia đôi màn hình theo chiều dọc | `Alt + K`, `Alt + V` | `F19 + V` |
| `UnsplitAll` | Gộp tất cả các màn hình chia nhỏ về một | `Alt + K`, `Alt + W` | `F19 + W` |
| `QuickList.FocusView` | Mở Quick List: Chế độ tập trung & Ẩn/hiện nhanh UI | `Alt + K`, `Alt + Z` | `F19 + Z` |
| `ActivateVersionControlToolWindow` | Mở tab Git/Version Control | `Alt + K`, `Alt + G` | |
| `ActivateRunToolWindow` | Mở cửa sổ Run (Kết quả chạy code) | `Alt + K`, `Alt + R` | |
| `ActivateDebugToolWindow` | Mở cửa sổ Debug | `Alt + K`, `Alt + D` | |
| `LocalHistory.ShowHistory` | Xem lịch sử sửa đổi local (Local History) | `Alt + K`, `Alt + L` | |
| `NextSplitter` | Di chuyển tiêu điểm sang khung màn hình chia tiếp theo | `Alt + K`, `Alt + O` | |
| `ViewStatusBar` | Ẩn/Hiện thanh trạng thái (Status Bar) | `Alt + K`, `Alt + S` | |

---

## 4. Git & VCS (Quản lý mã nguồn - Alt+G)

Nhóm này sử dụng tiền tố **`Alt + G`**:

| Action ID | Chức năng | Phím tắt |
| :--- | :--- | :--- |
| `Git.Commit.Stage` | Mở cửa sổ Commit/Stage thay đổi | `Alt + G`, `Alt + c` |
| `Git.Push` | Đẩy code lên remote (Git Push) | `Alt + G`, `Alt + P` |
| `Git.Pull` | Kéo code từ remote về (Git Pull) | `Alt + G`, `Alt + U` |
| `Git.Fetch` | Lấy thông tin mới từ remote (Git Fetch) | `Alt + G`, `Alt + F` |
| `Git.Branches` | Mở danh sách các nhánh (Git Branches) | `Alt + G`, `Alt + B` |
| `Vcs.Show.Log` | Xem lịch sử commit (Git Log) | `Alt + G`, `Alt + L` |
| `Compare.SameVersion` | Xem diff thay đổi của file hiện tại | `Alt + G`, `Alt + D` |
| `ChangesView.Revert` | Hoàn tác thay đổi (Rollback/Revert) | `Alt + G`, `Alt + R` |
| `Annotate` | Bật chế độ xem ai viết dòng code nào (Git Blame) | `Alt + G`, `Alt + G` |
| `QuickList.GitExtended` | Mở Quick List: Các thao tác Git nâng cao | `Alt + G`, `Alt + E` |

---

## 5. Code Folding (Đóng/Mở khối code - Alt+F)

Nhóm này sử dụng tiền tố **`Alt + F`**:

| Action ID | Chức năng | Phím tắt |
| :--- | :--- | :--- |
| `CollapseRegion` | Thu gọn khối code hiện tại | `Alt + F`, `Alt + C` |
| `ExpandRegion` | Mở rộng khối code hiện tại | `Alt + F`, `Alt + E` |
| `CollapseBlock` | Thu gọn toàn bộ khối bao ngoài | `Alt + F`, `Alt + B` |
| `ExpandCollapseToggleAction` | Bật/Tắt đóng mở nhanh khối code | `Alt + F`, `Alt + T` |
| `CollapseSelection` | Thu gọn vùng code được bôi đen | `Alt + F`, `Alt + S` |
| `CollapseAllRegions` | Thu gọn tất cả các khối code trong file | `Alt + F`, `Shift + Alt + C` |
| `ExpandAllRegions` | Mở rộng tất cả các khối code trong file | `Alt + F`, `Shift + Alt + E` |
| `FoldImports` | Thu gọn danh sách Imports | `Alt + F`, `Alt + I` |

---

## 6. Selection & Caret Helpers (Chọn vùng & Đa con trỏ - Alt+S)

Nhóm này sử dụng tiền tố **`Alt + S`**:

| Action ID | Chức năng | Phím tắt |
| :--- | :--- | :--- |
| `EditorCloneCaretAbove` | Thêm con trỏ ở dòng phía trên | `Alt + S`, `Alt + X` |
| `EditorCloneCaretBelow` | Thêm con trỏ ở dòng phía dưới | `Alt + S`, `Alt + C` |
| `EditorSelectWord` | Bôi đen từ tại con trỏ (mở rộng vùng chọn) | `Alt + S`, `Alt + W` |
| `EditorUnselectWord` | Thu nhỏ vùng bôi đen đang chọn | `Alt + S`, `Alt + D` |
| `EditorSelectSingleLineAtCaret` | Chọn nhanh toàn bộ dòng hiện tại | `Alt + S`, `Alt + L` |

---

## 7. Refactoring & Code Actions (Tái cấu trúc code - Alt+R)

Nhóm này sử dụng tiền tố **`Alt + R`** hoặc phím tắt trực tiếp **`F19`**:

| Action ID | Chức năng | Phím tắt 1 | Phím tắt 2 (F19 Layer) |
| :--- | :--- | :--- | :--- |
| `RenameElement` | Đổi tên biến/hàm/lớp (Rename) | `Alt + R`, `Alt + R` | `F19 + R` |
| `ReformatCode` | Định dạng lại code (Format) | `Alt + R`, `Alt + F` | `F19 + S` |
| `OptimizeImports` | Dọn dẹp & sắp xếp Import tối ưu | `Alt + R`, `Alt + O` | |
| `ExtractMethod` | Trích xuất đoạn code thành hàm (Extract Method) | `Alt + R`, `Alt + M` | |
| `Inline` | Gộp ngược hàm/biến về vị trí gọi (Inline) | `Alt + R`, `Alt + I` | |
| `IntroduceVariable` | Khởi tạo biến từ biểu thức chọn (Introduce Variable) | `Alt + R`, `Alt + V` | |
| `IntroduceConstant` | Khởi tạo hằng số (Introduce Constant) | `Alt + R`, `Alt + C` | |
| `IntroduceParameter` | Khởi tạo tham số cho hàm (Introduce Parameter) | `Alt + R`, `Alt + P` | |
| `Generate` | Mở menu tự động sinh code (Generate Getter/Setter...) | `Alt + R`, `Alt + G` | |

---

## 8. Running & Testing (Chạy & Chạy thử nghiệm - Alt+T)

Nhóm này sử dụng tiền tố **`Alt + T`** hoặc phím tắt trực tiếp **`F19`**:

| Action ID | Chức năng | Phím tắt 1 | Phím tắt 2 (F19 Layer) |
| :--- | :--- | :--- | :--- |
| `GotoTest` | Đi đến hoặc tạo nhanh file Test tương ứng | `Alt + T`, `Alt + G` | `F19 + G` |
| `Run` | Chạy ứng dụng hiện tại | `Alt + T`, `Alt + T` | |
| `Debug` | Gỡ lỗi ứng dụng hiện tại | `Alt + T`, `Alt + D` | |
| `RunClass` | Chạy file Class/Test hiện tại | `Alt + T`, `Alt + R` | |
| `DebugClass` | Gỡ lỗi file Class/Test hiện tại | `Alt + T`, `Alt + E` | |
| `RerunFailedTests` | Chạy lại các bài Test bị lỗi trước đó | `Alt + T`, `Alt + S` | |
| `ChooseRunConfiguration` | Mở menu lựa chọn cấu hình Run/Debug | `Alt + T`, `Alt + C` | |
