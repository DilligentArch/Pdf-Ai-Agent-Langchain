
# 📄 PDF AI Agent with LangChain & Ollama

This project is a lightweight AI agent that can read and answer questions from **any PDF document** using a Retrieval-Augmented Generation (RAG) pipeline.

Built with:
- 🧠 [LangChain](https://www.langchain.com/)
- 💬 [Ollama](https://ollama.com/) (`phi4` model)
- 📚 FAISS vector store
- 📄 PyMuPDF for PDF parsing

---

## ✨ Features

- Load and process any PDF file
- Automatically split content into chunks
- Generate local embeddings using `Ollama` (`phi4`)
- Store embeddings in a FAISS vector store
- Use a local LLM to answer natural language questions about the document

---

## 📦 Tech Stack

- `LangChain`
- `Ollama` (LLM + Embeddings)
- `FAISS`
- `PyMuPDF`
- `Python`

---

## 🚀 Getting Started

### 1. Install Dependencies

```bash
pip install langchain pymupdf faiss-cpu
````

Make sure **Ollama** is installed and running locally:
➡️ [https://ollama.com/download](https://ollama.com/download)

Then pull the required model (e.g., `phi4`):

```bash
ollama pull phi4
```

---

### 2. Add Your PDF

Place your PDF in the project folder and set the path in the script:

```python
pdf_path = "your-document.pdf"
```

---

### 3. Run the Script

```bash
python pdf_ai_agent.py
```

You can then interact with the agent in the terminal:

```
> What is this PDF about?
> Who is the author?
> Summarize section 2.
```

---

## 🧠 How It Works

1. **Load PDF:** Parses PDF content using `PyMuPDFLoader`
2. **Split Text:** Uses `RecursiveCharacterTextSplitter` to chunk the data
3. **Embed:** Generates vector embeddings with `OllamaEmbeddings`
4. **Store:** Saves embeddings to a FAISS index
5. **Query:** Uses `ChatOllama` + `RetrievalQA` to answer your questions

---

## 📁 File Structure

```
📦 pdf-ai-agent-langchain
 ┣ 📄 your-document.pdf
 ┣ 📄 pdf_ai_agent.py
 ┗ 📄 README.md
```

---

## ✅ Example Use Cases

* Chat with academic papers
* Analyze business reports
* Extract information from technical documentation
* Explore books or manuals

---

## 📌 Notes

* This runs **fully offline**, assuming Ollama is set up locally
* You can replace `phi4` with other supported models as needed

---

## 📬 Feedback / Ideas?

If you're experimenting with AI agents and local LLMs, feel free to connect or suggest improvements!

---

### License

MIT License

```




