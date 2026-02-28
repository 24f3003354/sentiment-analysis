
# Sentiment Analysis System

A FastAPI-based sentiment analysis service that leverages OpenAI's GPT-4o Mini model to analyze the sentiment of user comments.

## Features

- Real-time sentiment analysis using GPT-4o Mini
- RESTful API built with FastAPI
- Simple and intuitive endpoint design
- vercel-ready deployment

## Installation

```bash
pip install fastapi uvicorn openai python-dotenv
```

## Configuration

Copy the `.env.example` file to `.env` and set your OpenAI API key:

```bash
cp .env.example .env
```

Then, edit the `.env` file to include your OpenAI API key:

```bash
OPENAI_API_KEY=your_openai_api_key_here
```

## Usage

Start the server:

```bash
uvicorn api.index:app --reload
```

### API Endpoint

**POST** `/comment`

Request body:
```json
{
    "text": "I love this product!"
}
```

Response:
```json
{
    "sentiment": "positive",
    "rating": 5
}
```

## Requirements

- Python 3.8+
- OpenAI API key
- FastAPI
- Uvicorn

## License

MIT
