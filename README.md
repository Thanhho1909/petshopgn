# Pet Shop Cung Cung 🐾

Website bán combo sản phẩm cho thú cưng - Landing page hiện đại, responsive và tối ưu SEO.

## ✨ Tính năng

- 🎨 **UI/UX hiện đại**: Thiết kế đẹp mắt với màu sắc pastel, animations mượt mà
- 📱 **Responsive**: Hoạt động tốt trên mọi thiết bị (mobile, tablet, desktop)
- ⚡ **Performance**: Tối ưu tốc độ tải trang, lazy loading images
- ♿ **Accessibility**: Hỗ trợ đầy đủ cho screen readers và keyboard navigation
- 🔍 **SEO**: Meta tags, structured data, semantic HTML
- 🎯 **Interactive**: Slider, filters, FAQ accordion, contact form

## 🚀 Deploy lên Vercel

### Cách 1: Deploy trực tiếp từ GitHub

1. Push code lên GitHub repository
2. Vào [Vercel](https://vercel.com) và đăng nhập
3. Click "New Project" và import repository từ GitHub
4. Vercel sẽ tự động detect và deploy

### Cách 2: Deploy bằng Vercel CLI

```bash
# Cài đặt Vercel CLI
npm i -g vercel

# Deploy
vercel

# Deploy production
vercel --prod
```

## 📁 Cấu trúc dự án

```
.
├── index.html        # File HTML chính (self-contained)
├── vercel.json       # Cấu hình Vercel
├── .gitignore        # Git ignore rules
└── README.md         # Tài liệu dự án
```

## 🛠️ Tùy chỉnh

### Thay đổi domain/URL

Sửa các URL trong file `index.html`:
- Line 13: `canonical` URL
- Line 17: `og:url`
- Line 24: `twitter:url`
- Line 2123: `url` trong structured data

### Thay đổi thông tin liên hệ

Sửa các thông tin trong file `index.html`:
- Line 2131: `telephone`
- Line 2132: `email`
- Line 3205: Email trong contact section
- Line 3209: Hotline trong contact section

### Thay đổi màu sắc

Sửa CSS variables trong `<style>` tag (line 33-57):
```css
:root {
  --brand: #f1e9b9;
  --pink: #ffb3d1;
  --orange: #ffc8a3;
  /* ... */
}
```

## 📝 Lưu ý

- File `index.html` là self-contained (chứa tất cả CSS và JS inline)
- Tất cả images sử dụng Unsplash (có thể thay bằng images của bạn)
- Form contact hiện tại chỉ là demo (cần tích hợp backend để xử lý thực tế)
- Các link Terms/Privacy là placeholder (cần thay bằng nội dung thật)

## 🔒 Security

File `vercel.json` đã được cấu hình với các security headers:
- X-Content-Type-Options
- X-Frame-Options
- X-XSS-Protection
- Referrer-Policy
- Permissions-Policy

## 📊 Performance

- Lazy loading cho images
- Intersection Observer cho animations
- Debounced scroll events
- Optimized CSS và JavaScript
- Preload critical resources

## 🌐 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

Tự do sử dụng cho dự án của bạn.

## 🤝 Đóng góp

Mọi đóng góp đều được chào đón! Vui lòng tạo issue hoặc pull request.

---

Made with ❤️ for pet lovers 🐾
