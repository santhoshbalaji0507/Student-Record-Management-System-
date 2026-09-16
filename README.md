# Student Records Management System

A lightweight, responsive, client-side web application built for managing academic student entries. Developed using pure HTML5, CSS3, and modern JavaScript (ES6+), this system implements full CRUD (Create, Read, Update, Delete) functionality with local storage persistence and client-side form validation.

---

## Project Features

* **Complete CRUD Operations**: Add new entries, display all records, edit existing profiles in-place, and remove records safely with confirmation.
* **Real-time Search & Filter**: Dynamically filter records by student name, roll number, or department as you type.
* **Data Persistence**: Uses the browser’s native `localStorage` API to retain records across sessions without external database dependencies.
* **Client-Side Validation**: Ensures data integrity via custom email pattern matching, compulsory fields, and numeric range limits (CGPA 0.0–10.0).
* **Responsive UI Design**: Built with a warm CSS theme using flexbox and CSS grid layout that adapts seamlessly across mobile, tablet, and desktop views.
* **User Feedback**: Non-blocking toast notifications alert users upon successful creation, update, deletion, or sample data loading.

---

## Tech Stack

* **Frontend**: HTML5, CSS3 (CSS Variables, Flexbox, Grid)
* **Logic / Scripting**: JavaScript (ES6+, IIFE Encapsulation Pattern)
* **Data Layer**: Browser `localStorage` API (JSON formatted)
* **Typography**: Google Fonts (*Source Serif 4*, *IBM Plex Sans*, *IBM Plex Mono*)

---

## System Architecture

The application is structured following a lightweight Model-View-Controller (MVC) flow packed within a single HTML document:

```text
  [ User Actions ] 
         │
         ▼
 ┌───────────────┐
 │   View (UI)   │ ◄─── (HTML Form & Records Table)
 └───────┬───────┘
         │ Event Handlers
         ▼
 ┌───────────────┐
 │  Controller   │ ◄─── (Validation, Event Listeners, State Logic)
 └───────┬───────┘
         │ Reads/Writes
         ▼
 ┌───────────────┐
 │ Model / Storage│ ◄─── (In-Memory Array synchronized with localStorage)
 └───────────────┘
