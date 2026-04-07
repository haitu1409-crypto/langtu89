# Checklist Kiểm Tra Preview Telegram

## So Sánh 2 Dự Án

### ✅ Dự án `linkquangcaochithien` - Preview HOẠT ĐỘNG
- URL: `https://chithien188Lux.vercel.app`
- Có `"name": "chithien188Lux"` trong `vercel.json`
- Meta tags đầy đủ

### ❌ Dự án `langtu89` - Preview KHÔNG HOẠT ĐỘNG
- URL: `https://langtu89.vercel.app`
- Đã thêm `"name": "langtu89"` vào `vercel.json` ✅
- Đã thêm `og:image:url` meta tag ✅
- Meta tags đầy đủ ✅

## Các Bước Kiểm Tra

### 1. ✅ Đã Cập Nhật
- [x] Thêm `"name": "langtu89"` vào `vercel.json`
- [x] Thêm `og:image:url` meta tag
- [x] Kiểm tra tất cả meta tags đã đầy đủ

### 2. 🔍 Kiểm Tra Deploy

**Kiểm tra URL có hoạt động không:**
```bash
# Mở trình duyệt và truy cập:
https://langtu89.vercel.app
```

**Kiểm tra ảnh preview có truy cập được không:**
```bash
# Mở trình duyệt và truy cập:
https://langtu89.vercel.app/imgs/preview.jpg
```

### 3. 🔍 Kiểm Tra Meta Tags

**Sử dụng công cụ debug:**
1. **Facebook Sharing Debugger:**
   - Truy cập: https://developers.facebook.com/tools/debug/
   - Nhập URL: `https://langtu89.vercel.app`
   - Click "Debug" để xem preview
   - Click "Scrape Again" để refresh cache

2. **Open Graph Debugger:**
   - Truy cập: https://www.opengraph.xyz/
   - Nhập URL: `https://langtu89.vercel.app`
   - Xem preview

3. **LinkedIn Post Inspector:**
   - Truy cập: https://www.linkedin.com/post-inspector/
   - Nhập URL: `https://langtu89.vercel.app`
   - Xem preview

### 4. 🔍 Kiểm Tra Telegram

**Cách test trên Telegram:**
1. Đảm bảo URL đã deploy và hoạt động: `https://langtu89.vercel.app`
2. Mở Telegram (app hoặc web)
3. Gửi link `https://langtu89.vercel.app` vào một chat
4. Đợi Telegram fetch preview (có thể mất 10-30 giây)
5. Kiểm tra preview hiển thị

**Nếu preview không hiển thị:**
- Đợi 5-10 phút (Telegram cache preview)
- Thử lại với URL có query string: `https://langtu89.vercel.app?v=1`
- Clear cache Telegram (nếu có thể)

### 5. 🔍 Kiểm Tra File Preview

**Đảm bảo file `imgs/preview.jpg`:**
- [ ] File tồn tại trong thư mục `imgs/`
- [ ] Kích thước: 1200x630px (tỷ lệ 1.91:1)
- [ ] Định dạng: JPG hoặc PNG
- [ ] Kích thước file: < 1MB (tối ưu < 500KB)
- [ ] File có thể truy cập qua HTTPS: `https://langtu89.vercel.app/imgs/preview.jpg`

### 6. 🔍 So Sánh Với Dự Án Hoạt Động

**Kiểm tra dự án `linkquangcaochithien`:**
- URL: `https://chithien188Lux.vercel.app`
- Test preview trên Telegram
- So sánh meta tags

**Nếu dự án `linkquangcaochithien` hoạt động nhưng `langtu89` không:**
- Kiểm tra xem URL `langtu89.vercel.app` đã được deploy chưa
- Kiểm tra xem file preview.jpg có truy cập được không
- Kiểm tra xem có lỗi gì trong console không

## Các Vấn Đề Thường Gặp

### ❌ Vấn đề 1: URL chưa được deploy
**Giải pháp:**
- Deploy lại lên Vercel
- Đảm bảo Project Name là `langtu89`
- Kiểm tra URL hoạt động: `https://langtu89.vercel.app`

### ❌ Vấn đề 2: File preview.jpg không truy cập được
**Giải pháp:**
- Kiểm tra file có tồn tại không
- Kiểm tra đường dẫn: `imgs/preview.jpg`
- Kiểm tra file có thể truy cập qua HTTPS không

### ❌ Vấn đề 3: Telegram cache preview cũ
**Giải pháp:**
- Đợi 5-10 phút
- Sử dụng URL với query string: `?v=1`
- Clear cache Telegram

### ❌ Vấn đề 4: Meta tags không đúng
**Giải pháp:**
- Kiểm tra tất cả meta tags đã đầy đủ
- Sử dụng Facebook Sharing Debugger để kiểm tra
- Đảm bảo URL trong meta tags đúng

## Checklist Cuối Cùng

Trước khi test preview trên Telegram:

- [ ] URL `https://langtu89.vercel.app` đã được deploy và hoạt động
- [ ] File `https://langtu89.vercel.app/imgs/preview.jpg` có thể truy cập được
- [ ] Tất cả meta tags đã được cấu hình đúng
- [ ] Đã test preview bằng Facebook Sharing Debugger
- [ ] Đã test preview bằng Open Graph Debugger
- [ ] Đã đợi 5-10 phút sau khi deploy để clear cache

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

⚠️ **URL Format:**
- Đảm bảo URL không có lỗi chính tả
- Đảm bảo URL có thể truy cập được

