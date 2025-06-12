# 📸 Receiptrix

**Receiptrix** is a mobile application that lets you scan receipts, clean messy OCR output using AI (LLM), and track expenses or inventory in an easy-to-use tabular format. The app works offline with full local database support and includes an optional premium feature using GPT for smarter receipt parsing.

---

## ✨ Features

- OCR scanning using **Google ML Kit**
- AI-powered receipt cleanup using **LLM (GPT)** via **FastAPI**
- Store parsed receipts locally in **SQLite**
- View, search, and filter past receipts
- Export data to **CSV**
- No sign-up, no cloud dependency by default

---

## 🔧 Tech Stack

| Layer     | Tech Used                         |
|-----------|-----------------------------------|
| Frontend  | Flutter (Dart)                    |
| OCR       | Google ML Kit (`google_ml_kit`)   |
| Backend   | FastAPI (Python)                  |
| AI/LLM    | OpenAI API (GPT-3.5 or GPT-4)     |
| Storage   | SQLite via `sqflite` (offline DB) |
| Export    | `csv` + `share_plus` (Flutter)    |

---

## 📱 Screenshots

| Capture | Edit Text | AI Cleanup | Receipt History |
|----------|------------|-------------|-----------------|
| _Coming soon_ | _Coming soon_ | _Coming soon_ | _Coming soon_ |

---

## 🏗️ Project Structure

```
receiptrix/
├── backend/                     # FastAPI microservice
│   ├── main.py
│   ├── parser.py
│   └── requirements.txt
├── flutter_app/                 # Flutter app
│   └── lib/
│       ├── screens/
│       ├── services/
│       ├── models/
│       └── main.dart
```

---

## 🚀 Getting Started

### 🖥️ Backend (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Run the server
uvicorn main:app --host 0.0.0.0 --port 8000
```

Set your OpenAI API key:

```bash
export OPENAI_API_KEY="your_api_key_here"
```

---

### 📱 Frontend (Flutter)

```bash
cd flutter_app
flutter pub get
flutter run
```

Configure your backend URL in your Flutter service file:

```dart
final apiUrl = "http://<your-ip>:8000/parse-receipt";
```

For Android emulators, use `http://10.0.2.2:8000`.

---

## 📤 Export Example

- Generate a `.csv` file from inventory data
- Share via WhatsApp, Email, etc.

---

## 🧠 Roadmap

- [ ] Add receipt categorization using custom LLM prompts
- [ ] In-app editing of structured receipt JSON
- [ ] Firebase login + sync
- [ ] In-app purchase/paywall toggle
- [ ] Warranty reminders with notifications

---

## 🛡️ License

MIT License. See [`LICENSE`](LICENSE) for details.

---

## 🙌 Contributing

Contributions are welcome! Please open issues or submit pull requests.
