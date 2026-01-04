Attentdant - AI Object Check-in System
Hệ thống điểm danh thông minh sử dụng AI nhận diện vật thể để xác thực sự hiện diện và tự động đóng dấu Watermark lên hình ảnh báo cáo.

🚀 Công nghệ sử dụng
Frontend: React.js (Hooks, Axios, Lucide Icons)

Backend: FastAPI (Python), Uvicorn

Computer Vision: OpenCV (ORB Algorithm), NumPy

Tools: Git, VS Code

✨ Tính năng cốt lõi
Object Recognition: Nhận diện vật thể đặc trưng qua camera để thay thế điểm danh GPS truyền thống.

Smart Watermarking: Tự động chèn Thời gian, Tên vật thể và ID xác thực trực tiếp vào pixel ảnh để chống gian lận.

Real-time Processing: Xử lý ảnh không đồng bộ với FastAPI giúp phản hồi kết quả gần như ngay lập tức.

Responsive Design: Giao diện thân thiện trên cả điện thoại và máy tính.

🛠 Hướng dẫn cài đặt
1. Cài đặt Backend
Bash

cd backend
python -m venv venv
source venv/bin/scripts/activate  # Trên Windows dùng: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
2. Cài đặt Frontend
Bash

cd frontend
npm install
npm start
🧠 Cơ chế hoạt động (AI Logic)
Hệ thống sử dụng thuật toán ORB (Oriented FAST and Rotated BRIEF) để trích xuất các điểm đặc trưng của vật thể:

Bước 1: Người dùng chụp ảnh qua giao diện React.

Bước 2: FastAPI nhận ảnh, chuyển về ảnh xám (Grayscale) và resize về 1024px.

Bước 3: Gọi hàm orb.detectAndCompute(gray, None) để lấy descriptors.

Bước 4: So khớp với dữ liệu mẫu. Nếu tỷ lệ khớp > 70%, tiến hành đóng dấu Watermark và lưu trữ.
