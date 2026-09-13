🎙️ Vaani AI

AI-Powered Multilingual Learning Platform for Language Accessibility

«Vaani AI is a multilingual, voice-enabled educational platform designed to make digital learning more accessible for students who face language and connectivity barriers — with a particular focus on Santali, Hindi, and English.»

---

🚀 Overview

Many students in underserved and tribal communities face two major barriers to digital education:

- 🌐 Educational content is predominantly available in languages they may not be comfortable with.
- 📶 Reliable internet connectivity is not always available.

Vaani AI addresses these challenges by combining AI-powered speech and translation technologies with an offline-first Progressive Web App (PWA) architecture.

The platform provides localized educational content, multilingual interaction, voice input/output, an offline dictionary, flashcards, quizzes, and NCERT-aligned learning resources.

---

🎯 Problem Statement

Digital education platforms often assume:

1. Students understand English or another dominant language.
2. Students have continuous internet connectivity.
3. Students can comfortably interact using text and keyboards.

These assumptions create accessibility barriers for students from linguistically diverse and low-connectivity communities.

Vaani AI aims to bridge this gap by bringing language accessibility + voice interaction + offline learning into a single platform.

---

💡 Our Solution

Vaani AI creates a localized learning environment where students can:

- 📚 Access curriculum-aligned educational content
- 🌍 Switch between English, Hindi, and Santali
- 🎤 Interact using voice input
- 🔊 Listen to generated responses using text-to-speech
- 📖 Use a Santali dictionary without an internet connection
- 🧠 Practice through flashcards and quizzes
- 📱 Install and use the platform as a PWA
- ⚡ Continue accessing cached learning resources even when connectivity is unavailable

---

✨ Key Features

🌐 Multilingual Interface

The application supports dynamic localization across:

- 🇬🇧 English
- 🇮🇳 Hindi
- 🟢 Santali

The custom internationalization system dynamically updates interface content without requiring a page reload.

---

🎤 Speech-to-Text

Vaani AI supports voice-based interaction using an Indic Conformer speech recognition model.

Flow:

User speaks
     ↓
Audio captured by browser
     ↓
Audio sent to backend
     ↓
Indic Conformer
     ↓
Transcribed text
     ↓
Displayed in application

---

🔊 Text-to-Speech

Generated responses can be converted into natural-sounding audio using Indic Parler-TTS.

Generated Text
      ↓
TTS Backend Router
      ↓
Indic Parler-TTS
      ↓
Audio Blob
      ↓
HTML5 Audio Player
      ↓
User hears response

---

🌍 AI-Powered Translation

Live translation requests are handled through a backend translation pipeline using Sarvam AI.

Static interface translations use locally stored language mappings, while live translation requests can be routed through the backend.

This hybrid approach reduces unnecessary network requests for frequently used interface content.

---

📖 Offline Santali Dictionary

One of Vaani AI's important accessibility features is its offline dictionary.

The dictionary uses locally available language data and can operate without an active internet connection.

User searches word
       ↓
Local dictionary
       ↓
Fuzzy search
       ↓
Matching Santali result

---

📚 NCERT-Aligned Learning Content

The platform contains 100+ mapped NCERT Class 1–5 chapters across subjects including:

- Mathematics
- English
- Environmental Studies

Educational content is organized into interactive learning modules.

---

🧠 Interactive Practice

Students can reinforce concepts through:

- 🃏 Interactive flashcards
- ❓ Quizzes
- 📖 Chapter-based practice
- ✅ Automatic answer validation

The practice engine uses structured curriculum data to dynamically generate learning activities.

---

📱 Progressive Web App

Vaani AI follows an offline-first PWA architecture.

The Service Worker caches the core application so that:

- The application shell can load offline.
- Core navigation remains available.
- The Santali dictionary remains usable offline.
- Cached resources can be accessed without repeatedly downloading them.

---

🏗️ System Architecture

                       ┌─────────────────────┐
                       │      User           │
                       │  Student / Learner  │
                       └──────────┬──────────┘
                                  │
                    Text / Voice / Interaction
                                  │
                                  ▼
                       ┌─────────────────────┐
                       │   Vaani AI PWA      │
                       │                     │
                       │ HTML / JS / CSS     │
                       │ i18n / UI / PWA     │
                       └──────────┬──────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
                    ▼                           ▼
           ┌────────────────┐          ┌────────────────┐
           │ Offline Layer  │          │ Backend Server │
           │                │          │                │
           │ Dictionary     │          │ Python Proxy   │
           │ NCERT Data     │          │                │
           │ Flashcards     │          │ API Routing    │
           │ Quizzes        │          │                │
           └────────────────┘          └───────┬────────┘
                                               │
                             ┌─────────────────┼─────────────────┐
                             │                 │                 │
                             ▼                 ▼                 ▼
                         Sarvam AI      Indic Conformer   Indic Parler-TTS
                         Translation          STT               TTS

---

🛠️ Technology Stack

Frontend

- HTML5
- CSS3
- JavaScript
- Progressive Web App (PWA)
- Service Workers
- LocalStorage
- Client-side JSON data

