# Retrieval-Augmented-Generation-over-Web-Articles-using-LangChain-Mistral


This project is a question-answering (QA) system over news articles using **LangChain**, **Streamlit**, **Mistral AI**, and **Chroma vector store**. Given a news URL, the app scrapes the article, chunks the content, stores it in a vector database, and allows the user to query it conversationally using a large language model.

---

## 🚀 Features

- 🔗 Enter any financial news URL
- 🧠 Extract and chunk the article using Unstructured
- 🗃️ Store chunks in a Chroma vector DB
- 💬 Ask questions conversationally using Mistral LLM
- 🖥️ Simple Streamlit UI

---

## 📂 Project Structure

```
.
├── main.py                   # Streamlit app file
├── langchain_helper.py      # LLM + Chroma + LangChain logic
├── requirements.txt         # Python dependencies
└── README.md                # Project overview
```

---

## 🧠 How it Works

1. Load article from URL using `UnstructuredURLLoader`
2. Chunk it using `RecursiveCharacterTextSplitter`
3. Generate vector embeddings via `HuggingFaceBgeEmbeddings`
4. Store in Chroma vector database
5. Use `RetrievalQAWithSourcesChain` with `Mistral` LLM
6. Ask questions via UI powered by Streamlit

---

## 🛠️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/Druva4444/-Retrieval-Augmented-Generation-over-Web-Articles-using-LangChain-Mistral.git
cd -Retrieval-Augmented-Generation-over-Web-Articles-using-LangChain-Mistral
```

### 2. Create virtual environment

```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add Mistral API Key

Create a `.env` file or export:

```bash
export MISTRAL_API_KEY=your_key_here
```

Or add this in your Python file (not recommended for production):

```python
os.environ['MISTRAL_API_KEY'] = 'your_key_here'
```

---

## ▶️ Run the App

```bash
streamlit run app.py
```

Visit `http://localhost:8501` in your browser.

---

## 🧪 Sample Use

Use this URL:

```
https://www.moneycontrol.com/news/business/markets/gainers-losers-top-10-stocks-that-moved-the-most-on-july-23-13313862.html
```

Ask:

> "How much did Nifty reclaim in today's session?"

---

## 📦 requirements.txt

```
streamlit
langchain>=0.2.0
langchain-community
langchain-core
chromadb
unstructured
huggingface-hub
sentence-transformers
mistralai
tiktoken
requests
```

---

## 📜 License

MIT License

---

## 🙌 Acknowledgements

- [LangChain](https://www.langchain.com/)
- [Mistral AI](https://mistral.ai/)
- [Streamlit](https://streamlit.io/)
- [Unstructured](https://github.com/Unstructured-IO/unstructured)
