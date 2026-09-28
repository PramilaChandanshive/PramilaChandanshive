# 🎯 AI Course Planner – Smart Study Assistant

> An intelligent Python desktop application that generates personalized study timetables by analyzing your daily routine and scheduling courses **only after you wake up** (respecting sleep hours).

![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python&logoColor=white)
![Tkinter](https://img.shields.io/badge/GUI-Tkinter-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-success)

---

## 📌 Overview

**AI Course Planner** solves a common student problem: *"When should I study?"*

Most learners have irregular routines (college, work, sleep, meals) and struggle to find consistent study time. This app analyzes your daily schedule, detects free time slots using an **interval-merging algorithm**, and automatically assigns course study sessions — **while guaranteeing no sessions during sleep hours**.

It's essentially a mini data platform: **ingest → transform → persist → analyze → notify**.

---

## ✨ Features

### 🔐 User Authentication
- Multi-user registration with email validation (regex)
- Login via email **or** username
- Password strength check (min 6 characters)
- Persistent JSON-based storage with atomic writes

### 📅 Daily Schedule Management
- Add daily activities (sleep, college, work, meals, travel)
- Handles **overnight activities** (e.g., sleep 23:00 → 07:00)
- Validates start time < end time for each activity

### 🧠 AI Scheduling Engine
- **Interval-merging algorithm** to detect free slots
- Handles overlapping intervals
- Schedules courses **only AFTER wake-up time** (post-sleep)
- Recommends optimal study hours based on free-slot analysis

### 📚 Multiple Course Addition Modes
| Mode | Description |
|------|-------------|
| **Quick Add** | Choose from 6+ predefined courses |
| **Custom Course** | Create your own with name, hours, lessons |
| **Smart Plan** | Set deadline (e.g., "Learn Python in 4 days") — AI distributes hours automatically |

### 📊 Dynamic Timetable
- 7-day × 24-hour grid (2-hour blocks)
- **Color-coded cells** based on progress:
  - 😴 Blue = Sleep / Rest time
  - 🔴 Red = Busy (college/work)
  - 🟡 Yellow = Course in progress (30-70%)
  - 🟢 Green = Course advanced (>70%)
  - ✨ Gray = Free time
- Scrollable with mousewheel support

### 📈 Progress Tracking
- Daily study minutes logged
- Lessons completed counter
- Overall progress percentage
- Total study time
- **Streak system** (consecutive days)
- **Achievements**: 3-Day Streak, 7-Day Streak, 5+ Hours Studied

### 🔔 Smart Notifications
- Study reminders at scheduled hours
- Morning motivation at 7:00 AM (after wake-up)
- Course completion alerts
- **Multithreaded** background worker (doesn't block GUI)
- **No notifications during sleep hours** (23:00 – 07:00)

---

## 🏗️ Architecture
┌─────────────────┐ ┌──────────────────┐ ┌─────────────────┐
│ User Input │────▶│ Transform Layer │────▶│ Persistent │
│ (Routine + │ │ • Interval │ │ Store │
│ Courses) │ │ Merging │ │ (JSON) │
│ │ │ • Free-slot │ │ │
│ │ │ Detection │ │ │
└─────────────────┘ └──────────────────┘ └─────────────────┘
│
▼
┌─────────────────┐ ┌──────────────────┐ ┌─────────────────┐
│ Notifications │◀────│ Analytics │◀────│ Timetable │
│ (Multithread) │ │ Aggregator │ │ Visualizer │
│ │ │ • Streaks │ │ • Color-coded │
│ │ │ • Progress % │ │ • Progress │
└─────────────────┘ └──────────────────┘ └─────────────────

---

### Data Flow Pipeline
1. **Extract** — Capture user's daily routine as raw time-interval records
2. **Transform** — Merge overlapping intervals, split overnight activities, compute free slots
3. **Load** — Persist structured schedules to JSON with atomic writes
4. **Analyze** — Aggregate study minutes, streaks, completion percentages
5. **Notify** — Run background jobs to send reminders and achievements

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Language** | Python 3.7+ |
| **GUI** | Tkinter (built-in) |
| **Data Storage** | JSON (file-based) |
| **Concurrency** | `threading` (daemon threads) |
| **Notifications** | `plyer` |
| **Time Logic** | `datetime` |
| **Validation** | `re` (regex) |

---

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/AI-Course-Planner.git
cd AI-Course-Planner

# 2. Install dependencies
pip install plyer

# 3. Run the application
python course_planner.py
