# 🌐✨ Groq-Powered LLM Translator API  
### ⚡ FastAPI + LangChain + LangServe + Groq (GPT-OSS-20B)

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-API%20Framework-009688?logo=fastapi)
![LangChain](https://img.shields.io/badge/LangChain-LCEL-orange)
![Groq](https://img.shields.io/badge/Groq-LPU%20Powered-red)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

---

## 🚀 **About the Project**

This project is a **lightning-fast Translation API** built using:

- ⚡ **FastAPI** for serving REST APIs  
- 🧠 **LangChain Expression Language (LCEL)** for prompt chaining  
- 🔥 **Groq’s GPT-OSS-20B** model for ultra-fast inference  
- 🌐 **LangServe** for automatic API and Playground generation  

With this setup, you can create a fully functional **LLM microservice** in seconds!

---

## 🧩 **Features**

- 🌍 Translate text into **any language**
- ⚡ Powered by **Groq’s low-latency LPU hardware**
- 🎯 Clean and modular LangChain pipeline (Prompt → Model → Parser)
- 🛠️ Auto-generated API routes via **LangServe**
- 🧪 Built-in interactive **Playground UI**
- 🚀 Ready to deploy anywhere (Docker, Render, Railway, etc.)

---

## 🏗️ **Architecture**

```txt
                  +-------------------------+
                  |      Client Request      |
                  |   (text + language)      |
                  +-------------+------------+
                                |
                                v
                     +-------------------+
                     |      FastAPI      |
                     |  /chain endpoint  |
                     +-------------------+
                                |
                                v
                    +----------------------+
                    |     LangServe        |
                    |  Runnable Pipeline   |
                    +----------------------+
                                |
                                v
         +------------------+       +---------------------------+
         | Prompt Template  | --->  | Groq GPT-OSS-20B Model    |
         +------------------+       +---------------------------+
                                |
                                v
                     +----------------------+
                     |  String Output Parser |
                     +----------------------+
                                |
                                v
                     +------------------------+
                     |  JSON Translation Out   |
                     +------------------------+
