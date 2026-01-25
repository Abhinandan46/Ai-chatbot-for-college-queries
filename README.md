<div align="center">

# 🎓 AI College Query Chatbot

### Intelligent NLP-Powered Assistant for College Information

[![Flask](https://img.shields.io/badge/Flask-3.1.0-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![SpaCy](https://img.shields.io/badge/SpaCy-3.7.4-09A3D5?style=for-the-badge&logo=spacy&logoColor=white)](https://spacy.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

**Get instant answers to college queries • 24/7 availability • Powered by AI**

[Features](#-features) • [Demo](#-demo) • [Installation](#-installation) • [Usage](#-usage) • [Contributing](#-contributing)

</div>

---

## 📖 Overview

An intelligent chatbot built with cutting-edge Natural Language Processing (NLP) technology to provide instant, accurate answers to college-related queries. Whether you're a prospective student, current student, parent, or visitor, get the information you need in seconds!

### 🎯 What Can It Do?

- 💬 Answer questions about admissions, courses, and programs
- 💰 Provide information on fees, scholarships, and financial aid
- 🏠 Share details about hostel facilities and campus life
- 🎓 Discuss placement statistics and career opportunities
- 🕒 Respond to queries about schedules, events, and deadlines
- 🤖 Learn from conversations with AI-powered fallback responses

---

## ✨ Features

### 🧠 **Smart Intent Detection**
- Advanced NLP using SpaCy for understanding user queries
- Keyword-based intent recognition for accurate responses
- Contextual conversation flow

### 📚 **Multi-Source Knowledge Base**
- **Rule-Based System**: Custom `knowledge_base.py` for structured responses
- **JSON Storage**: Dynamic FAQ management with easy updates
- **Fuzzy Matching**: Finds closest answers even with typos or variations
- **AI Fallback**: HuggingFace models for handling unknown queries

### 🔐 **User Management**
- Secure authentication with password hashing
- Session management for personalized experiences
- Chat history tracking for each user

### 💡 **Intelligent Responses**
- Context-aware answers using HuggingFace's Question-Answering models
- Text generation fallback for complex queries
- Graceful handling of unknown questions

### 🎨 **User-Friendly Interface**
- Clean, modern web UI
- Responsive design for all devices
- Intuitive chat experience

---

## 🖼️ Demo

<div align="center">

### Main Chat Interface
<img width="1920" height="1080" alt="Chat Interface" src="https://github.com/user-attachments/assets/ab8191bd-a6d6-430b-8621-29739f319f9a" />

### Interactive Conversations
<img width="1920" height="1080" alt="Conversation Flow" src="https://github.com/user-attachments/assets/710ef858-78e6-453a-a64c-66abca859af3" />

### Smart Response System
<img width="1920" height="1080" alt="Smart Responses" src="https://github.com/user-attachments/assets/2db074de-688c-43fc-87d7-667593217b02" />

### Knowledge Base Integration
<img width="1920" height="1080" alt="Knowledge Base" src="https://github.com/user-attachments/assets/29f874a4-7b74-4165-8c3d-97ce61a3496a" />

</div>

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Flask** | Web framework for backend server |
| **SpaCy** | Natural Language Processing and tokenization |
| **FuzzyWuzzy** | Fuzzy string matching for query similarity |
| **HuggingFace API** | AI-powered fallback for complex queries |
| **Werkzeug** | Secure password hashing |
| **Python-dotenv** | Environment variable management |

---

## 🚀 Installation

### Prerequisites

- Python 3.7 or higher
- pip (Python package installer)
- Git

### Step-by-Step Setup

1️⃣ **Clone the Repository**
```bash
git clone https://github.com/Abhinandan46/Ai-chatbot-for-college-queries.git
cd Ai-chatbot-for-college-queries
```

2️⃣ **Create Virtual Environment (Recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3️⃣ **Install Dependencies**
```bash
pip install -r requirements.txt
```

4️⃣ **Download SpaCy Language Model**
```bash
python -m spacy download en_core_web_sm
```

5️⃣ **Configure Environment Variables**

Create a `.env` file in the root directory:
```env
SECRET_KEY=your_secret_key_here
HF_API_KEY=your_huggingface_api_key_here
```

> 💡 **Tip**: Get a free HuggingFace API key at [https://huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)

6️⃣ **Run the Application**
```bash
python app.py
```

7️⃣ **Access the Chatbot**

Open your browser and navigate to:
```
http://localhost:5000
```

---

## 📁 Project Structure

```
Ai-chatbot-for-college-queries/
│
├── 📄 app.py                    # Main Flask application
├── 📄 knowledge_base.py         # Rule-based intent & keyword responses
├── 📄 requirements.txt          # Python dependencies
├── 📄 .env                      # Environment variables (create this)
├── 📄 .gitignore               # Git ignore file
├── 📄 LICENSE                   # Project license
├── 📄 README.md                 # This file
│
├── 📂 static/                   # Static assets
│   ├── style.css               # Custom CSS styling
│   └── assets/                 # Images and icons
│
├── 📂 templates/                # HTML templates
│   └── index.html              # Main chat interface
│
├── 📂 en_core_web_sm/          # SpaCy language model
│
├── 📄 knowledge_base.json       # JSON-based FAQ storage
├── 📄 chat_history.json         # User chat history
└── 📄 users.json                # User authentication data
```

---

## 💻 Usage

### Basic Queries

Ask the chatbot natural questions like:

- "What are the admission requirements?"
- "Tell me about the computer science program"
- "How much is the tuition fee?"
- "Do you offer scholarships?"
- "What are the hostel facilities?"
- "Tell me about campus placements"

### Admin Features

**Add New FAQs**: Update the `knowledge_base.json` file with new question-answer pairs.

```json
{
  "What is the library timing?": "The library is open from 8 AM to 10 PM on weekdays.",
  "How do I apply for hostel?": "You can apply for hostel through the student portal during admission."
}
```

---

## 🔧 Configuration

### Knowledge Base Customization

Edit `knowledge_base.py` to add new intents and keywords:

```python
intent_keywords = {
    "greeting": ["hi", "hello", "hey"],
    "admission": ["admission", "apply", "enrollment"],
    "fees": ["fee", "cost", "tuition"],
    # Add your custom intents here
}

intent_responses = {
    "greeting": "Hello! How can I help you today?",
    "admission": "Our admission process begins in June...",
    # Add your custom responses here
}
```

### HuggingFace Model Selection

In `app.py`, you can change the AI models:

```python
# For Question-Answering
qa_url = "https://api-inference.huggingface.co/models/deepset/roberta-base-squad2"

# For Text Generation
tg_url = "https://api-inference.huggingface.co/models/google/flan-t5-base"
```

---

## 🤝 Contributing

Contributions are what make the open-source community amazing! Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions

- 🌍 Multi-language support
- 📊 Analytics dashboard for admin
- 🎨 UI/UX improvements
- 🧪 Unit tests
- 📱 Mobile app integration
- 🔊 Voice input/output

---

## 🐛 Known Issues & Roadmap

### Current Limitations
- Requires internet connection for HuggingFace API
- Limited to text-based queries

### Future Enhancements
- [ ] Voice recognition support
- [ ] Multi-language support (Hindi, Spanish, etc.)
- [ ] Integration with college database
- [ ] Admin dashboard for analytics
- [ ] Export chat transcripts
- [ ] Mobile responsive improvements

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Abhinandan46**

- GitHub: [@Abhinandan46](https://github.com/Abhinandan46)
- Repository: [Ai-chatbot-for-college-queries](https://github.com/Abhinandan46/Ai-chatbot-for-college-queries)

---

## 🙏 Acknowledgments

- [SpaCy](https://spacy.io/) for powerful NLP capabilities
- [HuggingFace](https://huggingface.co/) for state-of-the-art AI models
- [Flask](https://flask.palletsprojects.com/) for the lightweight web framework
- All contributors and users of this project

---

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/Abhinandan46/Ai-chatbot-for-college-queries/issues) page
2. Create a new issue with detailed information
3. Star ⭐ the repository if you find it helpful!

---

<div align="center">

**Made with ❤️ by Abhinandan46**

If this project helped you, please give it a ⭐!

[⬆ Back to Top](#-ai-college-query-chatbot)

</div>
