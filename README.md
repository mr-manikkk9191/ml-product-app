# 🛒 AI Product Recommendation System

An intelligent full-stack web application that helps users discover products using AI-driven recommendations, vector search, and computer vision.

## 🚀 Overview

The AI Product Recommendation System is an intelligent web-based platform that helps users discover products similar to their interests using AI-driven recommendations. The system analyzes product embeddings using Pinecone & OpenAI and presents results with visualization dashboards and a Computer Vision module.

## ✨ Features

* **🤖 AI-Powered Search:** Find similar products using natural language text queries.
* **🧠 Vector Recommendations:** Utilizes **Pinecone** and **OpenAI** embeddings for high-speed semantic search.
* **🎨 Modern Dark-Themed UI:** A clean, responsive, and visually appealing interface.

* **📊 Analytics Dashboard:**
    * **Top Categories:** Visualizes the most common product categories.
    * **Top Brands:** Shows the most popular brands in the dataset.
    * **Price Histogram:** Displays the price distribution across all products.
    * **Scatter Plot:** Analyzes Price vs. Title Length.
    * **Product Gallery:** A browseable gallery of all products.

* **🖼️ Zero-Shot Computer Vision:**
    * Classify product images without prior model training.
    * Users can upload an image or paste an online image URL.
    * The AI predicts the product category and a confidence score (e.g., `{"label": "chair", "confidence": 92%}`).

## 🛠️ Tech Stack

| Category | Tools Used |
| :--- | :--- |
| **Backend** | FastAPI, LangChain, OpenAI, Pinecone |
| **Frontend** | React (Vite), Axios, Recharts |
| **ML / CV** | OpenAI Zero-Shot Vision |

## 🗂️ Project Structure

Here is the raw Markdown content. You can copy the text below and save it as a `README.md` file.

```markdown
# 🛒 AI Product Recommendation System

An intelligent full-stack web application that helps users discover products using AI-driven recommendations, vector search, and computer vision.

## 🚀 Overview

The AI Product Recommendation System is an intelligent web-based platform that helps users discover products similar to their interests using AI-driven recommendations. The system analyzes product embeddings using Pinecone & OpenAI and presents results with visualization dashboards and a Computer Vision module.

## ✨ Features

* **🤖 AI-Powered Search:** Find similar products using natural language text queries.
* **🧠 Vector Recommendations:** Utilizes **Pinecone** and **OpenAI** embeddings for high-speed semantic search.
* **🎨 Modern Dark-Themed UI:** A clean, responsive, and visually appealing interface.

* **📊 Analytics Dashboard:**
    * **Top Categories:** Visualizes the most common product categories.
    * **Top Brands:** Shows the most popular brands in the dataset.
    * **Price Histogram:** Displays the price distribution across all products.
    * **Scatter Plot:** Analyzes Price vs. Title Length.
    * **Product Gallery:** A browseable gallery of all products.

* **🖼️ Zero-Shot Computer Vision:**
    * Classify product images without prior model training.
    * Users can upload an image or paste an online image URL.
    * The AI predicts the product category and a confidence score (e.g., `{"label": "chair", "confidence": 92%}`).

## 🛠️ Tech Stack

| Category | Tools Used |
| :--- | :--- |
| **Backend** | FastAPI, LangChain, OpenAI, Pinecone |
| **Frontend** | React (Vite), Axios, Recharts |
| **ML / CV** | OpenAI Zero-Shot Vision |

## 🗂️ Project Structure
ml-product-app/
│
├── Backend/              \# FastAPI Backend (AI Logic + API Endpoints)
│   ├── main.py
│   ├── data/             \# Dataset CSVs (intern\_data\_ikarus.csv)
│   ├── models/           \# Embedding Models (if applicable)
│   └── requirements.txt
│
├── frontend/             \# React Frontend (Vite + Recharts)
│   ├── src/
│   ├── pages/
│   ├── api/
│   └── package.json
│
└── README.md             \# Project Documentation

````

## ⚙️ Installation Guide

### ✅ Prerequisites

* Python 3.10+
* Node.js & npm
* OpenAI API Key
* Pinecone API Key

---

### 🖥️ Backend Setup (FastAPI)

1.  **Navigate to the backend directory:**
    ```bash
    cd Backend
    ```
2.  **Create and activate a virtual environment:**
    ```bash
    # Windows
    python -m venv myenv
    myenv\Scripts\activate
    
    # macOS / Linux
    python3 -m venv myenv
    source myenv/bin/activate
    ```
3.  **Install required packages:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Create a `.env` file:**
    Create a file named `.env` inside the `Backend/` directory and add your API keys:
    ```ini
    OPENAI_API_KEY=your_openai_key
    PINECONE_API_KEY=your_pinecone_key
    PINECONE_INDEX=ml-project1
    PINECONE_REGION=us-east-1
    ```
5.  **Run the Backend Server:**
    ```bash
    uvicorn Backend.main:app --reload --port 8000
    ```
    📡 The API will be running at `http://localhost:8000`

---

### 💻 Frontend Setup (React + Vite)

1.  **Navigate to the frontend directory (in a new terminal):**
    ```bash
    cd frontend
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Run the development server:**
    ```bash
    npm run dev
    ```
    🌍 The app will open at `http://localhost:5173`

## 📌 API Endpoints (Backend)

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/recommend` | `POST` | Get AI product recommendations based on a text query. |
| `/group` | `POST` | Cluster and return similar products. |
| `/analytics` | `GET` | Retrieve aggregated data for the analytics dashboard. |
| `/classify-image-file` | `POST` | Classify an uploaded product image file. |
| `/classify-image-url` | `POST` | Classify a product image from a provided URL. |

## 🚀 Deployment

The project is designed to be deployed as two separate services, with plans for full hosting.

| Platform | Usage |
| :--- | :--- |
| **Render** | Host FastAPI Backend |
| **Vercel** | Host React Frontend |
| **Railway/Heroku** | Complete Stack Hosting |

## 🔮 Future Enhancements

* **🧑‍💼 User Accounts & Personalization:** Allow users to create accounts for saved preferences and personalized recommendation history.
* **💾 Database Integration:** Add a persistent database (e.g., PostgreSQL or MongoDB) to manage user data.
* **☁️ Full Deployment:** Complete the deployment pipeline to Render/Vercel.
* **🎯 Improved Filtering & Sorting:** Add advanced options to filter and sort recommendation results.

## 👤 Author

**Manik Thakur**

This project showcases AI integration with real-world eCommerce solutions using vector search, machine learning, and data analytics.
````