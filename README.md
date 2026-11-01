# 🚀 VectorDB – Build Your Own AI

A C++ based Vector Database project with vector similarity search, document storage, and AI-powered question answering using Retrieval-Augmented Generation (RAG).

## ✨ Features

- Vector storage and similarity search
- HNSW-based vector indexing
- Document insertion and search
- Semantic search
- AI-powered question answering
- Web-based user interface
- C++ REST API
- Ollama integration

## 🛠️ Technologies Used

- C++17
- HNSW
- cpp-httplib
- Ollama
- nomic-embed-text
- llama3.2
- HTML, CSS and JavaScript

---

# 💻 How to Run the Project on Windows

Follow these steps carefully.

## PART 1: First-Time Setup

Complete these steps only once when setting up the project for the first time.

### Step 1: Install Required Software

Install the following:

1. **Git:** https://git-scm.com/
2. **GCC Compiler (MinGW):** https://www.mingw-w64.org/
3. **Ollama:** https://ollama.com/download

After installing GCC, make sure its `bin` folder is added to your Windows PATH.

Check installation:

Open PowerShell and run:

```powershell
g++ --version
```

```powershell
ollama --version
```

Both commands should display version information.

### Step 2: Download the Project

Open PowerShell.

Run:

```powershell
git clone https://github.com/prateek2k5/VectorDB.git
```

Move into the project folder:

```powershell
cd VectorDB
```

### Step 3: Download AI Models

Run these commands in PowerShell:

```powershell
ollama pull nomic-embed-text
```

```powershell
ollama pull llama3.2
```

These models are downloaded once. You do not need to download them every time you run the project.

### Step 4: Compile the Project

Make sure PowerShell is inside the VectorDB project folder.

Run:

```powershell
g++ -std=c++17 -O2 -pthread main.cpp -o vectordb.exe
```

If compilation succeeds, a `vectordb.exe` file will be created in the project folder.

### Step 5: Start Ollama

Open a **second PowerShell window**.

Run:

```powershell
ollama serve
```

Keep this window open while using the AI features.

If Ollama is already running in the background, you do not need to start it again.

### Step 6: Start VectorDB

Return to the first PowerShell window.

Make sure you are inside the project folder.

Run:

```powershell
.\vectordb.exe
```

The C++ server will start.

Keep this window open too.

### Step 7: Open the Website

Open Google Chrome or another browser.

Visit:

```text
http://localhost:8080
```

If your server is configured to use another port, use that port instead.

You can now use:

- **Search:** Search vector records.
- **Documents:** Insert and search documents.
- **Ask AI:** Ask questions using document context.

---

# 🔄 PART 2: How to Restart the Project

You do NOT need to clone the repository, download models, or compile the project again every time.

Whenever you close everything and want to run the project again:

### Step 1: Open PowerShell

Open PowerShell and move into your existing project folder:

```powershell
cd "$HOME\Downloads\VectorDB"
```

If your project is saved somewhere else, use that folder's actual path.

### Step 2: Start Ollama

Open another PowerShell window.

Run:

```powershell
ollama serve
```

If Ollama is already running, skip this command.

### Step 3: Start VectorDB

In the first PowerShell window, run:

```powershell
.\vectordb.exe
```

### Step 4: Open the Browser

Visit:

```text
http://localhost:8080
```

Your project is running again!

---

# 🛑 How to Stop the Project

To stop the C++ server:

1. Open the terminal running VectorDB.
2. Press `Ctrl + C`.

To stop Ollama manually:

1. Open the terminal running Ollama.
2. Press `Ctrl + C`.

You can close the browser whenever you want.

---

# 🧰 Troubleshooting

### 1. Ollama Unavailable

Make sure Ollama is running:

```powershell
ollama serve
```

### 2. Model Not Found

Download the models:

```powershell
ollama pull nomic-embed-text
ollama pull llama3.2
```

### 3. g++ Is Not Recognized

Install GCC and add its `bin` folder to the Windows PATH.

Restart PowerShell and check:

```powershell
g++ --version
```

### 4. vectordb.exe Not Found

Compile the project again:

```powershell
g++ -std=c++17 -O2 -pthread main.cpp -o vectordb.exe
```

### 5. Website Is Not Opening

- Check whether the C++ server is running.
- Check the port configured in `main.cpp`.
- Make sure the browser URL uses the correct port.

---

# 🔐 Security

- Never upload `.env` files or private API keys to GitHub.
- Keep credentials private.
- Do not expose API keys in frontend code.

---

# 👨‍💻 Developer

**Prateek Verma**

## ⭐ Support

If you find this project useful, consider giving the repository a star!

