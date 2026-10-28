# NovaPC — Website tĩnh bán máy tính

Website bài tập bằng **HTML5 và CSS3 thuần**, gồm 4 trang với giao diện chung, đường dẫn tương đối và thiết kế đáp ứng trên máy tính, máy tính bảng, điện thoại. Không cần cài thư viện, không có JavaScript hoặc bước build.

**NovaPC là thương hiệu hư cấu.** Tên sản phẩm, cấu hình và giá là dữ liệu minh họa. Website không thực hiện mua hàng, thanh toán hoặc tư vấn thực tế.

## Cấu trúc thư mục

```text
web-ban-may-tinh/
├── index.html          # Trang chủ
├── products.html       # Bộ sưu tập, bộ lọc sản phẩm và hướng dẫn chọn máy
├── about.html          # Giới thiệu, thông tin dự án và ghi nguồn
├── contact.html        # Biểu mẫu minh họa và câu hỏi thường gặp
├── css/
│   └── style.css       # Giao diện dùng chung và responsive
├── images/
│   ├── setup.svg       # Góc máy tính ở trang chủ
│   ├── laptop.svg      # Laptop xanh bạc
│   ├── laptop-pro.svg  # Laptop xám
│   ├── desktop.svg     # Thùng máy
│   ├── workspace.svg   # Góc làm việc
│   └── favicon.svg     # Biểu tượng website
├── .nojekyll           # Đánh dấu website tĩnh cho GitHub Pages
├── .gitignore
└── README.md
```

## Nội dung từng trang

| Trang | Nội dung |
| --- | --- |
| `index.html` | Giới thiệu, nhóm nhu cầu, sản phẩm nổi bật và góc làm việc |
| `products.html` | 6 máy tính minh họa; lọc Tất cả / Laptop / PC gaming / Làm việc bằng radio và CSS |
| `about.html` | Câu chuyện thương hiệu, giá trị, phạm vi bài tập, nguồn nội dung và hình ảnh |
| `contact.html` | Biểu mẫu dùng kiểm tra HTML của trình duyệt; câu hỏi thường gặp dùng `details` / `summary` |

Mỗi trang có tiêu đề riêng, thanh điều hướng, nội dung chính và chân trang. Trang đang mở được đánh dấu trong điều hướng. Có liên kết bỏ qua điều hướng cho người dùng bàn phím, mô tả ảnh, nhãn biểu mẫu và trạng thái focus.

## Xem website trên máy

Mở `index.html` bằng trình duyệt. Tất cả trang, CSS và SVG dùng đường dẫn tương đối nên hoạt động khi mở trực tiếp hoặc đặt trong thư mục con của GitHub Pages.

Nếu có Python, cũng có thể chạy máy chủ tại thư mục dự án:

```powershell
python -m http.server 5500 --bind 127.0.0.1
```

Sau đó mở `http://127.0.0.1:5500`. Dừng máy chủ bằng `Ctrl+C`.

## Đưa mã nguồn lên GitHub

