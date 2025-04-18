# 🩺 Virtual Diabetologist

**Virtual Diabetologist** is an AI-powered healthcare web application that provides diabetes prediction, diabetic retinopathy detection, and an intelligent chatbot for personalized support. Built with **Flask**, **Node.js**, **React**, and **machine learning models**, it offers a comprehensive solution for diabetes management and can be integrated into external systems via APIs.

---

## 🚀 Features

- 🔍 **Diabetes Prediction**  
  Predicts diabetes likelihood based on inputs like age, BMI, glucose, heart disease, and more.

- 🖼️ **Retinopathy Detection**  
  Uses CNN-based image analysis to detect diabetic retinopathy from retinal scans.

- 🤖 **AI Chatbot**  
  Offers personalized, context-aware health advice using LLMs (via LangChain).

- 🧠 **Context Management**  
  Dynamically updates patient data for more relevant chatbot responses.

- 🛠️ **API Integration**  
  Built-in endpoints for third-party use cases — perfect for external health platforms.

- 📄 **PDF Report Generation**  
  Converts chat history and health insights into downloadable AI diagnosis reports.

---

## 🧰 Tech Stack

### Backend
- **Flask (Python)** – ML model serving, chatbot logic, and API endpoints  
- **Node.js** – Middleware for managing requests, file uploads, and security  
- **LangChain** – Orchestrates LLMs, embeddings, and memory for chatbot intelligence  
- **Machine Learning Models**:  
  - Pre-trained diabetes prediction classifier  
  - CNN-based diabetic retinopathy detector (image-based)

### Frontend
- **React** – Frontend UI components  
- **Tailwind CSS** – Clean, responsive styling  
- **Font Awesome** – Iconography and visual cues

---

## ⚙️ Installation Guide

### ✅ Prerequisites
Make sure the following are installed:
- Python 3.7+
- Node.js (with npm or yarn)
- pip (Python package installer)

---

### 🔧 Backend Setup (Flask)
```bash
git clone https://github.com/yourusername/virtual-diabetologist.git
cd virtual-diabetologist
pip install -r requirements.txt
python server.py

 ```

### 💻 Frontend (React)
1. Navigate to the `frontend` directory:
    ```bash
    cd frontend
   ```

2. Install JavaScript dependencies:
    ```bash
    npm install
    ```

3. Start the React development server:
    ```bash
    npm start
    ```

### 🌐 Middleware (Node.js)
1. Navigate to the `middleware` directory:
    ```bash
    cd middleware
    ```

2. Install Node.js dependencies:
    ```bash
    npm install
    ```

3. Start the Node.js server:
    ```bash
    node server.js
    ```

## 📡 API Endpoints

### 🔍 Diabetes Prediction
- **POST** `/predict`
    - Request Body:
      ```json
      {
        "gender": "Male",
        "age": 45,
        "hypertension": 0,
        "heart_disease": 1,
        "smoking_history": "never",
        "bmi": 28.7,
        "HbA1c_level": 6.5,
        "blood_glucose_level": 120
      }
      ```
    - Response:
      ```json
      {
        "predictions": ["predicted to have diabetes"]
      }
      ```

### 🖼️ Retinopathy Detection
- **POST** `/detect`
    - Request Body:
      ```json
      {
        "image": "base64-encoded-image-string"
      }
      ```
    - Response:
      ```json
      {
        "result": "You have diabetic retinopathy."
      }
      ```

### 🤖 Chatbot
- **POST** `/ask`
    - Request Body:
      ```json
      {
        "prompt": "What are the symptoms of diabetes?"
      }
      ```
    - Response:
      ```json
      {
        "response": "Common symptoms of diabetes include increased thirst, frequent urination, extreme hunger, etc."
      }
      ```

### 🧠 Update User Context
- **POST** `/update-context`
    - Request Body:
      ```json
      {
        "bloodSugar": 180,
        "heartRate": 72,
        "age": 45,
        "glucoseLevels": 200,
        "hb1ac": 7.2
      }
      ```
    - Response:
      ```json
      {
        "message": "User data context updated successfully"
      }
      ```

## 🎥 Demo  
[Watch Demo Video on YouTube](https://shorturl.at/myew2)

## 📄 License

This project is licensed under the MIT License.

