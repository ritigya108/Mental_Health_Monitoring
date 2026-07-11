# 🚀 Git Setup Guide - MindCare AI Mental Health Monitoring

Complete guide to push your project to GitHub.

## 📋 Prerequisites

- Git installed on your system
- GitHub account created
- Terminal/Command Line access

## 🎯 Quick Setup (5 Steps)

### Step 1: Initialize Git Repository

```bash
cd ~/Desktop/mental-health-ai
git init
```

### Step 2: Add All Files

```bash
git add .
```

### Step 3: Create First Commit

```bash
git commit -m "Initial commit: AI Mental Health Monitoring System for India"
```

### Step 4: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `mindcare-ai-mental-health`
3. Description: `AI-powered mental health monitoring solution for India with crisis support`
4. Choose: **Public** or **Private**
5. **DO NOT** initialize with README (we already have one)
6. Click "Create repository"

### Step 5: Push to GitHub

```bash
# Replace YOUR_USERNAME with your GitHub username
git remote add origin https://github.com/YOUR_USERNAME/mindcare-ai-mental-health.git
git branch -M main
git push -u origin main
```

## 📁 What Will Be Pushed

### ✅ Included Files

```
mental-health-ai/
├── .gitignore                          # Git ignore rules
├── README.md                           # Main documentation
├── QUICKSTART.md                       # Setup guide
├── PROJECT_STRUCTURE.md                # File organization
├── FEATURES_COMPLETE.md                # Feature list
├── GIT_SETUP.md                        # This file
│
├── backend/                            # FastAPI Backend
│   ├── main.py
│   ├── models.py
│   ├── database.py
│   ├── ai_analyzer.py
│   ├── requirements.txt
│   ├── .env.example
│   └── README.md
│
├── frontend/                           # React Frontend
│   ├── package.json
│   ├── public/
│   │   └── index.html
│   └── src/
│       ├── index.js
│       ├── index.css
│       ├── App.js
│       ├── components/
│       │   └── Navigation.js
│       ├── pages/
│       │   ├── Dashboard.js
│       │   ├── MoodTracker.js
│       │   ├── Journal.js
│       │   ├── ChatBot.js
│       │   ├── Resources.js
│       │   └── Profile.js
│       └── services/
│           └── api.js
│
└── streamlit-app/                      # Streamlit Version
    ├── Home.py
    ├── requirements.txt
    ├── README.md
    ├── TROUBLESHOOTING.md
    ├── run.sh
    └── pages/
        ├── 1_Mood_Tracker.py
        ├── 2_Journal.py
        ├── 3_AI_Chat.py
        ├── 4_Resources.py
        └── 5_Profile.py
```

### ❌ Excluded Files (via .gitignore)

- `node_modules/` - Node dependencies
- `venv/` - Python virtual environment
- `.env` - Environment variables (secrets)
- `*.db` - Database files
- `__pycache__/` - Python cache
- `.DS_Store` - Mac system files
- `*.log` - Log files

## 🔧 Detailed Git Commands

### Initialize Repository

```bash
cd ~/Desktop/mental-health-ai
git init
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

### Check Status

```bash
git status
```

### Add Files

```bash
# Add all files
git add .

# Or add specific files
git add README.md
git add backend/
git add frontend/
git add streamlit-app/
```

### Commit Changes

```bash
git commit -m "Initial commit: Complete AI Mental Health Monitoring System"
```

### Connect to GitHub

```bash
# Add remote repository
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# Verify remote
git remote -v

# Push to GitHub
git branch -M main
git push -u origin main
```

## 📝 Good Commit Messages

Use clear, descriptive commit messages:

```bash
# Initial commit
git commit -m "Initial commit: AI Mental Health Monitoring System"

# Feature additions
git commit -m "Add: Streamlit dashboard with mood tracking"
git commit -m "Add: AI sentiment analysis for journal entries"
git commit -m "Add: Indian crisis hotlines and resources"

# Bug fixes
git commit -m "Fix: DataFrame ArrowTypeError in mood logs"
git commit -m "Fix: Journal input clearing issue"

# Updates
git commit -m "Update: Localize all content for India"
git commit -m "Update: Add KIRAN and Vandrevala helplines"

