# 🩺 Medical Healthcare Chatbot

A multilingual AI-powered medical chatbot that provides information on diseases, symptoms, causes, precautions, and treatments.  
Built with **Qwen-7B**, **IndicTrans2**, and **FAISS**, it enables healthcare insights across multiple Indian languages.

---

## ✨ Features
- 🌐 **Multilingual Support**: Handles English and Indian regional languages.  
- 🔍 **Context-Aware Retrieval**: Uses FAISS for fast and accurate disease information search.  
- 🤖 **Generative Responses**: Leverages Qwen-7B to provide natural, human-like answers.  
- 📊 **Custom Dataset**: Curated disease dataset with symptoms, causes, treatments, and severity levels.  
- 🧠 **Translation Pipeline**: Bidirectional translation with IndicTrans2 for smooth user interaction.  

---

## 🛠 Tech Stack
- **Python**  
- **FAISS** for similarity search  
- **Hugging Face Transformers** (Qwen-7B)  
- **IndicTrans2** for translation  
- **Flask / Gradio** for chatbot interface  

---

## 🔄 How It Works (Pipeline)
1. Detects the user’s query language.  
2. Translates query into English using **IndicTrans2**.  
3. Retrieves top results from the **FAISS vector store** built on the disease dataset.  
4. Generates a response using **Qwen-7B** with the retrieved context.  
5. Translates the final answer back into the user’s language (if needed).  

---

## 📖 Dataset References
- Mendeley Dataset – Foundational medical data for model training and validation.  
  🔗 [Mendeley Dataset](https://data.mendeley.com/datasets/2cxccsxydc/1)  

- Qwen Model – Advanced multilingual model for natural language understanding and generation.  
  🔗 [Qwen-7B](https://huggingface.co/Qwen/Qwen-7B)  

- IndicTrans2 – Transformer-based translation system supporting nuanced communication across Indian regional languages.  
  🔗 [IndicTrans2 EN→Indic](https://huggingface.co/ai4bharat/indictrans2-en-indic-200M) | [IndicTrans2 Indic→EN](https://huggingface.co/ai4bharat/indictrans2-indic-en-200M)  

- Twilio Sandbox – Enabling seamless integration with WhatsApp for broad user accessibility.  
  🔗 [Twilio Sandbox](https://www.twilio.com/docs/whatsapp/sandbox)  

- WHO & CDC Guidelines – Ensuring medical accuracy and alignment with global public health.  
  🔗 [WHO Fact Sheets](https://www.who.int/news-room/fact-sheets)  


---

## ⚠️ Disclaimer
This chatbot is for **educational and informational purposes only**.  
It is **not a substitute for professional medical advice, diagnosis, or treatment**.  
Always seek guidance from a qualified healthcare provider for medical concerns.

