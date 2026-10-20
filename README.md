# Xưởng Truyện: viết chương truyện từ bản nháp

Web app nhận bản nháp (dàn ý, ghi chú, lời thoại thô, đoạn văn cần viết lại), gửi cho Gemini kèm bộ quy tắc trong thư mục `prompts/`, rồi trả về chương truyện hoàn chỉnh.

## Cấu trúc

| File / thư mục | Vai trò |
|---|---|
| `index.html` | Giao diện người dùng |
| `api/rewrite.js` | Hàm phía server: kiểm tra mật khẩu, gọi Gemini, trả chữ về dần |
| `prompts/SKILL.md` | Quy tắc chính |
| `prompts/references/` | Các file quy tắc tham chiếu (thoại, chiến đấu, thể chế…) |
| `prompts/templates/` | Mẫu lập kế hoạch và theo dõi tính liên tục |
| `vercel.json` | Cấu hình Vercel (thời gian chạy tối đa 300 giây, đóng gói thư mục prompts) |

## Triển khai lần đầu

### 1. Lấy API key Gemini
1. Vào https://aistudio.google.com/apikey, đăng nhập Google.
2. Bấm **Create API key** và sao chép key.
3. Không dán key vào bất kỳ file nào trong thư mục này.

### 2. Đưa code lên GitHub
1. GitHub → **New repository** → đặt tên (ví dụ `xuong-truyen`) → chọn **Private** → **Create repository**.
2. Bấm **uploading an existing file**.
3. Kéo **toàn bộ nội dung bên trong** thư mục đã giải nén vào (gồm `index.html`, `package.json`, `vercel.json`, `README.md`, và hai thư mục `api`, `prompts`). Không kéo thư mục cha, vì `index.html` phải nằm ở cấp ngoài cùng của repo.
4. Bấm **Commit changes**.

### 3. Deploy trên Vercel
1. Vercel → **Add New → Project** → chọn repo vừa tạo → **Import**.
2. Framework Preset để **Other**, không chỉnh gì thêm.
3. Mở mục **Environment Variables**, thêm:

| Key | Value |
|---|---|
| `GEMINI_API_KEY` | API key vừa lấy |
| `ACCESS_PASSWORD` | Mật khẩu bạn tự đặt để dùng web |
| `GEMINI_MODEL` | (không bắt buộc) mặc định `gemini-3.8-flash` |

4. Bấm **Deploy**.

### 4. Kiểm tra
- Mở `https://<tên-dự-án>.vercel.app/api/rewrite`. Nếu cấu hình đúng sẽ thấy `"apiKey":"đã có"`, `"password":"đã có"` và `"ruleFilesLoaded":15`.
- Mở trang chính, nhập mật khẩu, dán bản nháp, bấm **Viết chương**.

## Sửa đổi sau này

- **Sửa bộ quy tắc:** mở file trong `prompts/` trên GitHub → biểu tượng bút chì → sửa → **Commit changes**. Vercel tự deploy lại sau khoảng 30 giây. Thêm file `.md` mới vào `prompts/references/` cũng được tự động nạp.
- **Đổi mô hình / mật khẩu / API key:** Vercel → Project → **Settings → Environment Variables** → sửa → vào tab **Deployments** → bấm `⋯` ở bản mới nhất → **Redeploy**. Biến môi trường chỉ có hiệu lực sau khi redeploy.

## Lỗi thường gặp

| Hiện tượng | Nguyên nhân / cách xử lý |
|---|---|
| "Website chưa được cấu hình đủ…" | Thiếu biến môi trường, hoặc đã thêm nhưng chưa Redeploy |
| "Đã chạm giới hạn lượt dùng miễn phí" | Gói miễn phí có giới hạn số lượt theo phút/ngày. Đợi rồi thử lại, hoặc đặt `GEMINI_MODEL=gemini-3.5-flash-lite` |
| "API key không hợp lệ" | Key sai hoặc đã bị thu hồi; tạo key mới |
| "Quá thời gian xử lý" | Bản nháp quá dài; chia nhỏ theo chương |
| Trang trắng / 404 | `index.html` không nằm ở cấp ngoài cùng của repo |

## Lưu ý dữ liệu

- Gói miễn phí của Gemini API: Google có thể dùng nội dung gửi lên để cải thiện sản phẩm. Không dùng cho bản thảo cần bảo mật. Muốn tránh điều này phải bật thanh toán (gói trả phí).
- Code gửi `store: false` để Google không lưu lại phiên làm việc phục vụ tính năng hội thoại nhiều lượt; điều này không thay đổi điều khoản sử dụng dữ liệu của gói miễn phí.
- Bản nháp và mật khẩu được lưu tạm trong trình duyệt của người dùng (localStorage) để không mất khi tải lại trang.
