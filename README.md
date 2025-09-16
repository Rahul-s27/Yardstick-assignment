# Yardstick-assignment using Groq API  

This project implements **two core tasks** using the **Groq API (OpenAI-compatible SDK)**.  
It demonstrates managing conversation history with summarization and extracting structured information using a JSON schema.

---

## 📌 Tasks Implemented  

### **Task 1: Managing Conversation History with Summarization**  
- Maintains a running conversation history between user and assistant.  
- Implements **truncation options**:  
  - By number of conversation turns (last `n` messages).  
  - By character length of messages.  
- Adds **periodic summarization**:  
  - Summarizes the conversation after every `k-th` run.  
  - Stores the summary in the conversation history.  
- Uses the Groq model: **`moonshotai/kimi-k2-instruct-0905`**.  
- Demonstrated with multiple conversation samples showing truncation and k-th run summarization.  

### **Task 2: JSON Schema Classification & Information Extraction**  
- Defines a **JSON schema** to extract 5 user details:  
  - Name, Email, Phone, Location, Age.  
- Uses **OpenAI function calling** with Groq API to return structured outputs.  
- Demonstrates:  
  - Parsing of 3 sample chats.  
  - Validation of outputs against the JSON schema.  

---

## ⚙️ Requirements  

- **Python 3.9+**  
- **Libraries**:  
  ```bash
  pip install openai jsonschema requests
