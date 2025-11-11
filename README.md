# 🧠 Sentimental Analysis on Reddit

Analyze Reddit posts and comments using **VADER sentiment analysis** — all through a simple **Flask web app**.

---

## 🚀 Project Overview

This project provides a **web-based sentiment analysis tool** for Reddit posts.  
It uses **VADER (Valence Aware Dictionary and sEntiment Reasoner)** to analyze and classify text as **positive**, **neutral**, or **negative**.

Built with **Flask**, it’s lightweight, extendable, and easy to deploy.

---

## 🌟 Features

- ✅ Fetch Reddit posts and comments  
- ✅ Analyze sentiment using VADER  
- ✅ Display scores and overall sentiment via a clean UI  
- ✅ Easily customizable and extendable backend  
- ✅ Ready for local or cloud deployment  

---
## 📁 Folder Structure

```
.
├── app/                   # Flask application package
├── instance/              # Configuration / instance-specific files
├── nltk_data/             # NLTK / VADER data
│   └── sentiment/
├── static/                # Static assets (CSS, images)
│   └── images/
├── .env                   # Environment variables
├── app.py                 # Flask app entry point
├── file.py                # Reddit data fetching & sentiment logic
├── requirements.txt       # Dependencies list
├── start.sh               # Startup script
└── test_sentiments.py     # Test module

```
---

## ⚙️ **Installation & Setup**

### 🧩 **Prerequisites**

- Python 3.x  
- `virtualenv` (recommended)  
- Reddit API credentials (`client_id`, `client_secret`, `user_agent`)  
- Internet access for NLTK/VADER data  

---

### 💻 **Setup Steps**

#### 1️. **Clone the Repository**
```
git clone https://github.com/Laxman17-crypto/Sentimental-Analysis-on-reddit.git
cd Sentimental-Analysis-on-reddit
```
---
#### 2. Create a Virtual Environment
```
python -m venv venv
# Activate
venv\Scripts\activate   # on Windows
source venv/bin/activate  # on macOS/Linux
```

#### 3.Install Dependencies
```
pip install -r requirements.txt
```

#### 4.Configure Environment Variables
Create a .env file in the project root (if not already present):
```
SQLALCHEMY_DATABASE_URL="sqlite:///sentiments.db"
REDDIT_CLIENT_ID=your_client_id
REDDIT_CLIENT_SECRET=your_client_secret
REDDIT_USER_AGENT=your_user_agent
```

#### 5.Download NLTK Data (Optional)
```
import nltk
nltk.download('vader_lexicon')
```

## ▶️ Run the Application

Start the Flask app:
```bash
python app.py
```
or using Flask CLI:
```bash
flask run
```
Then open your browser and visit:
```cpp
http://127.0.0.1:5000/api/sentiment
```

## 🧪 Running Tests
Run the included test file:
```bash
pytest test_sentiments.py
```
## 🔍 How It Works

1. **Reddit Fetching** – Uses Reddit API (via file.py) to collect posts/comments.

2. **Sentiment Analysis** – Text is passed through the VADER analyzer.

3. **Classification** – Based on compound scores:

    ```compound > 0.05``` → Positive

    ```compound < -0.05``` → Negative

    Otherwise → Neutral

4. **Results Displayed** – Flask renders the analyzed data in a web interface.

## 💡 Future Enhancements

- Add subreddit/topic filters

- Aggregate sentiment statistics

- Integrate Transformer-based models (e.g., BERT)

- Visual sentiment dashboards

- Dockerize and deploy on Render/Heroku/AWS

## 🧾 License

This project is open-source under the **MIT License**.
```
MIT License  
© 2025 Laxman17-crypto
```

## 🙏 Acknowledgements

- VADER Sentiment Analyzer

- Reddit API

- Flask and NLTK communities for their support and tools.

## 🧑‍💻 Author

Laxman17-crypto
📦 **GitHub:** : [Laxman17-crypto](https://github.com/Laxman17-crypto)





