# Cattle Breed AI

AI-powered web application for identifying **Indian cattle and buffalo breeds from images** using deep learning.

The project combines a **React + Vite frontend** with a **Flask + PyTorch backend** to provide breed predictions along with confidence scores and breed information.

## Features

* Cattle & buffalo breed identification
* Deep-learning based image classification
* Top-3 breed predictions with confidence scores
* Breed information and characteristics
* Image preview before prediction
* JPG, JPEG, PNG and WEBP support
* Upload limit of 10 MB
* GPU support with CPU fallback
* Separate frontend and backend deployment
* API health-check endpoint

## How It Works

```text
Animal Image
     ↓
React Frontend
     ↓
Flask API
     ↓
Image Preprocessing
     ↓
PyTorch Model
     ↓
Class Probabilities
     ↓
Top-3 Predictions
     ↓
Breed Information
```

## Tech Stack

| Technology       | Purpose             |
| ---------------- | ------------------- |
| React            | Frontend            |
| Vite             | Frontend tooling    |
| JavaScript / JSX | UI logic            |
| CSS              | Styling             |
| Flask            | Backend API         |
| PyTorch          | Deep learning       |
| Pillow           | Image processing    |
| Gunicorn         | Production server   |
| Vercel           | Frontend deployment |
| Render           | Backend deployment  |

## Setup & Running Locally

### Prerequisites
- Python 3.11
- Node.js 18+ and npm
- Git

### 1. Clone the repository
```bash
git clone https://github.com/bharviT/Cattle_Breed.git
cd Cattle_Breed
```

### 2. Backend setup (Flask + PyTorch)
```bash
pip install -r requirements.txt
python app.py
```
The backend will start on `http://localhost:5000`. On first run, it downloads the trained model weights automatically from Hugging Face (`ujjwal75/indian-bovine-breeds-model`), so an internet connection is required the first time.

### 3. Frontend setup (React + Vite)
In a separate terminal:
```bash
npm install
npm run dev
```
The frontend will start on `http://localhost:5173` and is pre-configured (via Vite's dev proxy) to talk to the local backend.

### 4. Environment variables
Copy `.env.example` to `.env` if deploying the frontend separately (e.g. to Vercel):
```bash
cp .env.example .env
```
Set `VITE_API_BASE_URL` to your deployed backend's URL. For local development, leave it empty.

### 5. Usage
Open `http://localhost:5173` in a browser, upload a cattle or buffalo image (JPG/PNG/WEBP, up to 10 MB), and view the top-3 breed predictions with confidence scores.

## Project Structure

```text
cattle-breed-ai-fixed/
│
├── Backend_new/
│   └── breedai_public_backend/
│       ├── backend.py
│       ├── predict_FINAL_FIXED.py
│       ├── requirements.txt
│       └── render.yaml
│
├── src/
│   ├── App.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
│
├── public/
├── app.py
├── predict.py
├── predict_FINAL_FIXED.py
├── package.json
├── vite.config.js
├── render.yaml
├── requirements.txt
└── README.md
```

## Deployment

The project uses a split deployment architecture:

```text
┌───────────────┐
│    Vercel     │
│ React + Vite  │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│    Render     │
│ Flask + PyTorch│
└───────────────┘
```

## Limitations

Prediction quality may vary depending on:

* Image quality
* Lighting
* Camera angle
* Background
* Animal visibility
* Similarity between breeds

The confidence score represents the model's prediction probability and should not be considered a guaranteed identification.

## Future Scope

* [ ] Support more breeds
* [ ] Improve difficult-image recognition
* [ ] Multi-animal detection
* [ ] Explainable AI
* [ ] Breed comparison
* [ ] Prediction history
* [ ] Mobile optimization
* [ ] Multilingual support

## Contributing

Contributions and suggestions are welcome.


---

### Cattle Breed AI

**Computer Vision • Deep Learning • Agriculture • Full-Stack Development**
