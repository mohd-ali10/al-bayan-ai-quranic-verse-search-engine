# 📖 AL-BAYAN | AI-Based Quranic Verse Search Engine

**AL-BAYAN** is an AI-powered Quranic search engine developed as a **Final Year Project (FYP)**, designed to bridge the gap between traditional keyword search and semantic understanding. It provides accurate, context-aware Quranic verse retrieval using **Hybrid Search (TF-IDF + Semantic Embeddings)** and **Retrieval-Augmented Generation (RAG)** techniques.

---

## 🎯 Project Objectives

* Enable semantic understanding of Quranic verses beyond exact keyword matching.
* Support multi-language search (Arabic, English, Urdu).
* Integrate AI-generated explanations using large language models (Google Gemini 1.5 Flash).
* Provide a modern, user-friendly web interface for Quranic study and research.

---

## 🚀 Key Features

* **Hybrid Search Engine**: Combines TF-IDF for precise keyword matching and Sentence Transformers for semantic similarity.
* **AI-Powered Insights (RAG)**: Generates contextual and scholarly summaries for queries.
* **Multi-Language Support**: Arabic Quran text, English translation (Sahih International), and Urdu translation.
* **Voice-Based Search**: Search Quranic verses using voice input.
* **Smart UI Controls**: Dark mode, adjustable font sizes, translation toggle.
* **Shareable Verse Cards**: Generate social media-friendly verse images.

---

## 🛠️ Tech Stack

### Backend

* Python
* Flask

### AI / Machine Learning

* PyTorch
* Sentence-Transformers (`all-MiniLM-L6-v2`)
* Scikit-learn (TF-IDF)

### LLM Integration

* Google GenAI SDK (Gemini)

### Frontend

* HTML5
* Tailwind CSS
* JavaScript

### Data

* Custom Quran JSON dataset
* Tafsir Ibn Kathir (English & Urdu)
> Note: Due to GitHub’s 25 MB file size limit, the final dataset is split into two JSON files and merged dynamically at runtime.

---

## 📂 Project Structure

```
AL-BAYAN/
│
├── app.py                      # Main Flask application
├── search_engine.py            # Hybrid search + RAG logic
├── models.py                   # ML model loading & embeddings
├── utils.py                    # Helper functions
├── cli.py                      # Optional CLI interface
│
├── requirements.txt            # Python dependencies
├── .gitignore                  # Ignored files
├── README.md                   # Main project documentation
│
├── templates/                  # Frontend HTML templates
│   ├── base.html
│   ├── index.html
│   ├── search.html
│   ├── browse.html
│   └── about.html
│
├── static/                     # Static frontend assets
│   ├── css/
│   │   └── styles.css
│   │
│   ├── js/
│   │   └── main.js
│   │
│   └── assets/                 # Screenshots (for viva)
│       ├── Home.png
│       ├── Browse_Surah.png
│       ├── About.png
│       └── README.md
│
├── data/                       # Dataset directory
│   ├── README.md               # Dataset explanation
│   │
│   ├── quran_part_1.json       # Surah 1–57
│   ├── quran_part_2.json       # Surah 58–114
│   │
│   └── sources/                # Raw / optional datasets
│       ├── README.md
│       ├── quran.json
│       ├── quran_ur.json
│       ├── quran_with_urdu.json
│       ├── en-tafsir-ibn-kathir.json
│       └── tafseer-ibn-e-kaseer-urdu.json
│
└── scripts/                    # Data preprocessing scripts
    ├── merge_english_urdu.py
    ├── merge_tafseer.py
    ├── final_merge.py
    └── precompute_embeddings.py

```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/AL-BAYAN.git
cd AL-BAYAN
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Set Up Google Gemini API Key

* Obtain an API key from [Google AI Studio](https://aistudio.google.com/).
* Set it as an environment variable (recommended):

```bash
export GEMINI_API_KEY="your_api_key_here"
```

or configure directly in `app.py` for local testing.

### 4️⃣ Run the Application

```bash
python backend/app.py
```

Visit: `http://127.0.0.1:5000`

---

## 📦 Dataset Information

Due to GitHub file size limitations, large Quran and Tafsir datasets may not be included. Access full datasets via Google Drive:

> [Add your Google Drive dataset link here]

**Included in `data/` folder:**

* Arabic Quran text (`quran.json`)
* English & Urdu translations (`quran_with_urdu.json`)
* Tafsir Ibn Kathir (English & Urdu)

---

##  Screenshots

Screenshots of UI and features can be added to an `assets/` folder and referenced here.

---

## 📄 License

This project is developed strictly for educational and academic purposes as a Final Year Project (FYP).

---

## 🕌 Acknowledgments

All Quranic text and Tafsir content are used with respect and solely for educational research purposes.

