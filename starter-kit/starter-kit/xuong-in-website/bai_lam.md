# BÀI LÀM – HACKATHON 02

- **Mã đề:** 06
- **Họ tên:*Nguyễn Thuận Phát*
- **Lớp:*CNTT3*
- **Link repository:*https://github.com/pnguyenthuan5-netizen/HN-K26-CNTT3_Nhap-mon-CNTT_Hackathon02*
- **Hệ điều hành (Windows/macOS):*Windows*

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\yeu_cau_khach_hang.txt .\docs\
mkdir backup
cp .\data\don_in_thang_6.xlsx .\backup\
rm -r *.tmp
cd .\logs\
Get-ChildItem
cd..


```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\xuong-in-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026  10:55 AM                backup
d-----        11/11/2026  10:50 AM                data
d-----        11/11/2026  10:54 AM                docs
d-----        11/11/2026  10:47 AM                evidence
d-----        11/11/2026  10:50 AM                logs
d-----        11/11/2026  10:44 AM                web
------         11/3/2026   7:07 AM             76 .env
-a----        11/11/2026  10:55 AM           2517 bai_lam.md


    Directory: C:\Users\admin\Downloads\starter-kit\starter-kit\xuong-in-we
    bsite\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM           6137 don_in_thang_6.xlsx


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\xuong-in-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM           6137 don_in_thang_6.xlsx


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\xuong-in-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM            153 yeu_cau_khach_hang.txt


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\xuong-in-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM            981 order.log


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\xuong-in-website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026  10:44 AM                images
------         11/3/2026   7:07 AM            594 app.js
------         11/3/2026   7:07 AM            516 index.html
------         11/3/2026   7:07 AM            460 style.css


    Directory: C:\Users\admin\Downloads\starter-kit\starter-kit\xuong-in-we
    bsite\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
------         11/3/2026   7:07 AM           3092 logo-printnow.png

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
 cat .\logs\order.log | Select-String "status=500" > .\logs\loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
2026-06-28 08:15:01 POST /api/thanh-toan status=500
2026-06-28 08:34:07 POST /api/tai-file status=500


```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
(cat .\logs\order.log | Select-String "status=500").count

```

```text
6

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
Dang tao bao cao...
Hoan thanh!

```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |Network  | logo.jpg  | Sửa lại đường dẫn tên file |
| 2 | Console |ERR_FILE_NOT_FOUND, hienThiSanPham is not defined  | Sửa lại đường dẫn tên file |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:*Lỗi logo không hiển thị bảng giá không hiển thị* 
- **Expected:*Web không thông báo lỗi* 
- **Actual:*Web chưa được sửa cần sửa lại* 
- **Log:*ERR_FILE_NOT_FOUND, hienThiSanPhan is not defined* 

### Câu tìm kiếm Google

```text
site:stackoverflow.com "ERR_FILE_NOT_FOUND"

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_in_thang_6.xlsx`, không cần ghi vào đây.
