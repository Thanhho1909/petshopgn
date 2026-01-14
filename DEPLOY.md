# 🚀 Hướng dẫn Deploy lên Vercel

## Bước 1: Chuẩn bị GitHub Repository

1. Tạo repository mới trên GitHub
2. Clone repository về máy:
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

3. Copy tất cả files vào thư mục repository:
   - `index.html`
   - `vercel.json`
   - `.gitignore`
   - `README.md`
   - `package.json`

4. Commit và push lên GitHub:
```bash
git add .
git commit -m "Initial commit: Pet Shop Cung Cung landing page"
git push origin main
```

## Bước 2: Deploy lên Vercel

### Cách 1: Deploy qua Vercel Dashboard (Khuyên dùng)

1. Truy cập [vercel.com](https://vercel.com) và đăng nhập
2. Click **"New Project"**
3. Import repository từ GitHub
4. Vercel sẽ tự động detect:
   - Framework: Other
   - Build Command: (để trống)
   - Output Directory: (để trống)
5. Click **"Deploy"**
6. Đợi vài giây, website sẽ được deploy!

### Cách 2: Deploy bằng Vercel CLI

```bash
# Cài đặt Vercel CLI (nếu chưa có)
npm i -g vercel

# Đăng nhập
vercel login

# Deploy
vercel

# Deploy production
vercel --prod
```

## Bước 3: Tùy chỉnh Domain

1. Vào Vercel Dashboard → Project Settings
2. Chọn tab **"Domains"**
3. Thêm domain tùy chỉnh (nếu có)
4. Hoặc sử dụng domain mặc định: `your-project.vercel.app`

## Bước 4: Cập nhật URL trong code

Sau khi có domain, cập nhật các URL trong `index.html`:

1. **Canonical URL** (line 13):
```html
<link rel="canonical" href="https://your-domain.com" />
```

2. **Open Graph URL** (line 17):
```html
<meta property="og:url" content="https://your-domain.com" />
```

3. **Twitter URL** (line 24):
```html
<meta property="twitter:url" content="https://your-domain.com" />
```

4. **Structured Data** (line 2123):
```json
"url": "https://your-domain.com"
```

## ✅ Kiểm tra sau khi deploy

- [ ] Website load được
- [ ] Tất cả images hiển thị đúng
- [ ] Form contact hoạt động (demo)
- [ ] Responsive trên mobile
- [ ] SEO meta tags đúng
- [ ] Performance tốt (check bằng Lighthouse)

## 🔧 Troubleshooting

### Lỗi 404
- Kiểm tra `vercel.json` có đúng không
- Đảm bảo file `index.html` tồn tại

### Images không load
- Kiểm tra URL Unsplash có đúng không
- Có thể thay bằng images của bạn

### Form không gửi được
- Form hiện tại chỉ là demo
- Cần tích hợp backend để xử lý thực tế

## 📚 Tài liệu tham khảo

- [Vercel Documentation](https://vercel.com/docs)
- [Vercel CLI](https://vercel.com/docs/cli)

---

Chúc bạn deploy thành công! 🎉
