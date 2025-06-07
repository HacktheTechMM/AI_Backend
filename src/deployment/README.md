# AI Backend

This project provides a set of FastAPI-based microservices for AI-powered educational tools, including code testing, quizzes, roadmaps, explanations, and text-to-text chat. Each service is accessible via a REST API endpoint.

## Table of Contents

- [Features & Endpoints](#features--endpoints)
- [Setup & Installation](#setup--installation)
- [API Usage](#api-usage)
- [Dependencies](#dependencies)

---

## Features & Endpoints

### 1. Code Test

- **Endpoint:** `/codetest/invoke`
- **Example Request:**
  ```json
  { "input": { "level": "beginner", "input": "start" } }
  ```
- **Response:**
  - Output: `['output']['content']`

### 2. Text-to-Text Chat

- **Endpoint:** `/chat/`
- **Example Request:**
  ```json
  { "prompt": "Programming ဆိုတာဘာလဲ" }
  ```
- **Response:**
  - Output: `['response']['response']`

### 3. Roadmap Generation

- **Endpoint:** `/roadmap/invoke`
- **Example Request:**
  ```json
  {
    "input": { "input": "I want to learn AI Engineer now I am beginner level." }
  }
  ```
- **Response:**
  - Output: `['output']['content']`

### 4. Explain Details

- **Endpoint:** `/steps/invoke`
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

- **Endpoint:** `/quiz/invoke`
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
