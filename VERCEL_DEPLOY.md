# 🚀 Hướng dẫn Deploy lên Vercel - cungcungpetshop

## ✅ Bước 1: Code đã được push lên GitHub
Repository: https://github.com/Thanhho1909/petshopgn.git

## 🎯 Bước 2: Deploy lên Vercel với tên "cungcungpetshop"

### Cách 1: Deploy qua Vercel Dashboard (Khuyên dùng)

1. **Truy cập Vercel:**
   - Vào [vercel.com](https://vercel.com)
   - Đăng nhập bằng GitHub account

2. **Tạo Project mới:**
   - Click nút **"Add New..."** → **"Project"**
   - Hoặc click **"New Project"**

3. **Import Repository:**
   - Tìm và chọn repository: **`Thanhho1909/petshopgn`**
   - Click **"Import"**

4. **Cấu hình Project:**
   - **Project Name:** `cungcungpetshop` (hoặc tên bạn muốn)
   - **Framework Preset:** Chọn **"Other"** hoặc để trống
   - **Root Directory:** Để trống (hoặc `./`)
   - **Build Command:** Để trống (static site)
   - **Output Directory:** Để trống
   - **Install Command:** Để trống

5. **Deploy:**
   - Click nút **"Deploy"**
   - Đợi vài giây để Vercel build và deploy

6. **Kết quả:**
   - Website sẽ có URL: `https://cungcungpetshop.vercel.app`
   - Hoặc URL tùy chỉnh nếu bạn đã set domain

### Cách 2: Deploy bằng Vercel CLI

```bash
# Cài đặt Vercel CLI (nếu chưa có)
npm i -g vercel

# Đăng nhập
vercel login

# Deploy với tên project cụ thể
vercel --name cungcungpetshop

# Deploy production
vercel --prod --name cungcungpetshop
```

## 🔧 Bước 3: Cấu hình Domain (Tùy chọn)

1. Vào Vercel Dashboard → Project **cungcungpetshop**
2. Click tab **"Settings"** → **"Domains"**
3. Thêm domain tùy chỉnh (nếu có):
   - `cungcung.pet`
   - `www.cungcung.pet`
   - Hoặc domain khác của bạn

## 📝 Bước 4: Cập nhật URL trong code (Sau khi có domain)

Sau khi có domain từ Vercel, cập nhật các URL trong `index.html`:

1. **Line 13** - Canonical URL:
```html
<link rel="canonical" href="https://cungcungpetshop.vercel.app" />
```

2. **Line 17** - Open Graph URL:
```html
<meta property="og:url" content="https://cungcungpetshop.vercel.app" />
```

3. **Line 24** - Twitter URL:
```html
<meta property="twitter:url" content="https://cungcungpetshop.vercel.app" />
```

4. **Line 2123** - Structured Data URL:
```json
"url": "https://cungcungpetshop.vercel.app"
```

Sau đó commit và push lại:
```bash
git add index.html
git commit -m "Update URLs for Vercel deployment"
git push
```

Vercel sẽ tự động redeploy khi có thay đổi trên GitHub!

## ✅ Kiểm tra sau khi deploy

- [ ] Website load được: `https://cungcungpetshop.vercel.app`
- [ ] Tất cả images hiển thị đúng
- [ ] Form contact hoạt động (demo)
- [ ] Responsive trên mobile
- [ ] SEO meta tags đúng
- [ ] Performance tốt

## 🔄 Auto Deploy

Vercel tự động deploy khi:
- Push code lên branch `main`
- Merge Pull Request
- Manual trigger từ Dashboard

## 📚 Tài liệu tham khảo

- [Vercel Documentation](https://vercel.com/docs)
- [Vercel CLI](https://vercel.com/docs/cli)
- [Custom Domains](https://vercel.com/docs/concepts/projects/domains)

---

**Chúc bạn deploy thành công! 🎉**

Website sẽ có tại: `https://cungcungpetshop.vercel.app`
