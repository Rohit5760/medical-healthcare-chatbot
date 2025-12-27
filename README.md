# QwenVeda 🧠🩺  
![Platform](https://img.shields.io/badge/platform-Windows-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Offline](https://img.shields.io/badge/Offline-Yes-success)

**Offline Multilingual Medical Information Assistant (CPU-only)**

QwenVeda is a fully offline desktop medical information chatbot designed to provide **structured, reliable, and reference-backed health information** without relying on cloud APIs or internet connectivity.

The system is built with a **retrieval-augmented generation (RAG)** pipeline using FAISS, MiniLM-based reranking, and Qwen medical language models — optimized to run entirely on **CPU**.

> ⚠️ QwenVeda is **not a diagnostic tool**. It is intended for educational and informational purposes only.

---

## 🔍 Key Features

- ✅ **Fully Offline** (no internet required)
- ✅ **CPU-only inference** (no CUDA / GPU required)
- 🌍 **Multilingual support**
  - English
  - Indian regional languages (via M2M100)
- 🧠 **RAG-based architecture**
  - FAISS vector search
  - Cross-encoder reranking
- 📋 **Structured medical responses**
  - Introduction
  - Causes
  - Symptoms
  - Precautions
  - References
  - Safety disclaimer
- 🔐 **Privacy-first**
  - No data collection
  - No external API calls

---

## 🏗️ System Architecture

**Pipeline overview:**

1. User query received via desktop UI
2. Language detection & translation (M2M100)
3. Intent classification (MiniLM)
4. FAISS vector retrieval
5. Cross-encoder reranking
6. Qwen medical LLM generates structured response
7. Output translated back to user language
8. Response displayed in UI

---

## 📦 Models Used

- **Qwen Medical LLM** (quantized, CPU-friendly)
- **MiniLM (all-MiniLM-L6-v2)** — embeddings & intent detection
- **MiniLM Cross-Encoder** — reranking
- **M2M100 (418M)** — multilingual translation
- **FAISS** — vector similarity search

Due to size constraints, model files are not included in this repository.

The Windows installer (linked below) contains all required models and dependencies.
---

## 💻 Platform Support

| Platform | Supported |
|--------|----------|
| Windows 10 / 11 (64-bit) | ✅ |
| macOS | ❌ |
| Linux | ❌ |

> Reason: Offline CPU inference relies on Windows-native `llama-cpp` binaries.

---

## ⬇️ Download (Windows)

👉 **[Download QwenVeda Installer – Windows (Offline)](https://drive.google.com/file/d/1BeAZQCot000VWx30zOo544JVM_Es50pI/view?usp=sharing)**

### Installer Notes
- No Python installation required
- No C++ build tools required
- No environment setup needed
- Just download → install → run

---
## 📁 Project Structure

```text
QwenVeda/
├─ main.py
├─ ui_chat.py
├─ pipeline.py
├─ translation.py
├─ faiss_search.py
├─ load_models.py
├─ qwen_inference.py
├─ requirements.txt
├─ README.md
├─ LICENSE
└─ .gitignore
```

---

## 🚀 How to Run (Installed Version)

1. Install the application using the installer
2. Launch **QwenVeda** from:
   - Desktop shortcut **or**
   - Start Menu
3. Wait for models to load
4. Enter a medical query

---

## 🧪 Example Queries

- “What are the symptoms and causes of dengue?”
- “Diabetes precautions in elderly patients”
- “Explain asthma in simple terms”
- “Heart attack warning signs”

---

## ⚠️ Medical Disclaimer

QwenVeda does **not** provide medical diagnoses, prescriptions, or treatment advice.

Always consult a qualified medical professional for diagnosis or treatment decisions.

---

## 🛠️ Development Setup (For Developers)

> ⚠️ This section is for contributors and advanced users only.

```bash
python -m venv vedaenv
vedaenv\Scripts\activate
pip install -r requirements.txt
python app/main.py
```

---

## 👨‍💻 Author

- Rohit Anand Bangar  
- Shivanurag Yayavaram  
- Samriddhi Gupta  
- Rishabh Khuswaha  
- Abhay Gour  
- Shan Rehman

---
