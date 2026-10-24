# 🎬 Teleprompter Pro - Ứng Dụng Máy Nhắc Chữ Trực Tuyến Hiện Đại

> Một ứng dụng Web Teleprompter mượt mà, trực quan, đầy đủ tính năng dành cho YouTuber, TikToker, Podcaster, MC, giảng viên và người thuyết trình.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## ✨ Điểm Nổi Bật

1. **Cuộn Chữ Siêu Mượt (Ultra-Smooth Scrolling)**:
   - Sử dụng `requestAnimationFrame` kết hợp thuật toán tính Delta Time và bộ tích lũy pixel phân số (Sub-pixel accumulator).
   - Tốc độ cuộn ổn định tuyệt đối trên màn hình tần số quét 60Hz, 120Hz, 144Hz, không bị giật/khựng.

2. **Giao Diện Điều Khiển Thông Minh**:
   - **Play / Pause**: Nút to trực quan, đổi màu trạng thái (Xanh lá khi sẵn sàng, Hổ phách khi đang chạy).
   - **Tốc độ (Speed)**: Tùy chỉnh linh hoạt từ 1 - 1000 với thanh trượt và phím tắt `↑`/`↓`.
   - **Cỡ chữ (Font Size)**: Từ 18px đến 96px, căn chỉnh phù hợp với mọi khoảng cách đứng/ngồi đọc.
   - **Chế độ Lật Gương (Mirror Rig)**: Hỗ trợ Flip X (Lật ngang) và Flip Y (Lật dọc) chuyên dụng cho lồng kính nhắc chữ quang học.
   - **Vạch tiêu điểm (Eye-line Reading Area)**: Dải màu mờ & mũi tên định vị đặt cố định tại vị trí 30% màn hình, giúp mắt người thuyết trình luôn nhìn thẳng vào ống kính máy quay.
   - **Đồng hồ bấm giờ (Timer)**: Theo dõi chính xác thời lượng đọc thực tế.
   - **Theme đa dạng**: Nền Tối (Dark OLED), Nền Sáng (Clean Paper), Nền Màu Kem (Sepia dịu mắt).
   - **Tự động ẩn thanh công cụ**: Thanh điều khiển sẽ tự động mờ đi khi đang đọc để không che khuất chữ.

3. **Màn Hình Soạn Thảo (Script Editor)**:
   - Tự động đếm số từ và thời lượng đọc ước tính (~140 từ/phút).
   - Tự động lưu nội dung vào `localStorage` (không lo mất kịch bản khi tắt tab hoặc f5).
   - Nút nạp kịch bản mẫu và xóa nhanh.

4. **Công Nghệ Nhận Diện Giọng Nói (Speech Recognition)**:
   - 🎙️ Tích hợp Web Speech API tiếng Việt (`vi-VN`).
   - Tự động lắng nghe và trượt tới câu bạn đang đọc.
   - Nếu ngập ngừng hoặc không có giọng nói, hệ thống tự động fallback về chế độ cuộn đều mượt mà.

---

## ⌨️ Phím Tắt Tiện Dụng (Keyboard Shortcuts)

| Phím | Chức Năng |
| :--- | :--- |
| <kbd>Space</kbd> | Bắt đầu cuộn / Tạm dừng |
| <kbd>↑</kbd> | Tăng tốc độ cuộn (+15) |
| <kbd>↓</kbd> | Giảm tốc độ cuộn (-15) |
| <kbd>←</kbd> | Tua ngược lên một đoạn |
| <kbd>→</kbd> | Tua nhanh xuống một đoạn |
| <kbd>R</kbd> | Đặt lại vị trí cuộn về đầu trang |
| <kbd>F</kbd> | Bật / Tắt chế độ Toàn màn hình (Fullscreen) |
| <kbd>Esc</kbd> | Quay về màn hình Soạn thảo kịch bản |

---

## 🚀 Hướng Dẫn Đưa Lên GitHub & GitHub Pages

Để đưa dự án lên GitHub và kích hoạt trang web chạy online miễn phí (GitHub Pages), bạn chỉ cần làm theo các bước sau:

### Cách 1: Tải lên tự động qua Git

1. Tạo một repository mới trên GitHub (ví dụ: `teleprompter-pro`).
2. Mở terminal tại thư mục dự án và chạy:

```bash
# Khởi tạo git và commit
git init
git add .
git commit -m "feat: initial commit Teleprompter Pro"

# Đổi nhánh chính sang main
git branch -M main

# Liên kết với repository của bạn trên GitHub (thay URL của bạn)
git remote add origin https://github.com/TÊN_TÀI_KHOẢN/teleprompter-pro.git

# Đẩy code lên GitHub
git push -u origin main
```

### Cách 2: Bật GitHub Pages để chạy web trực tiếp
1. Vào repository trên GitHub > bấm vào tab **Settings**.
2. Chọn mục **Pages** ở thanh menu bên trái.
3. Ở phần **Branch**, chọn `main` và thư mục `/ (root)`, sau đó nhấn **Save**.
4. Chờ khoảng 1 - 2 phút, GitHub sẽ cung cấp cho bạn một đường link web dạng:
   `https://TÊN_TÀI_KHOẢN.github.io/teleprompter-pro/`

---

## 🛠️ Công Nghệ Sử Dụng
- **HTML5 & Semantic Elements**
- **TailwindCSS (CDN)**: Giao diện hiện đại, responsive trên mobile/tablet/desktop.
- **Vanilla JavaScript (ES6+)**:
  - `requestAnimationFrame` + Timestamp Delta calculation
  - Web Speech API (`SpeechRecognition` / `webkitSpeechRecognition`)
  - Fullscreen API
  - Web Storage API (`localStorage`)
- **Fonts**: Be Vietnam Pro & Inter (Google Fonts)

