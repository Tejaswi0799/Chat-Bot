# Android Chatbot API using Flask & Ngrok

## 📌 Project Overview
This project is a **Flask-based chatbot API** that can be integrated into an **Android application**. The chatbot is built using **ChatterBot**, trained with a corpus of conversations, and is accessible over the internet using **Ngrok**. The API enables Android applications to send user messages and receive intelligent chatbot responses.

## ✨ Features
- ✅ **Chatbot using ChatterBot** – Pretrained with a conversational corpus
- ✅ **Flask API** – Serves chatbot responses via RESTful endpoints
- ✅ **Ngrok Integration** – Exposes the API publicly for easy access
- ✅ **CORS Enabled** – Secure communication between the Android app & API
- ✅ **Android Integration Ready** – Connect with Retrofit/Volley in Android apps

## 📂 Project Structure
```
├── chatbot_api.py  # Flask server with chatbot logic
├── requirements.txt  # Project dependencies
├── README.md  # Project documentation
└── .gitignore  # Files to be ignored in Git
```

## 🚀 Getting Started
### 1️⃣ Install Dependencies
Ensure you have **Python 3.x** installed, then run:
```bash
pip install flask flask-cors chatterbot chatterbot_corpus pyngrok
```

### 2️⃣ Run the Flask Chatbot
```bash
python chatbot_api.py
```
This will start the API on **http://127.0.0.1:5000**.

### 3️⃣ Expose API with Ngrok
```bash
ngrok http 5000
```
Copy the **public URL** (e.g., `https://your-ngrok-url.ngrok-free.app`) for use in Postman or Android.

## 📡 API Usage
### 🔹 API Endpoint:
- **URL:** `POST /chat`
- **Request Body (JSON):**
  ```json
  {
    "message": "Hello"
  }
  ```
- **Response (JSON):**
  ```json
  {
    "response": "Hi there! How can I help you?"
  }
  ```

## 📱 Integrating with an Android App
Use **Retrofit** or **Volley** to send API requests from an Android app.

### Retrofit Example (Java)
```java
public interface ApiService {
    @POST("/chat")
    @Headers("Content-Type: application/json")
    Call<ResponseBody> getChatResponse(@Body RequestBody body);
}
```
Replace `BASE_URL` with the **Ngrok public URL**.

## 💡 Future Enhancements
- 🔹 Implement **AI-based chatbot (GPT/Transformers)**
- 🔹 Add **User Authentication** for secured access
- 🔹 Deploy the API to **AWS/GCP/Heroku** for production use

## 👨‍💻 Author
👤Gunnala Durga Tejaswi  
💼 Data Analyst | Automation Expert | Chatbot Developer  
🔗 [LinkedIn Profile](#) | 📧 [Email](#)

## 📜 License
📄 This project is **open-source** under the **MIT License**.

---
This README provides **everything needed** to set up, run, and integrate the chatbot API. 🚀 Feel free to contribute and improve the project! 😊

# Chat-Bot
