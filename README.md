# IPLitics — IPL Insights & Predictions

A student-built app that mixes live IPL info with simple ML models so fans can explore player/team stats and try basic score/outcome predictions. Built with Flutter + Python (Flask), designed in Figma, and backed by a small analytics pipeline.

---

## 🎯 Objective
We wanted a clean, reliable place for IPL fans to check form, compare players/teams, and play with data-driven predictions — not just a fantasy lineup tool or a score ticker.  
The aim was to combine real-time match info with historical data analysis and basic machine learning for quick insights.

---

## 📌 Features

- **Live Match View** — Displays scores and key stats in a familiar scoreboard style.
- **Top Players & Teams** — Carousels leading to detailed views with stats like matches played, runs, strike rate, wickets, coach, and roster.
- **Quick Selections** — Dropdowns and pickers for faster, cleaner data input.
- **Basic Predictions** — Simple models estimating batting and bowling outcomes based on recent stats.

---

## 📱 Screens

- **Home** — Carousels for quick navigation.
- **Live Matches**
- **Players**
- **Teams**

---

## 🛠 Tech Stack

### **Design**
- Figma — Low-fidelity → high-fidelity flows

### **Mobile App**
- Flutter (Dart) — `carousel_pro`, `url_launcher`, `Cupertino`, `BottomNavigationBar`, `ListView.builder`, async/await
- AnimationController for smooth UI transitions
- `HttpOverrides` for live API integration

### **Backend**
- Python + Flask REST API

### **Machine Learning**
- EDA → PCA / feature filtering → Model training → Deployment
- Simple models for explainability and speed

---

## 📊 Data & Modeling

### **EDA Highlights**
- Cleaned batting & bowling data
- Fixed null/missing values and unified data types
- Derived opponent team per innings for better context

### **Feature Screening**
- Checked correlations (e.g., Runs ↔ Balls Faced ≈ 0.93)
- Removed highly correlated or irrelevant features

### **Model Results**
#### Batsman (Demographic Features)
- KNN: **0.9729**
- Linear Regression: **0.9806**
- Random Forest: **0.9757**

#### Bowler (Demographic Features)
- KNN: **0.2242**
- Linear Regression: **0.3507**
- Random Forest: **0.3640**

> Overall app outcomes: **~93% accuracy** across test matches.

---
