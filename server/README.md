# Emotion Detection API Server

This is the FastAPI server for the Real-Time Emotion Detection AI Project.

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

## Installation

1. Navigate to the server directory:
   ```bash
   cd server
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   ```

3. Activate the virtual environment:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Server

1. Make sure you're in the `server` directory and your virtual environment is activated.

2. Start the server using uvicorn:
   ```bash
   uvicorn main:app --reload --host 0.0.0.0 --port 8000
   ```

   Or simply:
   ```bash
   python main.py
   ```
   (if you add the uvicorn command to main.py)

3. The server will start on `http://localhost:8000`

4. API documentation will be available at:
   - Swagger UI: `http://localhost:8000/docs`
   - ReDoc: `http://localhost:8000/redoc`

## API Endpoints

### POST `/process-image/`
Processes an image for emotion detection.

**Request:**
- Content-Type: `multipart/form-data`
- Body: Image file (form field name: `file`)

**Response:**
```json
["emotion_name", confidence_percentage]
```

Example:
```json
["sad", 99]
```

## Model Files

The server expects model files to be in the `models/` directory. Make sure all `.keras` model files are present in their respective subdirectories.

## Notes

- The server uses CORS middleware to allow requests from the frontend
- Model files are loaded at startup
- Image processing resizes input to 96x96 pixels
- The server uses threading for parallel emotion detection

