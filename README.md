# 📖 Life Logger AI: Daily Journal Generator

**Life Logger AI** is an automated journaling system built with **n8n**. It captures your daily life by analyzing photos from Google Drive, checking your Google Calendar, and fetching local weather data to generate a cohesive, first-person narrative stored in Google Docs.

## 🛠 Features

- **Vision-to-Text:** Uses Gemini 2.5 Flash to analyze photos for emotions, activities, and locations.
- **Contextual Awareness:** Integrates Google Calendar (schedules) and OpenWeatherMap (atmosphere).
- **Vector Memory (RAG):** Stores photo descriptions in a PostgreSQL Vector database for intelligent retrieval.
- **Automated Delivery:** Formats and appends entries to a Google Doc.

---

## 📋 Prerequisites

- **Docker & Docker Compose** installed.
- **Google Cloud Project** with Drive, Docs, and Calendar APIs enabled.
- **API Keys:** Gemini (Google AI Studio) and OpenWeatherMap.

---

## ⚙️ Environment Configuration

1. Copy the `.env.example` to a new file named `.env`.
2. Update the values with your actual API keys and database credentials.

### Key Variables:

| Variable                 | Description                              |
| :----------------------- | :--------------------------------------- |
| `OPENWEATHERMAP_API_KEY` | Used for fetching local weather.         |
| `POSTGRES_PASSWORD`      | Secure password for the vector database. |
| `TELEGRAM_BOT_TOKEN`     | Used for daily status notifications.     |
| `GOOGLE_CLIENT_ID`       | OAuth2 ID for Google services.           |

---

## 🚀 Getting Started

### 1. Launch the Stack

Run the following command to start n8n:

```bash
docker-compose up -d
```
