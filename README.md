# 🚀 VectorDB – Build Your Own AI

A C++ based Vector Database project that combines vector search, document storage, and AI-powered question answering using Retrieval-Augmented Generation (RAG).

## ✨ Features

- 🔍 Vector similarity search
- ⚡ HNSW-based vector indexing
- 📄 Document insertion and storage
- 🧠 Semantic document search
- 🤖 AI-powered question answering
- 🌐 Web-based user interface
- 🔗 REST API using C++

## 🛠️ Tech Stack

- **Language:** C++17
- **Vector Search:** HNSW
- **AI Integration:** Ollama
- **Embedding Model:** nomic-embed-text
- **Language Model:** llama3.2
- **HTTP Server:** cpp-httplib
- **Frontend:** HTML, CSS, JavaScript

## 📁 Project Structure

```text
VectorDB/
│
├── main.cpp
├── httplib.h
├── index.html
├── Dockerfile
├── .gitignore
└── README.md
```

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/prateek2k5/VectorDB.git
cd VectorDB
```

### 2. Install Requirements

Make sure you have installed:

- GCC C++ Compiler
- C++17 support
- Git
- [Ollama](https://ollama.com/download)

### 3. Download Ollama Models

Open your terminal and run:

```bash
ollama pull nomic-embed-text
ollama pull llama3.2
```

### 4. Start Ollama

```bash
ollama serve
```

Keep Ollama running in the background.

### 5. Compile the Project

**Windows (MinGW):**

```bash
g++ -std=c++17 -O2 -pthread main.cpp -o vectordb.exe
```

**Linux:**

```bash
g++ -std=c++17 -O2 -pthread main.cpp -o vectordb
```

### 6. Run the Project

**Windows:**

```bash
.\vectordb.exe
```

**Linux:**

```bash
./vectordb
```

### 7. Open in Browser

Visit:

```text
http://localhost:8080
```

If your application uses a different port, open the port configured in `main.cpp`.

## 💡 How It Works

1. Users can store and search vector data.
2. Documents are divided into smaller chunks.
3. Ollama generates embeddings for document chunks.
4. Relevant document chunks are retrieved using vector similarity search.
5. The retrieved context is passed to the language model.
6. The AI generates an answer based on the retrieved information.

## 🔧 Troubleshooting

**Ollama unavailable:**

```bash
ollama serve
```

**Model not found:**

```bash
ollama pull nomic-embed-text
ollama pull llama3.2
```

**Compilation issues:**

- Check that GCC is installed.
- Make sure C++17 is supported.
- Verify that `httplib.h` is present.

## 🔐 Security

- Never upload API keys or `.env` files to GitHub.
- Keep private credentials in environment variables.
- Do not expose secrets in frontend code.

## 👨‍💻 Developer

**Prateek Verma**

## 📜 License

Created for educational and learning purposes.

---

⭐ If you find this project useful, consider giving it a star!
