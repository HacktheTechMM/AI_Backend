# AI Backend

<<<<<<< HEAD
This project provides a set of FastAPI-based microservices for AI-powered educational tools, including code testing, quizzes, roadmaps, explanations, and text-to-text chat. Each service is accessible via a REST API endpoint.
=======
In order to test "code_test" : https://ai-backend-12.onrender.com/formatcode/invoke
{"input":{
"input": "advanced code test question"
}}
take the output: ["output"]["content"]
>>>>>>> 3f7168c51a6200be14864a052ce0cea1b54eeae6

## Table of Contents

- [Features & Endpoints](#features--endpoints)
- [Setup & Installation](#setup--installation)
- [API Usage](#api-usage)
- [Dependencies](#dependencies)

---

<<<<<<< HEAD
## Features & Endpoints
=======
In order to test "quiz" : https://quizzz-cver.onrender.com/quiz/invoke
{"input":{"input": "{Beginner Python}"}}
take the output: ['output']['content']
>>>>>>> 3f7168c51a6200be14864a052ce0cea1b54eeae6

### 1. Code Test

- **Endpoint:** `https://ai-backend-12.onrender.com/formatcode/invoke`
- **Example Request:**
  ```json
  { "input": { "level": "beginner", "input": "start" } }
  ```
- **Response:**
  - Output: `['output']['content']`

### 2. Text-to-Text Chat

- **Endpoint:** `https://ai-backend-1-n8mt.onrender.com/chat/`
- **Example Request:**
  ```json
  { "prompt": "Programming ဆိုတာဘာလဲ" }
  ```
- **Response:**
  - Output: `['response']['response']`

### 3. Roadmap Generation

- **Endpoint:** ` https://ai-backend-3-3gjd.onrender.com/roadmap/invoke/`
- **Example Request:**
  ```json
  {
    "input": { "input": "I want to learn AI Engineer now I am beginner level." }
  }
  ```
- **Response:**
  - Output: `['output']['content']`

### 4. Explain Details

- **Endpoint:** `https://ai-backend-9.onrender.com/steps/invoke/`
- **Example Request:**
  ```json
  {
    "input": {
      "input": "{\"title\": \"Introduction to AI and Machine Learning\", \"description\": \"Learn the basics of AI, ML, and DL. Understand the types of AI, ML, and DL.\", What is the Neural Network?"
    }
  }
  ```
- **Response:**
  - Output: `['output']['content']`

### 5. Quiz Generation

- **Endpoint:** `https://quizzz-cver.onrender.com/quiz/invoke`
- **Example Request:**
  ```json
  { "input": { "input": "{Beginner Python}" } }
  ```
- **Response:**
  - Output: `['output']['content']`

---

## Setup & Installation

1. **Clone the repository**
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Set up environment variables:**
   - Create a `.env` file with your required API keys and settings.
4. **Run a service:**
   ```bash
   uvicorn <script_name>:app --reload
   ```
   Replace `<script_name>` with the desired service, e.g., `roadmap`, `quiz`, etc.

---

## Dependencies

- langchain-community
- langchain-groq
- langgraph
- langserve
- dotenv
- fastapi
- uvicorn
- sse_starlette
- langchain_google_genai

---

## Notes

- Each service runs independently. You can deploy them separately or together as needed.
- For production, configure proper environment variables and secure your API keys.
