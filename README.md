# 🎓 NLP-Powered College Information Chatbot

A sophisticated AI chatbot built with Natural Language Processing (NLP) to provide instant answers to college-related queries. Features advanced intent detection, fuzzy matching, and a dynamic admin panel for content management.

## 🌐 Overview

This intelligent chatbot serves students, parents, and visitors by answering questions about college admissions, fees, scholarships, hostels, placements, and more. It combines rule-based NLP with machine learning techniques for accurate and helpful responses.

## ✨ Key Features

### 🤖 Advanced NLP Capabilities
- **Intent Detection**: Recognizes greetings, help requests, and farewells using SpaCy token analysis
- **Keyword Extraction**: Identifies relevant topics from user queries
- **Fuzzy Matching**: Finds similar questions using approximate string matching
- **Real-time Responses**: Includes dynamic features like current time/date queries

### 🔧 Dynamic Knowledge Base
- **JSON-based Storage**: Flexible and easily maintainable Q&A database
- **Admin Panel**: Full CRUD operations for Q&A management
- **Search & Filter**: Real-time search through existing Q&A pairs
- **Export Functionality**: Download knowledge base as JSON

### 🔒 Security & Privacy
- **Hashed Passwords**: Secure authentication using Werkzeug security
- **Environment Variables**: Protected API keys and secrets
- **Two-Factor Admin Access**: Additional password confirmation for admin panel
- **Session Management**: Secure user sessions with automatic logout

### 🎨 Modern User Interface
- **Responsive Design**: Works on desktop and mobile devices
- **Bootstrap Framework**: Professional styling with animations
- **Voice Input**: Speech-to-text functionality for accessibility
- **Dark Mode**: Toggle between light and dark themes
- **Interactive Elements**: Hover effects and smooth transitions

### 📊 Admin Dashboard
- **Q&A Management**: Add, edit, delete, and search Q&A pairs
- **Statistics Display**: Real-time count of knowledge base entries
- **Quick Actions**: Export data and refresh functionality
- **Modal Editing**: User-friendly edit interface

## 🛠️ Technologies Used

- **Backend**: Flask (Python web framework)
- **NLP Engine**: SpaCy with en_core_web_sm model
- **String Matching**: FuzzyWuzzy library
- **Authentication**: Werkzeug security utilities
- **Environment Management**: python-dotenv
- **Frontend**: HTML5, CSS3, Bootstrap 5, JavaScript
- **Icons**: Font Awesome
- **Data Storage**: JSON files

## 🚀 Installation & Setup

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Step-by-Step Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Abhishek-sandhu/Ai-Chatbot-for-college-queries.git
   cd Ai-Chatbot-for-college-queries
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download SpaCy model**
   ```bash
   python -m spacy download en_core_web_sm
   ```

4. **Configure environment variables**
   Create a `.env` file in the root directory:
   ```env
   SECRET_KEY=your_super_secret_key_here
   HF_API_KEY=your_huggingface_api_key_here
   ```

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Access the chatbot**
   Open your browser and navigate to: `http://localhost:5000`

## 🔐 User Accounts

### Default Admin Account
- **Username**: admin
- **Password**: admin123 (change this in production!)

### Creating User Accounts
1. Visit the login page
2. Click on registration link
3. Create a new account

## 📁 Project Structure

```
NLP-Powered-Chatbot-for-College-Information/
│
├── app.py                      # Main Flask application with routes and logic
├── knowledge_base.py           # Intent keywords and predefined responses
├── requirements.txt            # Python dependencies
├── users.json                  # Hashed user credentials
├── knowledge_base.json         # Dynamic Q&A knowledge base
├── chat_history.json           # Chat conversation history
│
├── data/
│   └── college_qa_dataset.csv  # Legacy CSV (no longer used)
│
├── static/
│   ├── styles.css              # Custom CSS styles
│   └── student_image.png       # Chat interface avatar
│
├── templates/
│   ├── index.html              # Main chat interface
│   ├── login.html              # User authentication
│   ├── admin_confirm.html      # Admin access confirmation
│   ├── admin.html              # Admin panel interface
│   └── history.html            # Chat history viewer
│
├── en_core_web_sm/             # SpaCy language model
└── __pycache__/                # Python bytecode cache
```

## 💬 How It Works

### Query Processing Pipeline

1. **User Input**: Question is received via web interface or voice input
2. **Preprocessing**: Text is tokenized and analyzed using SpaCy
3. **Intent Detection**: Keywords are matched against predefined intent categories
4. **Knowledge Base Search**: Direct lookup in JSON knowledge base
5. **Fuzzy Matching**: Approximate matching for similar questions
6. **Fallback Response**: HuggingFace API integration for unmatched queries
7. **Response Generation**: Formatted answer returned to user

### Example Interactions

**User**: "How can I apply for admission?"
**Bot**: "To apply for admission, visit our official website and fill out the online application form..."

**User**: "What time is it?"
**Bot**: "The current time is 14:30:25."

**User**: "Tell me about placements"
**Bot**: "Our placement cell has achieved 95% placement rate with average package of 6 LPA..."

## ⚙️ Admin Panel Features

### Access Requirements
- Must be logged in as admin user
- Additional password confirmation required
- Session-based access control

### Available Operations
- **Add Q&A**: Create new question-answer pairs
- **Edit Q&A**: Modify existing entries with modal interface
- **Delete Q&A**: Remove unwanted entries with confirmation
- **Search**: Real-time filtering of knowledge base
- **Export**: Download complete knowledge base as JSON
- **Statistics**: View total number of Q&A pairs

## 🔒 Security Measures

- **Password Hashing**: All passwords stored as secure hashes
- **Session Security**: Flask session management with secret keys
- **Input Validation**: Length limits and sanitization
- **Environment Protection**: Sensitive data in .env files
- **Access Control**: Role-based permissions for admin features

## 🎯 Future Enhancements

- [ ] Multi-language support
- [ ] Advanced ML models for better intent detection
- [ ] Integration with college database
- [ ] Voice response capability
- [ ] Analytics dashboard for admin
- [ ] API endpoints for external integrations

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙌 Acknowledgments

- **Built by**: Abhishek Sandhu
- **Purpose**: College project exploring NLP applications in education
- **Tech Stack**: Flask, SpaCy, FuzzyWuzzy, Bootstrap
- **Special Thanks**: Open source community for amazing libraries

---

**⭐ Star this repository if you found it helpful!**

For questions or support, please open an issue on GitHub.

