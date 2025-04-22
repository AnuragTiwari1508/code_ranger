```markdown
# 🤖 Code Ranger - Gemini AI Chatbot with MongoDB Integration

Welcome to **Code Ranger**, a full-stack chatbot project that connects Google's Gemini AI with a MongoDB database to answer user queries in real-time. This app is designed for developers and AI enthusiasts who want to create powerful, database-aware chatbots with persistent storage and a clean API.

---

## 📦 Tech Stack

- **Frontend**: HTML/CSS/JS (or your preferred stack)
- **Backend**: Node.js + Express
- **AI**: Gemini Pro via Google AI API
- **Database**: MongoDB (Mongoose ODM)
- **Hosting**: Vercel / Localhost

---

## 🧠 Features

- 🔗 Connect Gemini Pro chatbot to MongoDB
- 💬 Ask questions and get AI-powered answers
- 🧾 Store every query and response in your MongoDB collection
- 🔄 RESTful API structure with clean endpoints
- 📸 Screenshot placeholders for walkthrough

---

## ⚙️ Project Setup

### 1. Clone the Repository

```bash
git clone https://github.com/AnuragTiwari1508/code_ranger.git
cd code_ranger
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Create `.env` File

Create a `.env` file in the root folder and add:

```env
MONGODB_URI=your_mongodb_connection_string
GEMINI_API_KEY=your_google_gemini_api_key
PORT=3000
```

### 4. Run the Server

```bash
npm start
```

Server will start on: `http://localhost:3000`

---

## 🧪 API Endpoints

### 🔹 `POST /api/chat`

Send user question to Gemini chatbot and get a response.

#### 📤 Request (JSON)
```json
{
  "prompt": "What is the Indian Constitution?"
}
```

#### 📥 Response
```json
{
  "response": "The Indian Constitution is the supreme law of India..."
}
```

✅ Also stores `prompt` and `response` in MongoDB.

---

## 📂 Project Structure

```
code_ranger/
│
├── server.js               # Express server
├── routes/
│   └── chat.js             # Chat route for Gemini API
├── models/
│   └── Chat.js             # Mongoose schema
├── .env                    # API keys & config
└── README.md
```

---

## 🧑‍💻 MongoDB Schema

```js
const ChatSchema = new mongoose.Schema({
  prompt: String,
  response: String,
  createdAt: { type: Date, default: Date.now }
});
```

Every user prompt and AI response is stored securely with timestamps.

---

## 📸 Screenshots (Add Here)

> ✨ _Upload these screenshots to your repo and update the links._

### 🖼️ Home UI  
![image](https://github.com/user-attachments/assets/a27c1702-c4af-4f04-887a-f20a1b99ebeb)


### 💬 Chat UI  
![Chat in action](./screenshots/chat.png)

---

## 🔒 Security Notes

- Never commit your `.env` file.
- Secure your Gemini API key.
- Use rate-limiting/middleware for production deployments.

---

---

## 🙌 Author

**Anurag Tiwari**  
IET DAVV | [GitHub](https://github.com/AnuragTiwari1508)

---


> “Code is the new pen, and AI is the new ink. Together, they write the future.”

```
