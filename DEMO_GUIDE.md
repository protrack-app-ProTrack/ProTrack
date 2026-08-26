# 🚀 ProTrack — Faculty Demonstration & Feature Guide

Welcome to the official feature tour and live demonstration guide for **ProTrack**. This guide is designed to help you showcase the entire app's capabilities to your project guide, supervisor, or evaluation panel.

---

## 🔑 Login Credentials for Demo

To demonstrate both student and faculty workflows, use the following pre-configured credentials:

| Role | User Persona | Email Address | Password | Key Actions to Show |
| :--- | :--- | :--- | :--- | :--- |
| **Faculty / Guide** | Dr. Sharma (Supervisor) | `sharma@college.edu` | `faculty123` | Supervision list, Rubric grading, Remarks, PDF print |
| **Student / Team Lead** | Aarav Mehta (Group 01 Lead) | `aarav@college.edu` | `student123` | Task creation, AI planner, Kanban, Gantt, Peer ratings |
| **Student / Developer** | Diya Sharma (Developer) | `diya@college.edu` | `student123` | Task status updates, Team chat |

---

## 🎬 Live Demonstration Script (Step-by-Step)

Follow these steps during your live presentation to showcase every feature in a logical flow:

### 1. The Entrance & Glassmorphic UI
* **Action:** Open the app and toggle **Dark Mode** 🌙 / **Light Mode** ☀️ in the header.
* **Talking Point:** *"ProTrack features an adaptive glassmorphic UI styled with translucent layers (`backdrop-filter: blur`), custom accent glows, and persistent theme switching. The date inputs and scrollbars are customized to blend with dark mode layouts."*

### 2. Subject Workspaces & AI Sprint Planner
* **Action:** Sign in as Aarav (`aarav@college.edu`). Open the **AI Sprint Planner** 🤖. Select a course (e.g., *23AID205 — Machine Learning*) and click **"Add Tasks to Board"**.
* **Talking Point:** *"Each semester subject is a dedicated hub. The AI Sprint Planner generates course-specific, pre-structured tasks (like dataset preprocessing or validation setup) matching our syllabus, allowing teams to bootstrap their sprint board in one click."*

### 3. Kanban Task Board & Live Filters
* **Action:** Go to the **Task Board** tab. 
  * Apply a filter: Select **"Assignee: Diya"** or click **"🙋 Only My Tasks"**.
  * Drag a card to the **Done** column to trigger the confetti celebration.
* **Talking Point:** *"The Kanban board supports real-time filtering by Assignee, Priority, and Topic to manage high-volume boards. Dragging a card to completion fires a confetti animation, and all updates sync instantly across teammates' screens via our Firebase backend."*

### 4. Interactive Gantt Timeline
* **Action:** Go to the **Timeline** tab. Scroll through the horizontal Gantt chart. Hover over/click a task bar.
* **Talking Point:** *"Instead of simple text lists, ProTrack generates a dynamic Gantt Chart Timeline. It maps task start and due dates onto project weeks. Completed items show in glassy green, blocked in red, and in-progress in blue. Clicking a bar opens details."*

### 5. Burndown Analytics Chart
* **Action:** Go to the **Analytics** tab. Show the **Burndown Trend** graph.
* **Talking Point:** *"The Analytics dashboard plots an SVG-based Burndown Chart. It dynamically calculates the linear ideal burndown path and contrasts it against our actual remaining tasks count, giving an instant indicator of team velocity."*

### 6. Teammate Peer Review & Rating
* **Action:** Go to the **My Team** tab. Show the rating stars and click **"Submit Ratings"**.
* **Talking Point:** *"To encourage collaboration, team members rate each other's performance across code contributions, communication, and responsiveness. Ratings are averaged and displayed on individual student dashboards."*

### 7. Faculty Supervision & Rubric Grading
* **Action:** Log out and log back in as Dr. Sharma (`sharma@college.edu`). 
  * Go to the **Groups** tab. Filter groups by subject code.
  * Click **"Grade & Evaluate Group"** for Group 01.
  * Enter marks out of maximums: Literature (10), Design (20), Code Quality (40), Presentation (30).
* **Talking Point:** *"Supervisors supervise multiple student groups, filtering them by course. Grading is handled through an academic rubric. The system automatically computes total scores and assigns letter grades (A+, A, B, C, F) mapped to institutional limits."*

### 8. Official Grade Scorecard PDF
* **Action:** On the graded group panel, click **"Download PDF"**.
* **Talking Point:** *"Once graded, either faculty or students can export an official evaluation sheet. It generates a formatted PDF complete with institutional headers, student roles, detailed marks breakdown, evaluator feedback, and guide signature blocks."*

---

## 🧰 Tech Stack Overview

Explain the clean, dependency-free architecture to your examiners:

* **Frontend:** Single-page Vanilla JS (HTML5, CSS Variables, SVG Charts, no frameworks like React/Vue to maintain lightweight performance).
* **Backend:** Node.js Express REST API with real-time SSE (Server-Sent Events) notifications.
* **Database & Sync:** Flexible JSON datastore (`data.json`) with direct Firebase Auth/Firestore real-time sync wrapper.
