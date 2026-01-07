# Contributing to Diabetes Care with AI 🩺

Thank you for your interest in contributing!  
This project leverages AI to provide accessible diabetes risk assessment and health information.  
We welcome contributions from developers, data scientists, and UI/UX designers of all skill levels.

---

## 🚀 Quick Start Guide

### 1. Fork and Clone

- Fork the repository on GitHub.
- Clone your fork locally:

```bash
git clone https://github.com/YOUR_USERNAME/Diabetes-care-with-AI.git
cd Diabetes-care-with-AI
```

- Add the upstream remote:

```bash
git remote add upstream https://github.com/Anshika09Singh/Diabetes-care-with-AI.git
```

---

### 2. Environment Setup

```bash
# Create and activate virtual environment
python -m venv venv

# Windows
.\venv\Scripts\activate

# macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

---

### 3. Configuration

Create a `.env` file in the root directory:

```env
GEMINI_API_KEY=your_api_key_here
```

> ⚠️ Do not commit the `.env` file. It is ignored via `.gitignore`.

---

### 4. Run the Application

```bash
# Development mode
python app.py

# Production mode (Gunicorn)
gunicorn app:app --bind 0.0.0.0:5000
```

Access the app at: **http://localhost:5000**

---

## 📂 Project Structure

| File / Folder | Description |
|--------------|------------|
| `app.py` | Flask application core (Routes, ML logic, Gemini API) |
| `diabetes_model.pkl` | Trained scikit-learn model |
| `scaler.pkl` | StandardScaler for feature normalization |
| `train.ipynb` | Model training & EDA notebook |
| `templates/` | Jinja2 HTML templates |
| `static/` | CSS, JS, and image assets |

---

## 🔌 API Endpoints

### Web Interface
- `GET /` : Landing Page  
- `GET /index` : Diabetes Prediction Form  
- `GET /chatbot` : AI Assistant Interface  
- `GET /forum` : Community Forum  

### Backend API
- `POST /predict` : Processes health data and returns diabetes risk  
- `POST /generate` : Gemini AI chatbot interface  
  ```json
  { "message": "string" }
  ```
- `GET /api/posts` : Fetch all forum entries  

---
# 💡 What Can You Contribute?

## 🐛 Bug Fixes

Found a bug?
Open an issue describing the bug.
Include steps to reproduce it.
After discussing, submit a PR that resolves it.

## ✨ New Features

Have an idea that would improve the project?
Propose it via an issue (with context/value).
Fork and develop on a feature branch:
git checkout -b feature/your-feature-name

## 📝 Documentation Improvements

Good docs matter! You can help by:
Improving the README
Adding usage examples
Clarifying parts of the contribution guide

## 🧪 Tests

Help us improve stability by:

Adding or updating tests in tests/
Ensuring coverage for new features

## 🎯 Commit Message Guidelines

Please use conventional commits to keep history readable

feat: — a new feature

fix: — bug fix

docs: — documentation only changes

style: — formatting/style changes

refactor: — code restructuring

test: — adding or updating tests

Example:

```

    git commit -m "feat: add health dashboard component"

```
---
## 🛠 Contribution Workflow

### 1. Pick an Issue
- Check the **Issues** tab for bugs or feature requests.
- If you have a new idea, open an issue first for discussion.

---

### 2. Branching and Commits

Create a feature branch:

```bash
git checkout -b feat/your-feature-name
```

We follow **Conventional Commits**:

- `feat:` A new feature  
- `fix:` A bug fix  
- `docs:` Documentation changes  
- `style:` Formatting / lint fixes  
- `refactor:` Code restructuring  

---

### 3. Submit a Pull Request

1. Push your branch:
```bash
git push origin feat/your-feature-name
```
2. Open a PR against the `main` branch.
3. Link the related issue (e.g., `Closes #52`).
4. Add screenshots for UI changes.

---

## ❓ Troubleshooting

### Issue: `GEMINI_API_KEY` not found
- Ensure `.env` exists in the root directory.
- Variable name must be **exactly** `GEMINI_API_KEY`.

### Issue: Model file not found (`.pkl`)
- Run `train.ipynb` to regenerate the model and scaler.

### Issue: Port 5000 already in use

**Windows**
```bash
netstat -ano | findstr :5000
taskkill /PID <PID> /F
```

**macOS/Linux**
```bash
lsof -i :5000
kill -9 <PID>
```

---

## ⚖️ Community Standards

Please be respectful and professional in all interactions.  
We aim to build a supportive and inclusive environment for healthcare innovation.

---

💬 **Questions?**  
Open an issue or comment on your Pull Request.

Happy coding! 🚀
Thank you for making Diabetes-care-with-AI better! ❤️