Backend

- Python
- Lightweight HTTP proxy server
- REST/API communication

AI / ML

Capability| Technology
Translation| Sarvam AI
Speech-to-Text| Indic Conformer
Text-to-Speech| Indic Parler-TTS

Data & Offline Technologies

- JavaScript/JSON curriculum datasets
- LocalStorage
- Service Worker caching
- Offline dictionary
- Client-side content delivery

---

🔄 How Vaani AI Works

1. Text Interaction

User Input
    ↓
Vaani AI Interface
    ↓
Local Dictionary / Translation Pipeline
    ↓
Processed Response
    ↓
User

2. Voice Interaction

Voice Input
    ↓
Browser Audio Capture
    ↓
Python Backend
    ↓
Indic Conformer
    ↓
Text
    ↓
AI / Translation Processing
    ↓
Response
    ↓
Indic Parler-TTS
    ↓
Audio Output

---

📴 Offline vs Online

Vaani AI uses a hybrid architecture rather than treating offline functionality as an afterthought.

Works Offline

✅ PWA application shell
✅ Core navigation
✅ Santali offline dictionary
✅ Locally stored curriculum resources
✅ Flashcards and quizzes
✅ Locally cached resources

Requires Internet

🌐 Live AI translation
🎤 Backend-based speech recognition
🔊 AI-generated TTS
🤖 Other AI-powered real-time interactions

This architecture allows the application to remain useful even when network connectivity is limited.

---

🔐 Privacy & Accessibility

Vaani AI does not require traditional user authentication for accessing the learning platform.

Local learning progress can be maintained using browser storage, reducing dependency on a centralized database.

The platform is designed around:

- Low-friction access
- Multilingual interaction
- Voice accessibility
- Low-connectivity environments
- Mobile-first usage

---

📊 What We Built

The current prototype demonstrates:

- ✅ English / Hindi / Santali localization
- ✅ 100+ NCERT Class 1–5 chapter mappings
- ✅ Interactive flashcards
- ✅ Quiz-based practice
- ✅ Santali offline dictionary
- ✅ Voice input pipeline
- ✅ AI translation pipeline
- ✅ Text-to-speech pipeline
- ✅ PWA offline architecture
- ✅ Local progress tracking
- ✅ Responsive web interface

---

🔮 Future Roadmap

Phase 1 — Current Prototype

- [x] Multilingual UI
- [x] Santali dictionary
- [x] NCERT learning content
- [x] Flashcards
- [x] Quizzes
- [x] PWA architecture
- [x] Voice input
- [x] Translation
- [x] Text-to-speech

Phase 2 — Advanced AI Tutor

- [ ] Real-time conversational voice tutor
- [ ] Personalized learning paths
- [ ] AI-generated explanations
- [ ] Adaptive difficulty
- [ ] Student performance analytics

Phase 3 — Deeper Offline AI

- [ ] Fully offline speech recognition
- [ ] Fully offline translation
- [ ] Browser-side AI models using WebAssembly
- [ ] Expanded low-resource language support

Phase 4 — Scale

- [ ] Additional Indian languages
- [ ] More state-board curricula
- [ ] Teacher dashboards
- [ ] Community-created learning resources
- [ ] Large-scale deployment in low-connectivity regions

---

🌱 Impact

Vaani AI is built around a simple idea:

«Language and connectivity should not determine who gets access to quality digital education.»

By combining multilingual technologies with offline-first design, Vaani AI can help make digital learning more accessible to communities that are often underserved by conventional education technology.

---

👥 Target Users

Vaani AI is particularly designed for:

- 👧 School students
- 🏫 Government-school learners
- 🌱 Tribal and rural communities
- 🗣️ Speakers of low-resource Indian languages
- 📱 Learners using low-cost mobile devices
- 📶 Students in areas with unreliable connectivity

---

⚡ Getting Started

Prerequisites

- Modern web browser
- Python 3.x
- Internet connection for AI-powered features

Clone the Repository

git clone https://github.com/Duskcrevice/Vaani-AI.git
cd Vaani-AI

Start the Backend

python server.py

Open the Application

Open the frontend in your browser or access the deployed PWA.

---

📁 Project Structure

Vaani-AI/
│
├── index.html
├── server.py
│
├── js/
│   ├── services/
│   │   └── translation.js
│   ├── i18n.js
│   ├── ncert.js
│   └── ...
│
├── data/
│   ├── db.json
│   └── ...
│
├── sw.js
│
├── css/
│   └── ...
│
├── assets/
│   └── ...
│
└── README.md

---

🏆 SIH Focus

Vaani AI is designed as a practical, deployable solution rather than a conceptual AI prototype.

Our approach combines:

AI + Indian Languages + Voice + Education + Offline-First Technology

The core differentiator is the integration of these components into a single learning platform targeted at users who may otherwise be excluded by language or connectivity barriers.

---

📜 License

This project is developed as part of the Smart India Hackathon (SIH).

Add the appropriate license and third-party attribution information before public distribution.

---

❤️ Built For Accessible Education

Vaani AI

Making learning more accessible — one language at a time.
