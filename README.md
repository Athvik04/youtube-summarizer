Gemini-Powered YouTube Summarizer
Summarize YouTube videos instantly using Google's Gemini AI! This web app allows users to input a YouTube video URL and get an AI-generated summary using Google's powerful GenAI models.

🚀 Features
🔗 Input any YouTube video URL

🧠 Summarization powered by Gemini (via Google GenAI SDK)

🌐 Flask-based web application

☁️ Deployed on Google Cloud Run

✨ Optional additional prompts to customize summaries

🧰 Tech Stack
Frontend: HTML, CSS

Backend: Python, Flask

AI Integration: Gemini via google-genai SDK

Deployment: Google Cloud Run

📝 Prerequisites
A Google Cloud project with billing enabled

Python installed (for local testing)

Basic knowledge of Python, Flask, and HTML

Familiarity with Google Cloud Shell and Vertex AI

📦 Installation
Clone or create the app using Google Cloud Shell

Use the Cloud Code plugin to generate a new Python Flask app

Enable APIs

bash
Copy
Edit
gcloud services enable aiplatform.googleapis.com \
                       run.googleapis.com \
                       cloudbuild.googleapis.com \
                       cloudresourcemanager.googleapis.com
Set project

bash
Copy
Edit
gcloud config set project YOUR_PROJECT_ID
Install dependencies

bash
Copy
Edit
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
🔧 Configuration
Add your Google Cloud Project ID in app.py under PROJECT_ID

Ensure your environment is authorized to use Gemini models through Vertex AI

🖥️ Running Locally
Run the app using:

bash
Copy
Edit
python app.py
Preview the app in Cloud Shell using port 8080.

☁️ Deploying to Cloud Run
From the project root directory:

bash
Copy
Edit
gcloud run deploy --source .
Give your service a name (e.g., youtube-summarizer)

Choose region: us-central1

Allow unauthenticated access for public use

You’ll receive a public URL to access your deployed app!

💡 Bonus Challenge
Want more? Try modifying the app to:

Upload local video files instead of YouTube links

Add support for multiple languages

Store summaries for later access

🧹 Clean Up
To avoid unnecessary charges:

Delete your Cloud Run service from the console

Or delete the entire project via the Manage Resources page in GCP