1. Đăng nhập [GitHub](https://github.com) và chọn **New repository**.
2. Đặt tên repository, ví dụ `nova-pc`. Chọn **Public** để dùng GitHub Pages miễn phí với tài khoản cá nhân thông thường. Để repository trống, không chọn tạo README, `.gitignore` hoặc license vì dự án đã có các tệp cần thiết.
3. Tại thư mục dự án, chạy các lệnh dưới đây, thay `TEN_TAI_KHOAN` và tên repository bằng thông tin của bạn:

```powershell
git add .
git commit -m "Add NovaPC static website"
git branch -M main
git remote add origin https://github.com/TEN_TAI_KHOAN/nova-pc.git
git push -u origin main
```

Nếu Git yêu cầu danh tính trước lần commit đầu tiên, đặt **tên và email của bạn** bằng `git config user.name` và `git config user.email`, rồi chạy lại lệnh commit. Nếu đã có remote `origin`, kiểm tra bằng `git remote -v` và dùng `git remote set-url origin URL_REPOSITORY_CUA_BAN` khi cần.

Bạn cũng có thể tải tệp bằng **Add file → Upload files** trên GitHub. Giữ nguyên các thư mục `css/` và `images/`, bảo đảm `index.html` nằm ngay ở gốc repository.

## Bật GitHub Pages

1. Mở repository → **Settings → Pages**.
2. Ở **Build and deployment**, chọn **Deploy from a branch**.
3. Chọn branch **main** và thư mục **/(root)**, bấm **Save**.
4. Chờ GitHub hoàn tất triển khai. Xem tiến độ trong **Actions** và lấy URL ở **Settings → Pages**.
5. Với repository `nova-pc`, URL thường có dạng `https://TEN_TAI_KHOAN.github.io/nova-pc/`. Nếu tên repository là `TEN_TAI_KHOAN.github.io`, website nằm ở tên miền gốc tương ứng.

Hướng dẫn chính thức: [Cấu hình nguồn xuất bản GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

### Kiểm tra sau khi xuất bản

- Mở URL GitHub Pages, kiểm tra trang chủ và cả 3 trang còn lại.
- Thử mọi liên kết điều hướng, nút sản phẩm và liên kết đến một phần nội dung.
- Kiểm tra ảnh, phông chữ, CSS không bị lỗi và không có lỗi 404.
- Thử bộ lọc sản phẩm, mục hỏi đáp và kiểm tra các trường bắt buộc trong biểu mẫu.
- Xem trên điện thoại hoặc chế độ responsive ở các độ rộng 375 px, 768 px và 1440 px.
- Nộp **URL repository** và **URL website GitHub Pages** theo yêu cầu của giảng viên.

## Biểu mẫu minh họa

Biểu mẫu Liên hệ không kết nối backend. Trình duyệt kiểm tra các trường bắt buộc và định dạng email, sau đó mở thông báo minh họa tại `contact.html#ban-nhap`.

Các trường cố ý không có thuộc tính `name`, nên nội dung người dùng nhập không được gửi trong truy vấn URL. Website không lưu dữ liệu bằng cookie, bộ nhớ cục bộ hoặc cơ sở dữ liệu. Trình duyệt có thể cung cấp chức năng tự điền của riêng nó.

Để dùng làm cửa hàng thật cần thay dữ liệu mẫu, thêm thông tin liên hệ thực tế và kết nối dịch vụ nhận biểu mẫu, đặt hàng, thanh toán phù hợp.

## Nguồn nội dung và hình ảnh

- Nội dung tiếng Việt được biên soạn riêng cho dự án.
- Tên thương hiệu, tên sản phẩm, cấu hình và giá là ví dụ hư cấu, không phải dữ liệu bán hàng.
- Tất cả hình minh họa trong `images/` và biểu tượng trong HTML được tự thiết kế bằng SVG. Không sử dụng hình ảnh từ website bên ngoài.
- Phông chữ là phông hệ thống: Segoe UI, Arial hoặc sans-serif của thiết bị. Không tải phông bên ngoài.
- Liên kết tài liệu GitHub ở trên là nguồn tham khảo cho hướng dẫn triển khai, không phải nguồn tài sản hình ảnh.

Thông tin ghi nguồn cũng được công khai tại `about.html#nguon`.

## Đối chiếu yêu cầu bài tập

- [x] Ít nhất 4 trang HTML; trang chủ tên `index.html`.
- [x] Mỗi trang có tiêu đề, điều hướng, nội dung chính và chân trang.
- [x] Chủ đề và giao diện thống nhất, có hình minh họa phù hợp.
- [x] Các trang liên kết với nhau; dùng đường dẫn tương đối.
- [x] HTML5, CSS3; phù hợp máy tính và điện thoại.
- [x] Tổ chức tệp rõ ràng, có ghi nguồn.
- [ ] Đưa mã nguồn lên repository GitHub của sinh viên.
- [ ] Bật GitHub Pages và kiểm tra bản xuất bản.

Hai bước cuối cần tài khoản và repository GitHub của bạn; mã nguồn chưa được xuất bản.

## Kết quả kiểm tra tại máy

- Đã kiểm tra cấu trúc của cả 4 trang, 129 đường dẫn tương đối và liên kết đến các phần nội dung; không phát hiện tệp hoặc điểm neo bị thiếu.
- Cả 6 tệp SVG phân tích cú pháp thành công.
- Đã kiểm tra cả 4 trang trong trình duyệt ở độ rộng 320, 375, 768 và 1440 px; không phát hiện tràn ngang.
- Bộ lọc hiển thị đúng 6 / 3 / 1 / 2 sản phẩm tương ứng với từng lựa chọn.
- Các trường bắt buộc và email không hợp lệ bị trình duyệt chặn. Hoàn tất biểu mẫu mở thông báo minh họa, không đưa dữ liệu nhập vào URL.
- Mục hỏi đáp mở và đóng bằng điều khiển HTML có sẵn.

Những kiểm tra này dành cho bản tại máy. Cần kiểm tra lại URL thực tế sau khi triển khai GitHub Pages.
#   t r a n g - b a n - m a y - t i n h  
 #   t r a n g - b a n - m a y - t i n h  
 