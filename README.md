# AI Email Reply Generator

## About the Project

This project is an AI-powered email reply generator built using **Spring Boot**, **React**, and the **Google Gemini API**.

The idea behind the project is simple: while replying to an email in Gmail, users can click an **AI Reply** button added by a Chrome Extension. The email content is sent to a Spring Boot backend, which communicates with the Gemini API to generate a context-aware reply. The generated response is then inserted directly into the Gmail compose window.

Apart from the Chrome Extension, the project also includes a React frontend that can be used independently to test and generate replies for texts other than email.

---

## Features

* Generate AI-powered email replies
* Chrome Extension integrated with Gmail
* Multiple reply tones (Professional, Casual and Friendly)
* Spring Boot REST API backend
* React frontend built with Material UI
* Copy generated replies to clipboard
* Secure API key management using environment variables

---

## Tech Stack

### Backend

* Java
* Spring Boot
* Spring Web
* WebClient
* Maven

### Frontend

* React
* Vite
* Material UI
* Axios

### Chrome Extension

* JavaScript
* Manifest V3
* MutationObserver
* DOM Manipulation

### AI

* Google Gemini API

---

## Project Structure

```
AI-Email-Reply-Generator
│
├── email-writer-sb        # Spring Boot Backend
├── email-writer-react     # React Frontend
└── email-writer-ext       # Chrome Extension
```

---

## How it Works

1. User opens an email in Gmail.
2. Clicking **Reply** displays an **AI Reply** button added by the Chrome Extension.
3. The extension extracts the email content.
4. A request is sent to the Spring Boot backend.
5. The backend forwards the prompt to the Gemini API.
6. Gemini generates a reply.
7. The generated response is automatically inserted into the Gmail compose box.

---

## Running the Project

### Backend

```bash
cd email-writer-sb
./mvnw spring-boot:run
```

Runs on:

```
http://localhost:8085
```

---

### Frontend

```bash
cd email-writer-react
npm install
npm run dev
```

Runs on:

```
http://localhost:5173
```

---

### Chrome Extension

* Open `chrome://extensions`
* Enable **Developer Mode**
* Click **Load unpacked**
* Select the `email-writer-ext` folder

---

## Environment Variables

Create an environment variable named:

```
GEMINI_KEY=YOUR_API_KEY
```

The API key is intentionally not included in this repository.

---

## Future Improvements

Some features I'd like to add in the future:

* More reply tone options
* Support for different AI models
* Email summarization
* Reply history
* User authentication
* Deployment with Docker

---

## Screenshots

Screenshots and a demo GIF will be added after deployment.
