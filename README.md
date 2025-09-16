---

# **[NT208 - Nhóm 1] Awesome Voice Cloning for Text to Everything**

---

## 🌟 Tổng quan
**Awesome Voice Cloning** là một module được phát triển bởi Nhóm 1 (NT208.P23.ANTT) nhằm tích hợp tính năng sao chép giọng nói (voice cloning) vào web app **Text to Everything**. Dự án sử dụng mô hình **Vi-XTTS** (dựa trên TTS của ThinhLPG) để tạo giọng nói tự nhiên từ văn bản, hỗ trợ đa ngôn ngữ và tối ưu hóa cho tiếng Việt. Bản demo trực tiếp này được triển khai trên Google Colab với giao diện tương tác, cho phép người dùng thử nghiệm ngay lập tức mà không cần cấu hình API.

- **Other Colab Link**: [Demo bằng API và Ngrok trên Colab](https://colab.research.google.com/drive/11sEp_-ardFb1qm9jMgGyLyYJh73PZPmk?usp=sharing)
- **GitHub Repo**: [Repo để chạy dự án ở local](https://github.com/vobao-xD/NT208_Awesome_voice_cloning)
- **Web App Repo**: [Text to Everything](https://github.com/vobao-xD/NT208__Project__Text-to-everything)
- **Tham khảo**: [ViXTTS Demo](https://github.com/thinhlpg/vixtts-demo)

---

## 🎯 Mục tiêu
- Cung cấp công cụ sao chép giọng nói chất lượng cao cho web app **Text to Everything**.
- Hỗ trợ người dùng tạo nội dung âm thanh tùy chỉnh (TTS) với giao diện thân thiện trên Colab.
- Tối ưu hóa trải nghiệm demo trực tiếp mà không cần cấu hình server.

---

## 📋 Nội dung tài liệu
- [Hướng dẫn cài đặt](#-hướng-dẫn-cài-đặt)
- [Hướng dẫn sử dụng](#-hướng-dẫn-sử-dụng)
- [Liên hệ](#-liên-hệ)

---

## 🚀 Hướng dẫn cài đặt

### Điều kiện tiên quyết
- **Google Colab**: Tài khoản Google với quyền truy cập GPU.
- **Python**: Phiên bản 3.11 hoặc cao hơn (đã tích hợp trong Colab).
- **Thư viện cần thiết**: Sẽ được cài đặt tự động trong notebook.
- **Internet**: Kết nối ổn định để tải mô hình và phụ thuộc.

### Các bước cài đặt
1. Chọn **Runtime** > **Change runtime type** > Chọn GPU (T4 hoặc cao hơn).
2. Chạy lần lượt các cell trong notebook theo thứ tự (từ **I. Environment setup** đến các bước tiếp theo).

### Thời gian
- Cài đặt môi trường: ~5 phút.
- Lần chạy đầu sẽ hơi mất thời gian vì cần tải model, thiết lập môi trường.

---

## 🎮 Hướng dẫn sử dụng

### 1. Cài đặt môi trường
- Chạy cell **I. Environment setup** để cấu hình múi giờ Việt Nam, cài thư viện (TTS, transformers, v.v.), và tải mô hình Vi-XTTS.
- Lưu ý: Nếu gặp crash, bỏ qua và chạy lại.

### 2. Upload mẫu giọng nói
- Chạy cell **II. Upload your voice sample**.
- Upload file âm thanh (định dạng WAV, dài ~20s, to, rõ). Tham khảo file `/content/model/vi_sample.wav`.
- Tích chọn `denoise` để loại bỏ nhiễu nếu file gốc có tiếng ồn.
- Giọng sẽ được lưu ở `/content/model/user_sample.wav`

### 3. Tạo giọng nói
- Chạy cell **III. Generate speech**.
- **Cài đặt**:
  - Ngôn ngữ: Chọn từ danh sách (Tiếng Việt, Tiếng Anh, v.v.).
  - Văn bản: Nhập nội dung (tối thiểu 10 từ/câu).
  - Giọng mẫu: Chọn file mẫu (user_sample.wav hoặc các giọng mặc định).
  - Tùy chọn: Chuẩn hóa văn bản, in chi tiết, lưu từng câu riêng.
- Kết quả sẽ được lưu ở `/content/output` và phát thử ngay trên Colab.

### 4. Lưu trữ và quản lý
- **Lưu vào Google Drive**: Chạy cell **IV. Save it to Google Drive** để lưu kết quả vào `/content/drive/MyDrive/_awesome_voice_cloning`.
- **Xóa output**: Chạy cell **V. Clear generated output** để xóa file trong `/content/output`.
- **Tắt runtime**: Chạy cell **VI. Turn off runtime** để tiết kiệm tài nguyên.

### Ví dụ
- Văn bản: "Xin chào, tôi là Võ Quốc Bảo, rất vui được gặp mọi người!"
- Giọng mẫu: `/content/model/user_sample.wav` (sau khi upload).
- Kết quả: File WAV trong `/content/output` với giọng nói tự nhiên, phát thử qua Audio player.

---

## 📞 Liên hệ
- **Nhóm trưởng**: Võ Quốc Bảo  
  - Email: 23520146@gm.uit.edu.vn  
- **Thời gian**: Luôn sẵn sàng hỗ trợ

---
