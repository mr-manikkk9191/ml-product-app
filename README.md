🛒 AI Product Recommendation System
Author: Manik Thakur
Project Type: Full-Stack AI/ML Web Application
Technologies: FastAPI, React (Vite), Pinecone, OpenAI, Machine Learning, Computer Vision


🚀 Overview
The AI Product Recommendation System is an intelligent web-based platform that helps users discover products similar to their interests using AI-driven recommendations. The system analyzes product embeddings using Pinecone & OpenAI and presents results with visualization dashboards and a Computer Vision module.


Users can:
🔎 Search products using natural language queries

🤖 Receive AI-based similar product recommendations

📊 View dataset analytics (brands, categories, price insights)

🖼️ Classify product images using Zero-Shot Computer Vision

🎨 Experience a modern Dark-Themed UI


🗂️ Project Structure
ml-product-app/
│
├── Backend/              # FastAPI Backend (AI Logic + API Endpoints)
│   ├── main.py
│   ├── data/             # Dataset CSVs (intern_data_ikarus.csv)
│   ├── models/           # Embedding Models (if applicable)
│   └── requirements.txt
│
├── frontend/             # React Frontend (Vite + Recharts)
│   ├── src/
│   ├── pages/
│   ├── api/
│   └── package.json
│
└── README.md             # Project Documentation


🔍 Core Features
Feature	Description
🔍 AI Search	Find similar products via text query
🧠 Vector Recommendations	Pinecone + OpenAI embeddings
📊 Data Analytics	Top brands, categories, price distribution
🖼️ Zero-Shot Vision	Classify uploaded/pasted images
🎨 Dark Theme UI	Modern and clean interface


🧠 Technologies & Tools
Category	Tools Used
Backend	FastAPI, LangChain, OpenAI, Pinecone
Frontend	React (Vite), Axios, Recharts
ML / CV	OpenAI Zero-Shot Vision
Deployment	GitHub, Render/Vercel (planned)


⚙️ Installation Guide
✅ Prerequisites

Python 3.10+
Node.js & npm
OpenAI & Pinecone API Keys


🖥️ Backend Setup (FastAPI)
# Step 1: Navigate to backend
cd Backend
# Step 2: Create a virtual environment
python -m venv myenv
myenv\Scripts\activate
# Step 3: Install required packages
pip install -r requirements.txt




🗝️ Create .env file inside Backend/
OPENAI_API_KEY=your_openai_key
PINECONE_API_KEY=your_pinecone_key
PINECONE_INDEX=ml-project1
PINECONE_REGION=us-east-1



▶ Run Backend Server
uvicorn Backend.main:app --reload --port 8000
📡 API will run at → http://localhost:8000




💻 Frontend Setup (React + Vite)
# Step 1: Navigate to frontend
cd frontend
# Step 2: Install dependencies
npm install
# Step 3: Run development server
npm run dev

🌍 App will open at → http://localhost:5173



🤖 Zero-Shot Computer Vision

✅ Upload an image or paste an online image URL.
✅ AI predicts product category without training.

Example:
Upload: chair image
Output: "label": chair, "confidence": 92%



📊 Analytics Dashboard

Includes:
📁 Top Categories
🏷️ Top Brands
📉 Price Histogram
🧪 Scatter Plot (Price vs Title Length)
🖼️ Product Gallery



📌 API Endpoints (Backend)
Endpoint	Method	Description
/recommend	POST	AI product recommendations
/group	POST	Clustering similar products
/analytics	GET	Dataset analytics
/classify-image-file	POST	Classify uploaded image
/classify-image-url	POST	Classify image URL



🚀 Future Enhancements

🧑‍💼 User Accounts & Personalization
💾 Database Integration (PostgreSQL / MongoDB)
☁️ Deployment (Render/Vercel)
🎯 Improved filtering & sorting



🧾 Deployment Options
Platform	Usage
Render	Host FastAPI Backend
Vercel	Host React Frontend
Railway/Heroku	Complete Stack Hosting



👤 Author

Manik Thakur
This project showcases AI integration with real-world eCommerce solutions using vector search, ML, and analytics.