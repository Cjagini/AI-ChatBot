# 🤖 AI ChatBot Application

A modern, full-stack AI chatbot application powered by OpenAI's GPT technology. This application provides a seamless conversational experience with real-time responses.

## Features

✨ **Modern UI** - Beautiful, responsive chat interface  
🤖 **AI Powered** - Integrated with OpenAI GPT-3.5-turbo  
💬 **Conversation History** - Maintains context across messages  
🔄 **Real-time Communication** - Instant message delivery  
📱 **Fully Responsive** - Works on desktop and mobile devices  
⚡ **Fast & Efficient** - Optimized performance

## Project Structure

```
AI ChatBot Project/
├── frontend/              # React frontend application
│   ├── public/
│   ├── src/
│   │   ├── App.js        # Main React component
│   │   ├── App.css       # Styling
│   │   └── index.js      # Entry point
│   └── package.json
├── backend/              # Express backend server
│   ├── server.js         # Main server file
│   ├── package.json
│   └── .env.example      # Environment variables template
├── README.md            # This file
└── .github/
    └── copilot-instructions.md
```

## Prerequisites

- **Node.js** (v14 or higher)
- **npm** or **yarn**
- **OpenAI API Key** (Get one from https://platform.openai.com)

## Installation & Setup

### 1. Backend Setup

**Prerequisites**: Python 3.8 or higher

```bash
cd backend
pip install -r requirements.txt
```

Create a `.env` file in the backend folder:

```
OPENAI_API_KEY=your_actual_api_key_here
PORT=5000
NODE_ENV=development
```

Replace `your_actual_api_key_here` with your actual OpenAI API key.

### 2. Frontend Setup

```bash
cd frontend
npm install
```

## Running the Application

### Terminal 1 - Start Backend Server

python server.py

````
Or with auto-reload in development:
```bash
uvicorn server:app --reload --port 5000
cd backend
npm start
````

Server will run on `http://localhost:5000`

### Terminal 2 - Start Frontend Application

```bash
cd frontend
npm start
```

Application will open on `http://localhost:3000`

## API Endpoints

### POST `/api/chat`

Send a message and get AI response

- **Body**:
  ```json
  {
    "message": "Your question here",
    "sessionId": "optional-session-id"
  }
  ```
- **Response**:
  ```json
  {
    "reply": "AI response text",
    "sessionId": "session-id"
  }
  ```

### GET `/api/health`

Check if the server is running

- **Response**: `{ "status": "Server is running" }`

### DELETE `/api/chat/history/:sessionId`

Clear conversation history for a session

- **Response**: `{ "message": "Conversation history cleared" }`

## Features Explained

### Conversation Context

The chatbot maintains conversation history for each session, allowing it to understand context and provide more relevant responses.

### Session Management

Each user session is tracked separately, allowing multiple conversations to happen simultaneously.

### Error Handling

Comprehensive error handling with user-friendly messages and detailed logging in development mode.

## Technologies Used

### Frontend

- **React** - UI library
- **Axios** - HTTP client
- **CSS3** - Styling with gradients and animations

### Backend

- **FastAPI** - Modern Python web framework
- **Uvicorn** - ASGI server
- **OpenAI API** - AI model
- **Pydantic** - Data validation
- **python-dotenv** - Environment variables

## Development

To run in development mode with hot reloading:
uvicorn server:app --reload --port 5000

```
FastAPI automatically provides:
- 📚 Interactive API docs at `/docs`
- 📄 Alternative docs at `/redoc`
- 🔄 Auto hot-reload on file changes
cd backend
npm run dev
```

(Requires nodemon to be installed)

### Frontend

```bash
cd frontend
npm start
```

## Troubleshooting

### "Failed to get response" Error

- Verify your OpenAI API key is correct in the `.env` file
- Check that the backend server is running on port 5000
- Ensure you have sufficient API credits on your OpenAI account

### CORS Error

- Make sure the backend is running before starting the frontend
- Check that `CORS` is properly enabled in the backend

### "Module not found" Error

- Run `npm install` in both frontend and backend directories
- Clear node_modules and reinstall if issues persist

## Future Enhancements

- 🔐 User authentication and profiles
- 💾 Persistent chat history with database
- 🎨 Custom themes and personalizations
- 🔊 Voice input/output capabilities
- 📊 Chat analytics and statistics
- 🌍 Multi-language support
- 🧠 Fine-tuned models for specific domains

## License

MIT License - Feel free to use this project for personal or commercial purposes.

## Support

For issues or questions, please check the troubleshooting section or refer to the official documentation:

- [OpenAI Documentation](https://platform.openai.com/docs)
- [React Documentation](https://react.dev)
- [Express Documentation](https://expressjs.com)

---

**Enjoy chatting with your AI assistant! 🚀**
