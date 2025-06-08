# 🎓 DeepEssay - Hệ thống Chấm điểm Bài luận IELTS thông minh

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Flask](https://img.shields.io/badge/Flask-2.3-green)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.14-orange)
![BERT](https://img.shields.io/badge/BERT-NLP-ff6600)
![Docker](https://img.shields.io/badge/Docker-24.0-blue)
![REST](https://img.shields.io/badge/REST-API-5b68d6)

## 👤 Tác giả / Author
**Phạm Lê Ngọc Sơn**
- 📧 Email: phamlengocsonstudy@gmail.com
- 🌐 GitHub: [@phamlengocsonstudy](https://github.com/phamlengocsonstudy)

---


---

## 🎯 Giới thiệu / Introduction

**DeepEssay** là một ứng dụng web thông minh được phát triển bởi **Phạm Lê Ngọc Sơn** để tự động chấm điểm bài luận IELTS sử dụng công nghệ AI tiên tiến. Hệ thống sử dụng mô hình BERT (Bidirectional Encoder Representations from Transformers) được tinh chỉnh đặc biệt để đánh giá chất lượng bài viết theo tiêu chuẩn IELTS.

**DeepEssay** is an intelligent web application developed by **Phạm Lê Ngọc Sơn** to automatically grade IELTS essays using advanced AI technology. The system uses a fine-tuned BERT model specifically designed to evaluate writing quality according to IELTS standards.

### 🎯 Mục tiêu dự án / Project Goals
- Cung cấp công cụ chấm điểm IELTS tự động chính xác và nhanh chóng
- Hỗ trợ học viên luyện thi IELTS cải thiện kỹ năng viết
- Ứng dụng công nghệ AI trong giáo dục ngôn ngữ
- Tạo ra giải pháp tiết kiệm thời gian cho giáo viên và học sinh

---

## ✨ Tính năng / Features

### 🖊️ Chấm điểm tự động
- **Phân tích bài luận toàn diện**: Đánh giá về ngữ pháp, từ vựng, cấu trúc và nội dung
- **Dự đoán điểm số IELTS**: Cung cấp điểm số từ 0-9 theo thang điểm IELTS chính thức
- **Phản hồi tức thì**: Kết quả chấm điểm trong vài giây

### 🔍 Kiểm tra và cảnh báo
- **Validation bài viết**: Kiểm tra độ dài tối thiểu và chất lượng nội dung
- **Cảnh báo thông minh**: Thông báo khi bài viết quá ngắn hoặc không đạt yêu cầu
- **Hướng dẫn cải thiện**: Gợi ý cụ thể để nâng cao chất lượng bài viết

### 🎨 Giao diện người dùng
- **Thiết kế hiện đại**: Giao diện thân thiện, dễ sử dụng
- **Responsive design**: Tương thích với mọi thiết bị
- **Trải nghiệm mượt mà**: Tối ưu hóa hiệu suất và tốc độ

---

## 🏗️ Kiến trúc hệ thống / System Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   AI Model      │
│   (HTML/CSS/JS) │◄──►│   (Flask)       │◄──►│   (BERT)        │
└─────────────────┘    └─────────────────┘    └─────────────────┘
        │                       │                       │
        │                       │                       │
        ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Static Files  │    │   Text          │    │   TensorFlow    │
│   (Images/CSS)  │    │   Validation    │    │   Pipeline      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

---

## 🤖 Mô hình AI / AI Model

### 📊 Lựa chọn mô hình
Sau khi phân tích và so sánh các phương pháp khác nhau, tôi đã chọn 3 mô hình chính:

1. **BERT fine-tuned cho regression task**
2. **BERT kết hợp với numerical features**
3. **BERT kết hợp với numerical và binary features**

### 📈 Hiệu suất mô hình
- **Dataset**: IELTS Writing Scored Essays Dataset
- **Metric**: Mean Absolute Error (MAE)
- **Mô hình được chọn**: BERT text model (tối ưu về độ trễ thấp)

### 🔬 Đặc điểm kỹ thuật
- **Architecture**: BERT-based neural network
- **Input**: Raw text essays
- **Output**: IELTS score (0-9 scale)
- **Training**: Fine-tuned on IELTS essay dataset

---

## 🛠️ Công nghệ sử dụng / Tech Stack

### Backend
- **🐍 Python 3.11**: Ngôn ngữ lập trình chính
- **🌶️ Flask 2.3**: Web framework
- **🧠 TensorFlow 2.14**: Machine learning framework
- **🤗 Hugging Face Transformers**: Pre-trained models
- **📊 Scikit-learn**: ML utilities

### Frontend
- **🌐 HTML5**: Cấu trúc trang web
- **🎨 CSS3**: Styling và responsive design
- **⚡ JavaScript**: Tương tác động

### DevOps & Deployment
- **🐳 Docker**: Containerization
- **☁️ Microsoft Azure**: Cloud deployment
- **🔧 Git**: Version control

---

## 📁 Cấu trúc dự án / Project Structure

```
DeepEssay_IELTS_Learning/
├── 📁 app/                          # Ứng dụng chính
│   ├── 📄 main.py                   # Entry point, Flask server
│   ├── 📄 text_validation.py        # Xử lý validation bài viết
│   ├── 📄 __init__.py               # Package initialization
│   │
│   ├── 📁 ML/                       # Machine Learning components
│   │   ├── 📄 pipeline.py           # ML pipeline và preprocessing
│   │   ├── 📄 __init__.py
│   │   └── 📁 models/               # Trained models (chưa có)
│   │       ├── 📁 training_bert_text/
│   │       ├── 📁 training_bert_num/
│   │       └── 📁 training_bert_num_bin/
│   │
│   ├── 📁 templates/                # HTML templates
│   │   ├── 📄 index.html            # Trang chính
│   │   └── 📄 warning.html          # Trang cảnh báo
│   │
│   └── 📁 static/                   # Static files
│       ├── 🖼️ watercolor-backgrounds-10.jpg
│       ├── 🖼️ watercolor-backgrounds-11.jpg
│       ├── 🖼️ watercolor-backgrounds-16.jpg
│       └── 🖼️ watercolor-backgrounds-19.jpg
│
├── 📁 assets/                       # Tài nguyên dự án
├── 📄 requirements.txt              # Python dependencies
├── 📄 IELTS_Grading_with_BERT.ipynb # Jupyter notebook training
├── 📄 Dockerfile                   # Docker configuration
├── 📄 .gitignore                   # Git ignore rules
├── 📄 LICENSE                      # Giấy phép MIT
└── 📄 README.md                    # Tài liệu này
```

### 📝 Mô tả chi tiết các thành phần

#### 🎯 Core Application (`app/`)
- **`main.py`**: Khởi tạo Flask server, định nghĩa routes chính
- **`text_validation.py`**: Xử lý validation đầu vào, kiểm tra chất lượng bài viết

#### 🧠 Machine Learning (`app/ML/`)
- **`pipeline.py`**: Pipeline xử lý text, load model, prediction
- **`models/`**: Thư mục chứa trained models (cần train trước khi sử dụng)

#### 🎨 Frontend (`app/templates/`, `app/static/`)
- **`index.html`**: Giao diện chính để nhập và hiển thị kết quả
- **`warning.html`**: Trang hiển thị cảnh báo validation
- **`static/`**: Hình ảnh nền watercolor cho UI

---

## 🚀 Cài đặt và chạy / Installation & Running

### 📋 Yêu cầu hệ thống / Prerequisites
- Python 3.11+
- pip (Python package manager)
- Git
- 4GB+ RAM (cho BERT model)

### 🔧 Cài đặt / Installation

1. **Clone repository**
```bash
git clone https://github.com/phamlengocsonstudy/DeepEssay_IELTS_Learning.git
cd DeepEssay_IELTS_Learning
```

2. **Tạo virtual environment**
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
```

3. **Cài đặt dependencies**
```bash
pip install -r requirements.txt
```

4. **Train model** (quan trọng!)
```bash
# Mở và chạy notebook để train model
jupyter notebook IELTS_Grading_with_BERT.ipynb
# Sau khi train xong, model sẽ được lưu vào app/ML/models/training_bert_text/
```

5. **Chạy ứng dụng**
```bash
python app/main.py
```

6. **Truy cập ứng dụng**
```
Mở trình duyệt và truy cập: http://localhost:5000
```

### 🐳 Chạy với Docker

1. **Build Docker image**
```bash
docker build -t deepessay .
```

2. **Run container**
```bash
docker run -p 5000:5000 deepessay
```

---

## 📖 Hướng dẫn sử dụng / Usage Guide

### 🎯 Chấm điểm bài luận IELTS

1. **Truy cập trang web**: Mở http://localhost:5000
2. **Nhập bài luận**: Paste bài viết IELTS vào text area
3. **Nhấn "Grade Essay"**: Hệ thống sẽ xử lý và phân tích
4. **Xem kết quả**: Điểm số IELTS sẽ hiển thị (0-9)

### ⚠️ Lưu ý quan trọng
- Bài viết cần có độ dài tối thiểu (>50 từ)
- Nội dung phải liên quan đến chủ đề IELTS
- Hệ thống sẽ cảnh báo nếu bài viết không đạt yêu cầu

### 🔍 Validation Rules
```python
# Các quy tắc validation trong text_validation.py
- Độ dài tối thiểu: 50 từ
- Kiểm tra nội dung spam
- Validate định dạng text
- Phát hiện ngôn ngữ
```

---

## 🔧 API Documentation

### 📡 Endpoints

#### `GET /` - Trang chính
- **Mô tả**: Hiển thị form nhập bài luận
- **Response**: HTML page

#### `POST /grade` - Chấm điểm bài luận
- **Mô tả**: Nhận bài luận và trả về điểm số
- **Request Body**:
```json
{
  "essay_text": "Bài luận IELTS của bạn..."
}
```
- **Response**:
```json
{
  "score": 7.5,
  "status": "success",
  "message": "Essay graded successfully"
}
```

#### `GET /warning` - Trang cảnh báo
- **Mô tả**: Hiển thị cảnh báo validation
- **Response**: HTML page

### 🔍 Error Handling
```python
# Các trường hợp lỗi được xử lý
- Essay quá ngắn → Redirect to warning page
- Format không hợp lệ → Error message
- Model loading error → 500 Internal Server Error
```

---

## 🎯 Roadmap

### 🚀 Version 2.0 (Planned)
- [ ] **Multi-language support**: Hỗ trợ tiếng Việt
- [ ] **Detailed feedback**: Phân tích chi tiết từng tiêu chí
- [ ] **Writing suggestions**: Gợi ý cải thiện cụ thể
- [ ] **User accounts**: Lưu lịch sử bài viết

### 🔮 Future Features
- [ ] **Real-time grading**: Chấm điểm khi đang gõ
- [ ] **Plagiarism detection**: Phát hiện đạo văn
- [ ] **Speaking practice**: Mở rộng sang kỹ năng nói
- [ ] **Mobile app**: Ứng dụng di động

### 🧪 Technical Improvements
- [ ] **Model optimization**: Cải thiện độ chính xác
- [ ] **Performance tuning**: Tối ưu tốc độ
- [ ] **Unit testing**: Thêm test coverage
- [ ] **CI/CD pipeline**: Tự động hóa deployment

---

## 📄 Giấy phép / License

📜 **MIT License**

Copyright (c) 2024 **Phạm Lê Ngọc Sơn**

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 🤝 Đóng góp / Contributing

Dự án này được phát triển bởi **Phạm Lê Ngọc Sơn**. Nếu bạn muốn đóng góp:

1. Fork repository
2. Tạo feature branch
3. Commit changes
4. Push to branch
5. Tạo Pull Request

---

## 📞 Liên hệ / Contact

**Phạm Lê Ngọc Sơn**
- 📧 Email: phamlengocsonstudy@gmail.com
- 💼 LinkedIn: [Phạm Lê Ngọc Sơn](https://linkedin.com/in/phamlengocsonstudy)
- 🐙 GitHub: [@phamlengocsonstudy](https://github.com/phamlengocsonstudy)

---

## 🙏 Acknowledgments

- Cảm ơn cộng đồng Hugging Face vì các pre-trained models
- Cảm ơn Kaggle vì IELTS Writing Scored Essays Dataset
- Cảm ơn các thư viện open source: Flask, TensorFlow, BERT

---

*Được phát triển với ❤️ bởi Phạm Lê Ngọc Sơn*