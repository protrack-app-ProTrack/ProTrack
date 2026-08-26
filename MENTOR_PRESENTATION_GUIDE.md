# 🛰️ ProTrack — Project Presentation & Storyboard Guide
> **Prepared for:** Yugal Garg  
> **Purpose:** Presenting the complete functionality of **ProTrack** to your Project Mentor / Faculty Panel.

---

## 📖 Chapter 1: The Elevator Pitch (Mentor Introduction)

Start your presentation by defining the core problem ProTrack solves:
> *"Sir/Ma'am, traditionally, college project tracking is fragmented. Teams use generic tools like Trello, WhatsApp, and Excel, while faculty supervisors review progress via manual emails. **ProTrack** is a unified, subject-centric workspace specifically built for academic environments (mapped to our B.Tech curriculum). It integrates student collaboration, AI task suggestion, horizontal timeline scheduling, peer evaluations, and official rubric grading in one secure platform."*

---

## 🎨 Chapter 2: Visual Screen-by-Screen Map (UI Layout Guide)

Here is exactly what is on the screen, what the elements do, and how they behave:

```
┌────────────────────────────────────────────────────────────────────────┐
│  [☀️/🌙 Toggle]                     Search [🔍 Tasks, Members]   [🔔]  │ ◄── Top Header
├─────────────────┬──────────────────────────────────────────────────────┤
│ 🛰️ ProTrack     │                                                      │
│                 │  📢 Current Subject Hub: 23AID205 (Machine Learning) │ ◄── Subject Workspace selector
│ 🏠 Dashboard    │                                                      │
│ 📋 Task Board   │  ┌────────────────────────────────────────────────┐  │
│ 📊 Timeline     │  │  📋 Kanban Board                               │  │
│ 📈 Analytics    │  │  To-Do ──▶ In Progress ──▶ In Review ──▶ Done  │  │ ◄── Core Board
│ 👥 My Team      │  │  [Only My Tasks]       [Priority: High 🔻]     │  │
│ ⚙️ Settings     │  └────────────────────────────────────────────────┘  │
│                 │                                                      │
│ 🚪 Logout       │  📉 Burndown Analytics (SVG Trend Line)              │ ◄── SVG Graphics
└─────────────────┴──────────────────────────────────────────────────────┘
  ▲
  └── Sidebar Navigation Panel (Glassmorphic Backdrop Blur)
```

---

## 🎬 Chapter 3: Slide-by-Slide Storyboard (Your Presentation Script)

Use these slides/notes to explain the website to your mentor who has zero prior knowledge:

### 📽️ Slide 1: Welcome & Landing
* **Visual on Screen:** Login/Sign-up Page (Glassmorphic card with dark mode toggled).
* **What to tell your mentor:**
  > *"This is the entry gate. ProTrack has built-in roles: **Students (Team Leads, Developers, Testers)** and **Faculty/Guides**. The theme is adaptive; toggling dark mode updates all inputs, borders, scrollbars, and calendar indicators for high-contrast visibility."*

### 📽️ Slide 2: The Core Workspace & AI Planner
* **Visual on Screen:** Dashboard showing active team task count, subject codes (23AID205, 23AID211, etc.), and the AI Sprint Planner button.
* **What to tell your mentor:**
  > *"Every subject from our B.Tech Semester 3 curriculum is an active workspace. To help students get started instantly, the **AI Sprint Planner** reads the subject code and auto-generates highly relevant tasks based on our syllabus (e.g. preprocessing datasets for ML, or writing DDL schemas for DBMS)."*

### 📽️ Slide 3: The Kanban Task Board & Live Filters
* **Action to Perform:** Focus search input, type a name, then filter by "High" priority. Drag a task card to "Done".
* **What to tell your mentor:**
  > *"This is the central execution board. Team Leads can create and assign tasks. To handle cluttered workspaces, we built dynamic **Kanban Filters** where students can isolate tasks by Assignee, Priority, or Topic instantly. Completing a task triggers a rewarding confetti celebration."*

### 📽️ Slide 4: Horizontal Gantt timeline
* **Visual on Screen:** Timeline tab showing horizontal timeline grid mapped across weeks (August, September, October).
* **What to tell your mentor:**
  > *"Standard trackers only show vertical lists. ProTrack generates an **Interactive Gantt Timeline** that maps active tasks as horizontal bars over time. Green means completed, blue is in-progress, and red indicates blocked items. Clicking any bar allows direct editing."*

### 📽️ Slide 5: Real-time Burndown Analytics
* **Visual on Screen:** Analytics tab showing the SVG line chart.
* **What to tell your mentor:**
  > *"We have built-in SVG graphics rendering a live **Burndown Trend Chart**. It automatically plots the ideal target path (dashed line) against actual remaining tasks (solid line) calculated from task update timestamps, giving an objective health score of our project velocity."*

### 📽️ Slide 6: Peer Reviews & Collaborative Feedback
* **Visual on Screen:** "My Team" tab displaying stars ratings next to student names.
* **What to tell your mentor:**
  > *"To ensure individual accountability, teammates rate each other's contributions (stars out of 5) on code, communication, and speed. Ratings are averaged and displayed as performance indicators on student dashboards."*

### 📽️ Slide 7: Faculty Supervision & Rubric Evaluator
* **Visual on Screen:** Logged in as Dr. Sharma (`sharma@college.edu`). Groups list, grading inputs, and "Download PDF" scorecard widget.
* **What to tell your mentor:**
  > *"For faculty guides, the dashboard provides oversight. They can filter teams by subject and grade them using a **weighted academic rubric**: Literature Survey (10), System Design (20), Code Quality (40), and Presentation (30). The system auto-calculates total scores and issues final letter grades (A+, A, B...)."*

### 📽️ Slide 8: Official Grade Scorecard PDF
* **Visual on Screen:** Clicking "Download PDF" which opens the print preview dialog.
* **What to tell your mentor:**
  > *"Finally, the system generates an official A4 evaluation scorecard PDF. It compiles all student names, project data, rubric scores, supervisor feedback comments, and signature blocks, ready to be printed or submitted to the department."*

---

## ❓ Chapter 4: Anticipated Questions & Smart Answers

Be ready for these common questions your mentor might ask:

* **Q: Where is the database hosted? How does it sync?**
  * *Answer:* "Sir, the application is built on a hybrid architecture. The frontend is a static Single Page Application (SPA). Data syncs in real-time using Firebase Firestore REST APIs. For offline or local setups, it automatically falls back to standard local browser storage."
* **Q: How does the app ensure students don't modify other teams' boards?**
  * *Answer:* "Permission boundaries are enforced. Standard students can only view or move tasks assigned to them within their specific groupId. Only the Team Lead has permission to add members and create tasks, and only the Faculty can enter grading metrics."
* **Q: What is the benefit of the Gantt Timeline over a regular list?**
  * *Answer:* "It allows the supervisor to detect scheduling overlap and workload issues visually. If too many high-priority tasks are scheduled in the same week, we can identify bottleneck risks immediately."