# Documentation
git commit -m "Docs: Add comprehensive setup guide"
git commit -m "Docs: Update README with Indian resources"
```

## 🌿 Branching Strategy

### Create Feature Branch

```bash
# Create and switch to new branch
git checkout -b feature/new-feature

# Make changes and commit
git add .
git commit -m "Add: New feature description"

# Push branch to GitHub
git push origin feature/new-feature
```

### Merge to Main

```bash
# Switch to main
git checkout main

# Merge feature branch
git merge feature/new-feature

# Push to GitHub
git push origin main
```

## 🔄 Regular Updates

### Pull Latest Changes

```bash
git pull origin main
```

### Push Your Changes

```bash
git add .
git commit -m "Your commit message"
git push origin main
```

## 📊 Repository Settings

### Recommended GitHub Settings

1. **Description**: 
   ```
   AI-powered mental health monitoring solution for India with crisis support, mood tracking, AI journal analysis, and chatbot
   ```

2. **Topics** (add these tags):
   - `mental-health`
   - `ai`
   - `machine-learning`
   - `streamlit`
   - `react`
   - `fastapi`
   - `india`
   - `healthcare`
   - `sentiment-analysis`
   - `crisis-support`

3. **Website**: Your deployed app URL (if any)

4. **License**: Choose appropriate license (MIT recommended for open source)

## 🔒 Security Best Practices

### Never Commit These

❌ API keys
❌ Passwords
❌ Database credentials
❌ `.env` files
❌ Personal data
❌ Large binary files

### Use .env.example Instead

```bash
# .env.example (safe to commit)
DATABASE_URL=your_database_url_here
API_KEY=your_api_key_here

# .env (never commit)
DATABASE_URL=postgresql://real_connection_string
API_KEY=sk-real-api-key-12345
```

## 📦 Large Files

If you have large files (>100MB):

```bash
# Install Git LFS
git lfs install

# Track large files
git lfs track "*.pth"
git lfs track "*.h5"

# Add .gitattributes
git add .gitattributes
git commit -m "Add Git LFS tracking"
```

## 🐛 Common Issues

### Issue: "fatal: remote origin already exists"

```bash
git remote remove origin
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
```

### Issue: "Permission denied (publickey)"

```bash
# Use HTTPS instead of SSH
git remote set-url origin https://github.com/YOUR_USERNAME/REPO_NAME.git
```

### Issue: "Updates were rejected"

```bash
# Pull first, then push
git pull origin main --rebase
git push origin main
```

### Issue: "Large files detected"

```bash
# Remove from history
git rm --cached large_file.bin
git commit -m "Remove large file"
```

## 📱 GitHub Desktop (Alternative)

If you prefer GUI:

1. Download GitHub Desktop: https://desktop.github.com/
2. Open GitHub Desktop
3. File → Add Local Repository
4. Select `mental-health-ai` folder
5. Click "Publish repository"
6. Choose public/private
7. Click "Publish"

## 🎯 Quick Reference

```bash
# Status
git status

# Add files
git add .

# Commit
git commit -m "message"

# Push
git push origin main

# Pull
git pull origin main

# Create branch
git checkout -b branch-name

# Switch branch
git checkout branch-name

# View history
git log --oneline

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Discard changes
git checkout -- filename
```

## 📚 Additional Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

## ✅ Verification Checklist

Before pushing:

- [ ] All files added (`git status` shows clean)
- [ ] .gitignore configured
- [ ] No sensitive data in commits
- [ ] README.md is complete
- [ ] Requirements files are up to date
- [ ] Code is tested and working
- [ ] Commit message is clear

## 🎊 After Pushing

Your repository will be live at:
```
https://github.com/YOUR_USERNAME/mindcare-ai-mental-health
```

Share it with:
- Collaborators
- Potential employers
- Open source community
- Mental health organizations

## 📞 Need Help?

- GitHub Support: https://support.github.com/
- Git Documentation: https://git-scm.com/
- Stack Overflow: https://stackoverflow.com/questions/tagged/git

---

**Happy Coding! 🚀**

Your AI Mental Health Monitoring System is ready to share with the world! 🇮🇳💙