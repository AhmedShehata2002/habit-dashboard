# 📊 Habit Dashboard PWA

An always-on personal productivity dashboard deployed via GitHub Pages as a Progressive Web App (PWA). Built to live permanently on an iPhone mounted to an IKEA SKÅDIS pegboard as a home control centre.

**[🔗 Live Demo](https://ahmedshehata2002.github.io/habit-dashboard)**

---

## Why I Built This

I wanted a single glance-able dashboard that scores my day across the habits that matter most — prayer, training, nutrition, and study — and logs that score automatically to Google Calendar so I can track consistency over time. No app subscriptions, no friction, just a number that tells me how I did today.

---

## What It Does

- **Daily scoring** — 9 points across 4 categories (prayer ×5, training, nutrition, study)
- **Abu Dhabi prayer times** — live countdown to next salah calculated from coordinates
- **Auto-logging** — pushes daily score + notes to Google Calendar at 11:30pm
- **Streak tracking** — visual streak counter with milestone rewards at day 7, 21, 66, 90
- **Live weather** — Abu Dhabi conditions via Open-Meteo (no API key needed)
- **Sound feedback** — distinct audio cue per category tap, dopamine-optimised for ADHD focus
- **Motivational states** — OFFLINE → ACTIVE → LOCKED IN → PERFECT DAY
- **Optional notes** — log what you studied, trained, ate per session
- **PWA** — installs to iPhone home screen, runs full-screen, works offline

  ---

  
## How It Works

The app is a single `index.html` file with no frameworks or dependencies:

- **Prayer time engine** — calculates Fajr, Dhuhr, Asr, Maghrib, Isha from Abu Dhabi coordinates using solar angle formulas
- **Scoring system** — tracks 9 daily points with localStorage persistence across sessions
- **Google Calendar link** — generates a pre-filled GCal URL with score and notes at 11:30pm
- **Streak engine** — persists across sessions and triggers milestone rewards at days 7, 21, 66, 90
- **Weather widget** — pulls live Abu Dhabi conditions from Open-Meteo API, refreshes every 10 minutes
- **Sound system** — Web Audio API generates distinct tones per category on each tap

---

## Tech Stack

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat&logo=pwa&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-222222?style=flat&logo=github&logoColor=white)

---

## Setup

1. Fork or clone this repo
2. Update the Abu Dhabi coordinates in `index.html` if you're in a different city
3. Deploy to GitHub Pages: Settings → Pages → Deploy from main branch
4. Open the URL in Safari on iPhone → Share → Add to Home Screen
5. Set Auto-Lock to Never, keep plugged in

---

## What I'd Build Next

- iOS Shortcuts automation to auto-check training from Whoop strain data
- MacroFactor API integration to auto-check nutrition when calorie goal is hit
- Weekly heatmap view (GitHub-style contribution graph for habits)
- Multi-user support with shared leaderboard

---

## Lessons Learned

Building this taught me a lot about the Web Audio API, PWA manifest configuration, and how to persist state cleanly across sessions without a backend. The prayer time calculation engine — computing solar angles from coordinates — was the most technically interesting part.

---
