# HealthBot

An AI-powered medical assistant web app built as an MCA capstone project. Users describe symptoms in natural language and get AI-driven guidance, backed by an ensemble ML model, a chat-based interface, and supporting health tools — prescription tracking, reminders, a nearby-care locator, and emergency contacts.

**Live app:** [healthbotsc.vercel.app](https://healthbotsc.vercel.app)

## Overview

HealthBot combines a conversational AI frontend, a Node.js backend, and a Python/Flask ML engine into a full-stack health assistant, installable as a PWA. It was built by a two-person team as part of an MCA capstone project (2024–2026).

## Team & contributions

**Junaid Nazeer — Frontend**
- Conversational chat UI, including tappable follow-up suggestions and symptom confirmation steps
- Authentication & onboarding: email OTP verification, Google OAuth, forgot-password flow
- Interactive BMI calculator with a circular dial UI and unit switching
- Care Locator UI: facility search with specialty filters and GPS auto-detect
- Prescription OCR upload UI and medicine reminder scheduling with browser notifications
- Emergency contact management UI
- Text-to-speech playback for AI responses
- PWA setup (manifest, icons, splash screens) and dark/light theming

**Murtaza Badam — Backend, ML Engine & Deployment**
- ML engine: ensemble of five models (Random Forest, Gradient Boosting, Naive Bayes) for symptom-based prediction, with SMOTE for class imbalance
- Backend API (Node.js/Express/MongoDB): auth routes, reminders, emergency notifications, Care Locator backend (OSM + Google Places hybrid)
- Groq AI integration for conversational responses
- Deployment across Vercel (frontend), Render (backend), and Hugging Face Spaces (ML engine)

## Architecture

- **Frontend:** React, Tailwind CSS — deployed on Vercel
- **Backend:** Node.js, Express, MongoDB — deployed on Render
- **ML engine:** Python, Flask, scikit-learn — deployed on Hugging Face Spaces

## Running locally

Each subproject has its own setup — see `frontend/`, `backend/`, and `ml-engine/` for stack-specific instructions. Copy `.env.example` files to `.env` in each subproject and fill in your own API keys/credentials before running.

```bash
# Frontend
cd frontend && npm install && npm start

# Backend
cd backend && npm install && npm start

# ML engine
cd ml-engine && pip install -r requirements.txt && python app.py
```

---

Built as part of an MCA capstone project.
