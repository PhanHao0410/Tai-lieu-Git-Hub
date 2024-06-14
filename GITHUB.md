# GIT && GITHUB

### 1.Introduction:

- Là một hệ thống kiểm soát phiên bản.
- Giúp theo dõi các thay đổi về code.
- Được sử dụng hợp tác về mã.
- Git và GitHub khác nhau.
- GitHub là nền tảng kho lưu trữ từ xa.

#### 1.1. Note: một số từ khóa cần biết trong quá trình học:

- **_repository_** : kho lưu trữ (repo).
- **_commit_** : một đơn vị làm việc: giúp theo dõi tiến trình và những thay đổi khi làm việc
- **_branch_** : nhánh.
- **_main/master_** : tên của repo chính (main repo).
- **_merge/rebase_** : kết hợp 2 nhánh.
- **_develop_** : tên của nhánh, lập trình viên.

#### 1.2. Note: một số câu lệnh hay dùng trong quá trình:

- **_git --help_** : trợ giúp, hướng dẫn.
- **_git --version_** : hiển thị thông tin phiên bản git.
- **_git status_** : hiển thị trạng thái kho lưu trữ.
- **_git log_** : hiển thị lịch sử các commit.

### 2. Các câu lệnh cơ bản quản lý file và thư mục:

- **_cd_** : change directory - thay đổi thư mục. (cd.. quay về thư mục cha).
- **_dir_** : liệt kê các tập tin, thư mục trong thư mục hiện hành. (Note: dir sử dụng trong Window, ls sử dụng tron linux, MacIOS).
- **_mkdir FolderName_** : tạo ra một thư mục mới.
- **_touch Tên file_** : tạo một file/tập tin mới.
- **_echo "Text"_** : in/xuất một nội dung.
- **_echo "text" > Ten file_** : chỉ định hướng (file) để in/xuất dữ liệu (Note: nó sẽ ghi đè lên nội dung trc đó over write).
- **_echo "text" >> Ten file_** : chỉ định hướng (file) để in/xuất dữ liệu.(Note: nó sẽ ghi vào dòng mới. new line).
- **_cat TenFile_** : hiển thị nội dung.
- **_diff file1 file2_** : so sánh khác biệt giữa 2 file.
- **_rm FileName_** : xóa một file/tập tin.
- **_rm -d FolderNam_** : xóa một thư mục rỗng.
- **_rm -r FolderName_** : xóa một thư mục có dữ liệu bên trong.

### 3. Các câu lệnh liên quan đến tạo và cấu hình Repository:

#### 3.1. Tạo repository:

- **_git init [repo name]_** : tạo ra một kho lưu trữ (repo).
- **_git clone [repo name]_** : để tạo một bản sao được liên kết với repo.
- **_git config -l_** : xem cấu hình hiện tại.
- **_git config -l [--scope] [option_name] [value]_** : trong đó scope:
  - **_--system_** : tất cả người dùng.
  - **_--global_** : liên quan đến nhiều repo(s).
  - **_--local_** : liên quan đến 1 repo.

#### 3.2. Cấu hình một repository:

- các bước để cấu hình:
  - 1. Tạo repository mới (hoặc vào repo có sẵn).
  - 2. Xem cấu hình. **_`git config -l`_**
  - 3. Xem cấu hình global. **_`git config -l --global`_**.
  - 4. Xem cấu hình local. **_`git config -l --local`_**
  - 5. Cấu hình global như 'user.name' và user.email':
       **_`git config --global user.name "Phan Thanh Hao"`_**
       **_`git config --global user.email "phanthanhhao3010@gmail.com"`_**.
  - 6. Lập lại bước 5, nhưng cấu hình local.

### 4. Thực hành: git add | git commit | git status | git diff.

- **_git add [File Name(s)]_** : thêm tệp vào index.
- **_git add ._** : thêm tệp (tất cả).
- **_git commit -m "nội dung"_** : tạo commit ->repo
- **_git status_** : sự khác biệt giữa 3 cây
- **_git diff_** : so sánh với commit cuối cùng.
- **_git log_** : để lịch sử.

### 5. GITIGNORE:

- Khi chia sẻ code, thường có những tệp hoặc phần trong dự án mà không muốn chia sẻ, có thể chỉ định những tệp hoặc phần nào trong dự án sẽ bị Git bỏ qua bằng cách sử dụng tệp .gitignore.
- syntax: **_`.gitignore`_**.

### 6. Tương tác với Remote Repository:

- **_git init --bare_** : tạo một central repo.
- **_git clone [repo.name] [clone.name]_** : sao chép và liên kết repo.name
- **_git fetch_** : lấy các thông tin commit mới từ central.
- **_git pull_** : lấy dữ liệu từ central về local repo.
- **_git push_** : đẩy các commit từ local về central.

### 7. Git checkout - chuyển đổi giữa các commit trong git:

- **_git checkout codecommit_** : chuyển đổi giữa các commit trong git.

### 8. Git branches - làm việc với nhiều nhánh và git merge - hợp nội dung từ các nhánh.

#### 8.1. Git Branches:

- **_`branch`_** là phiên bản mới riêng biệt của kho lưu trữ.
- Các branch cho phép làm việc trên các phần khác nhau của dự án mà không ảnh hưởng đến nhánh chính.
- **_git branch <branchname>_** : tạo nhánh
- **_git checkout <branchname>_** : chuyển nhánh
- **_git branch -l_** : xem nhánh hiện tại và xem danh sách các nhánh.

#### 8.2. Merge branch:

- dùng để hợp nhất các nhánh vào với nhau

**_git merge_** : hợp nhất các nhánh

#### 8.3. Git rebase - tái cơ sở cho một nhánh trong Git:

- **_git rebase <tên nhánh>_** : tái cơ sở lại cho nhánh.
- **_git rebase --continue_** : tiếp tục áp dụng những thay đổi rebase.
- **_git rebase --skip_** : bỏ qua những thay đổi.

#### 8.4. xóa một branch - nhánh:

- **_git branch -d <branchName>_** : xóa nhánh trên local
- **_git push origin -d <branchName>_** : xóa nhánh trên remote repository.

### 9. Git reset - hủy bỏ commit và Git revert - quay lại các commit trước đây.

#### 9.1. Git reset:

- **_git reset --soft <commit id>_** : di chuyển HEAD về vị trí commit reset. Trạng thái của stage và tất cả sự thay đổi của file được giữ nguyên.
- **_git reset <commit id>_** : di chuyển HEAD về vị trí commit reset, vẫn giữ tất cả thay đổi của file, nhưng loại bỏ các thay đổi stage (--mixed).
- **_git reset --hard <commit id>_** : di chuyển con trỏ HEAD về vị trí commit reset và loại bỏ tất cả sự thay đổi của file, stage.

#### 9.2. Git revert:

- **_git revert <commit id>_** : quay lại trạng thái code nào đó khi muốn quay lại thông qua commit

### 10. GITHUB:

#### 10.1. Đẩy một dự án lên git:

- thao tác tạo các file, add và commit
- **_git remote add origin <linkrepository trên github>_** : tạo liên kết với repository trên github
- **_git branch -M <branch name>_** : đổi tên nhánh
- **_git push -u origin main_** : đẩy dữ liệu dự án lên github

#### 10.2. Git fork.

- Ta sẽ fork một repo hay một dự án của ng khác về github của mk.
- sau đó ta sẽ clone về sử dụng.
