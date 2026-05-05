# HocTot.vn - Nền tảng học tập thông minh

Đây là một nền tảng học tập toàn diện sử dụng AI Gemini để giúp học sinh học tập nhanh hơn và hiểu bài sâu hơn.

## 🎯 Tính năng chính

1. **Giới thiệu** - Thông tin về nền tảng
2. **Tạo tài khoản** - Đăng ký/Đăng nhập
3. **Bài học tập** - 9 môn học với AI test tương tác
4. **Quản lý tài khoản** - Cập nhật thông tin cá nhân
5. **Dev AI Gia sư** - Chat với AI Gemini
6. **Bảng xếp hạng** - So sánh kết quả với người dùng khác
7. **Báo cáo lỗi & Góp ý** - Gửi feedback
8. **Admin Dashboard** - Quản lý hệ thống (chỉ admin)

## 🛠️ Tech Stack

- **Backend**: Django + Django REST Framework
- **Database**: MongoDB
- **AI Integration**: Google Gemini API
- **Frontend**: HTML5, CSS3, JavaScript
- **Authentication**: JWT Token

## 📋 Cài đặt

### Yêu cầu
- Python 3.8+
- MongoDB
- pip

### Bước 1: Clone repository
\`\`\`bash
git clone https://github.com/kietphantuan200-wq/HocTot.vn.git
cd HocTot.vn
\`\`\`

### Bước 2: Tạo virtual environment
\`\`\`bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\\Scripts\\activate     # Windows
\`\`\`

### Bước 3: Cài đặt dependencies
\`\`\`bash
pip install -r requirements.txt
\`\`\`

### Bước 4: Cấu hình MongoDB
Cập nhật `settings.py` với connection string MongoDB của bạn

### Bước 5: Chạy server
\`\`\`bash
python manage.py runserver
\`\`\`

Server sẽ chạy tại `http://localhost:8000`

## 📁 Cấu trúc thư mục

```
HocTot.vn/
├── manage.py
├── requirements.txt
├── config/                 # Django settings
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── apps/
│   ├── users/             # Quản lý user
│   ├── lessons/           # Bài học & test
│   ├── ai_tutor/          # Dev AI Gia sư
│   ├── ranking/           # Bảng xếp hạng
│   ├── feedback/          # Báo cáo & góp ý
│   └── admin_dashboard/   # Admin panel
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── templates/
│   ├── index.html
│   ├── auth/
│   ├── lessons/
│   ├── dashboard/
│   └── admin/
└── media/                 # Lưu ảnh tạm
```

## 🔑 API Endpoints

### Users
- `POST /api/auth/register/` - Đăng ký
- `POST /api/auth/login/` - Đăng nhập
- `POST /api/auth/verify-password/` - Xác thực mật khẩu
- `GET /api/users/profile/` - Lấy thông tin tài khoản
- `PUT /api/users/profile/` - Cập nhật thông tin
- `PUT /api/users/avatar/` - Cập nhật avatar
- `PUT /api/users/change-password/` - Đổi mật khẩu

### Lessons
- `GET /api/lessons/` - Lấy danh sách bài học
- `POST /api/lessons/upload-images/` - Upload ảnh đề
- `POST /api/lessons/generate-test/` - Tạo bài test từ ảnh
- `POST /api/lessons/submit-test/` - Nộp bài test
- `GET /api/lessons/results/` - Lấy kết quả bài test

### AI Tutor
- `POST /api/ai/chat/` - Chat với Dev AI
- `GET /api/ai/chat-history/` - Lịch sử chat
- `POST /api/ai/copy-answer/` - Copy câu trả lời

### Ranking
- `GET /api/ranking/` - Lấy bảng xếp hạng
- `GET /api/ranking/my-rank/` - Xem hạng cá nhân

### Admin
- `GET /api/admin/dashboard/` - Dashboard thống kê
- `GET /api/admin/users/` - Quản lý tài khoản
- `GET /api/admin/feedback/` - Xem góp ý & báo cáo

## 🔐 Bảo mật

- Mật khẩu được hash bằng bcrypt
- JWT Token cho authentication
- Rate limiting cho API
- CORS configuration

## 📝 Góp ý & Báo cáo

- Góp ý được lưu để cải thiện nền tảng
- Báo cáo lỗi được track và xử lý ưu tiên
- Admin có thể phản hồi trực tiếp

## 👨‍💼 Tác giả

**Phan Tuấn Kiệt** - Admin & Creator

## 📞 Liên hệ

- Email: kietphantuan200@example.com
- GitHub: [@kietphantuan200-wq](https://github.com/kietphantuan200-wq)

---

**Phiên bản**: 1.0.0 | **Cập nhật**: 05/05/2026
