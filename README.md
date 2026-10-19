# 🎧 SmartSound - Ứng dụng Nghe Âm Thanh Máy Tính & Dịch sang Text

Ứng dụng Python chuyên dụng để **bắt trực tiếp âm thanh đang phát ra từ máy tính** (Youtube, video bài giảng, cuộc họp trực tuyến, phim ảnh, podcast...) hoặc từ **Microphone**, sau đó tự động **nhận diện giọng nói thành văn bản (Speech-to-Text)** và **dịch song ngữ** giữa **Tiếng Anh và Tiếng Việt**.

---

## 🌟 Tính năng nổi bật

1. **Nghe trực tiếp âm thanh từ máy tính (System Audio Loopback)**:
   - Sử dụng công nghệ WASAPI Loopback giúp bắt chính xác 100% âm thanh phát ra từ trình duyệt web, phần mềm xem video, nhạc mà không cần cắm dây kết nối phụ.
   - Hỗ trợ chuyển đổi linh hoạt giữa âm thanh máy tính (loa) và Microphone.

2. **Dịch thuật song ngữ Tiếng Anh ↔ Tiếng Việt**:
   - 🇬🇧 **Tiếng Anh ➔ 🇻🇳 Tiếng Việt**: Nghe video/tiếng Anh trên máy tính và tự động hiển thị bản dịch tiếng Việt ngay tức thì.
   - 🇻🇳 **Tiếng Việt ➔ 🇬🇧 Tiếng Anh**: Nghe âm thanh tiếng Việt và dịch sang tiếng Anh.
   - 🇬🇧 / 🇻🇳 **Chế độ chỉ nhận diện (STT)**: Chép lời nguyên bản mà không cần dịch.

3. **Giao diện trực quan & Hiện đại (PyQt6)** chia làm 2 phần rõ ràng:
   - **Phần 1: Hiển thị văn bản**:
     - Cột trái: Văn bản gốc nhận diện được kèm mốc thời gian `[HH:MM:SS]`.
     - Cột phải: Bản dịch tương ứng tương ứng theo từng câu.
     - Thanh đo mức sóng âm lượng thời gian thực (VU Meter).
     - Nút sao chép (Copy) riêng biệt cho từng cột.
   - **Phần 2: Nút điều khiển chức năng**:
     - Nút **Bắt đầu nghe / Dừng nghe** nổi bật.
     - Danh sách chọn nguồn âm thanh (Loa máy tính / Mic).
     - Danh sách chọn chế độ dịch.
     - Thanh trượt căn chỉnh độ nhạy âm thanh.
     - Nút **Xóa toàn bộ** và **Lưu kết quả ra file .txt**.

---

## 🚀 Cách khởi động ứng dụng

Môi trường Python Anaconda của bạn đã được cấu hình tại: `D:\anaconda3`.

### Cách 1: Nhấp đúp chuột (Khuyên dùng)
- Nhấp đúp vào file **`run.bat`** trong thư mục `e:\A\SmartSound`.

### Cách 2: Chạy bằng Terminal / PowerShell
Mở PowerShell tại thư mục `e:\A\SmartSound` và gõ:
```powershell
D:\anaconda3\python.exe main.py
```

---

## 📖 Hướng dẫn sử dụng

1. **Chọn nguồn âm thanh**:
   - Để nghe âm thanh đang mở trên máy tính (Youtube, video, phim...): Chọn `🔊 [Âm thanh máy tính] Speakers ... (Mặc định)`.
   - Để nói trực tiếp qua micro: Chọn `🎤 [Microphone] ...`.

2. **Chọn chế độ dịch**:
   - Chọn `🇬🇧 Tiếng Anh ➔ 🇻🇳 Tiếng Việt` (mặc định) nếu bạn muốn xem video tiếng Anh và nhận bản dịch tiếng Việt.

3. **Bắt đầu**:
   - Nhấn nút **`▶ BẮT ĐẦU NGHE`**.
   - Bật video, âm thanh trên máy tính của bạn.
   - Quan sát thanh sóng âm lượng nhảy theo điệu nhạc/lời nói.
   - Khi hết câu nói, phần mềm sẽ tự động nhận diện và dịch hiển thị lên màn hình.

4. **Sao chép hoặc Lưu**:
   - Nhấn **`📋 Sao chép`** để copy văn bản vào clipboard.
   - Nhấn **`💾 Lưu file (.txt)`** để xuất toàn bộ nội dung ra file text lưu trữ.

---

## 📁 Cấu trúc dự án

- **`main.py`**: Mã nguồn giao diện chính PyQt6.
- **`audio_engine.py`**: Bộ máy xử lý ghi âm loopback âm thanh máy tính và nhận dạng giọng nói.
- **`translator.py`**: Bộ xử lý dịch văn bản Anh ↔ Việt tốc độ cao.
- **`run.bat`**: File chạy nhanh ứng dụng bằng Anaconda.
- **`requirements.txt`**: Danh sách thư viện Python.
