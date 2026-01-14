# Hướng Dẫn Deploy Lên Vercel

## Cách 1: Deploy qua GitHub (Khuyến nghị - Dễ nhất)

1. **Đăng nhập Vercel:**
   - Truy cập: https://vercel.com
   - Đăng nhập bằng tài khoản GitHub của bạn

2. **Import Project:**
   - Click "Add New..." → "Project"
   - Chọn repository `haitu1409-crypto/quangcao`
   - Click "Import"

3. **Cấu hình Project:**
   - **Project Name**: Đặt tên là `lumi68`
   - Framework Preset: Chọn "Other" hoặc "Static Site"
   - Root Directory: `./`
   - Build Command: (Để trống vì là static HTML)
   - Output Directory: `./`

4. **Deploy:**
   - Click "Deploy"
   - Vercel sẽ tự động deploy và tạo URL: `https://lumi68.vercel.app`

5. **Auto Deploy:**
   - Mỗi lần push code lên GitHub, Vercel sẽ tự động deploy lại

## Cách 2: Deploy bằng Vercel CLI

1. **Cài đặt Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Đăng nhập:**
   ```bash
   vercel login
   ```

3. **Deploy:**
   ```bash
   vercel
   ```
   - Khi được hỏi project name, nhập: `lumi68`
   - Chọn options theo hướng dẫn

4. **Production Deploy:**
   ```bash
   vercel --prod
   ```

## Lưu ý

- Tên miền sẽ là: `https://lumi68.vercel.app`
- Nếu muốn tên khác, đổi tên project trong Vercel Dashboard
- File `vercel.json` đã được tạo để cấu hình routing








