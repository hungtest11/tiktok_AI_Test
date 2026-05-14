# GitHub Pages deploy plan cho TikTok Developer App URLs

## Mục tiêu
Dùng **GitHub Pages** để tạo 3 URL công khai cần cho TikTok Developer App:
- Terms of Service URL
- Privacy Policy URL
- Web/Desktop URL

## File đã được chuẩn bị sẵn
- `Tiktok/app-site/index.html`
- `Tiktok/app-site/terms.html`
- `Tiktok/app-site/privacy.html`
- `Tiktok/app-site/redirect.html`
- `Tiktok/app-site/styles.css`
- `.github/workflows/tiktok-app-site-pages.yml`
- `Tiktok/app-site/.nojekyll`

## Cách deploy
### Bước 1 - Đưa workspace này lên GitHub repo
- Tạo 1 repository GitHub
- Push toàn bộ workspace hoặc tối thiểu thư mục này lên repo

### Bước 2 - Bật GitHub Pages bằng GitHub Actions
Trong repo GitHub:
- vào **Settings**
- vào **Pages**
- ở phần **Build and deployment** chọn **Source = GitHub Actions**

### Bước 3 - Chạy workflow deploy
Có 2 cách:
- push thay đổi lên nhánh mặc định
- hoặc vào tab **Actions** và chạy workflow `Deploy TikTok app-site to GitHub Pages`

### Bước 4 - Lấy URL public
Sau khi workflow chạy xong, GitHub Pages sẽ cho 1 URL dạng ví dụ:
- `https://<github-username>.github.io/<repo-name>/`

## Mapping điền vào TikTok Developer App
Giả sử URL public là:
- `https://<github-username>.github.io/<repo-name>/`

Thì điền như sau:
- **Web/Desktop URL**
  - `https://<github-username>.github.io/<repo-name>/`
- **Terms of Service URL**
  - `https://<github-username>.github.io/<repo-name>/terms.html`
- **Privacy Policy URL**
  - `https://<github-username>.github.io/<repo-name>/privacy.html`
- **Redirect URI** nếu TikTok yêu cầu
  - `https://<github-username>.github.io/<repo-name>/redirect.html`

## Việc nên chỉnh trước khi public
- thay placeholder liên hệ trong:
  - `Tiktok/app-site/terms.html`
  - `Tiktok/app-site/privacy.html`
- kiểm tra lại tên app hiển thị trong `index.html`

## Kết luận
Đây là đường nhanh nhất để boss có URL public hợp lệ mà không phải tự dựng web phức tạp.
