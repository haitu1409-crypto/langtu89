# Hướng Dẫn Test Preview Trên Telegram

## Các Meta Tags Đã Được Cấu Hình

Trang web đã được cấu hình đầy đủ các meta tags cho Telegram:

### Open Graph Tags (Telegram sử dụng)
- ✅ `og:title` - Tiêu đề preview
- ✅ `og:description` - Mô tả preview  
- ✅ `og:image` - Hình ảnh preview (1200x630px)
- ✅ `og:url` - URL trang web
- ✅ `og:type` - Loại nội dung (website)
- ✅ `og:site_name` - Tên site

### Các Tags Bổ Sung
- ✅ `og:image:width` và `og:image:height` - Kích thước ảnh
- ✅ `og:image:type` - Loại file ảnh
- ✅ `og:locale` - Ngôn ngữ (vi_VN)

## Cách Test Preview

### Bước 1: Deploy Lên Vercel
1. Đăng nhập vào [Vercel Dashboard](https://vercel.com)
2. Import project từ GitHub: `haitu1409-crypto/langtu89`
3. Đặt Project Name: `langtu89`
4. Deploy và đợi URL: `https://langtu89.vercel.app`

### Bước 2: Test Preview Trên Telegram

**Cách 1: Test Trực Tiếp**
1. Mở Telegram (app hoặc web)
2. Gửi link `https://langtu89.vercel.app` vào một chat
3. Đợi Telegram fetch preview (có thể mất vài giây)
4. Kiểm tra preview hiển thị:
   - ✅ Tiêu đề: "Trang Đăng Ký - Tham Gia Ngay Để Nhận Ưu Đãi Đặc Biệt"
   - ✅ Mô tả: "Tham gia ngay để nhận những ưu đãi đặc biệt. Đăng ký ngay hôm nay!"
   - ✅ Hình ảnh: `imgs/preview.jpg` (1200x630px)
   - ✅ URL: `https://langtu89.vercel.app/`

**Cách 2: Test Bằng Công Cụ Online**
1. Sử dụng [Telegram Bot Preview Tester](https://tg.i-c-a.su/) (nếu có)
2. Hoặc sử dụng [Open Graph Debugger](https://www.opengraph.xyz/)
3. Nhập URL: `https://langtu89.vercel.app`
4. Xem preview

**Cách 3: Test Bằng Telegram Bot**
1. Gửi link cho bot @WebpageBot trên Telegram
2. Bot sẽ trả về preview card

### Bước 3: Kiểm Tra Preview Image

Đảm bảo file `imgs/preview.jpg`:
- ✅ Tồn tại và có thể truy cập: `https://langtu89.vercel.app/imgs/preview.jpg`
- ✅ Kích thước khuyến nghị: 1200x630px (tỷ lệ 1.91:1)
- ✅ Định dạng: JPG hoặc PNG
- ✅ Kích thước file: < 1MB (tối ưu < 500KB)

### Bước 4: Xử Lý Nếu Preview Không Hiển Thị

Nếu preview không hiển thị trên Telegram:

1. **Kiểm tra URL có truy cập được không:**
   ```bash
   curl -I https://langtu89.vercel.app
   ```

2. **Kiểm tra ảnh preview có truy cập được không:**
   ```bash
   curl -I https://langtu89.vercel.app/imgs/preview.jpg
   ```

3. **Clear Telegram Cache:**
   - Telegram có thể cache preview cũ
   - Đợi 5-10 phút hoặc sử dụng URL với query string: `?v=1`

4. **Kiểm tra Meta Tags:**
   - Sử dụng [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)
   - Hoặc [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/)

## Lưu Ý Quan Trọng

⚠️ **Telegram Cache:**
- Telegram cache preview trong vài phút đến vài giờ
- Nếu thay đổi preview, có thể cần đợi hoặc thêm query string vào URL

⚠️ **HTTPS Required:**
- Telegram yêu cầu HTTPS cho preview images
- Vercel tự động cung cấp HTTPS

⚠️ **Image Size:**
- Ảnh quá lớn (>1MB) có thể không load
- Nên optimize ảnh preview trước khi upload

## Checklist Trước Khi Test

- [ ] Đã deploy lên Vercel
- [ ] URL truy cập được: `https://langtu89.vercel.app`
- [ ] Ảnh preview truy cập được: `https://langtu89.vercel.app/imgs/preview.jpg`
- [ ] Meta tags đã được cấu hình đúng trong `index.html`
- [ ] Ảnh preview có kích thước phù hợp (1200x630px)

