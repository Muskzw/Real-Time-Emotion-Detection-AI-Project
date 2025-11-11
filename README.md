# Real-Time Emotion Detection AI Project

A real-time emotion detection system using AI/ML models to analyze facial expressions from webcam input. Features a modern web frontend and a FastAPI backend server.

## Project Structure

- `frontend/`: Client-side code including HTML, CSS, JavaScript, and static assets
  - `index.html`: Main application interface
  - `src/`: Source code (JS, CSS, components)
  - `assets/`: Images, icons, and other static assets
  - `public/`: Public static files

- `server/`: API server implementation
  - `main.py`: FastAPI application with emotion detection endpoints
  - `models/`: Trained ML models for emotion classification
  - `requirements.txt`: Python dependencies
  - `README.md`: Server setup and running instructions

- `notebooks/`: Jupyter notebooks for data analysis, model training, and experimentation

- `docs/`: Documentation, notes, and diagrams
- `tests/`: Test files

## Quick Start

### Frontend
1. Open `frontend/index.html` in a web browser, or serve it using a local HTTP server
2. The frontend connects to the API server at `http://localhost:8000` by default

### Backend Server
1. Navigate to the `server/` directory
2. Install dependencies: `pip install -r requirements.txt`
3. Run the server: `python main.py` or `uvicorn main:app --reload`
4. See `server/README.md` for detailed setup instructions

## Features

- Real-time emotion detection from webcam feed
- Support for 8 emotions: Happy, Neutral, Sad, Angry, Surprised, Disgusted, Contempt, Fear
- Analytics dashboard with charts and statistics
- Session recording capabilities
- Modern, responsive UI

## License
MIT


