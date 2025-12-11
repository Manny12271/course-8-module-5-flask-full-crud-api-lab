# Flask Full CRUD API Lab

## Overview

Build a RESTful API in Flask to manage **events**. Supports:

- **POST /events** – create a new event  
- **PATCH /events/<id>** – update an event title  
- **DELETE /events/<id>** – remove an event  

Uses in-memory Python objects to simulate a database. Returns JSON with proper HTTP status codes.

---

## Setup

```bash
git clone <repo-url>
cd course-8-module-5-flask-full-crud-api-lab
pipenv install   # or pip install flask
pipenv shell     # or activate your environment
python app.py
API Endpoints

Create Event:
POST /events
Body: { "title": "Hackathon" }
Response: 201 Created
{ "id": 3, "title": "Hackathon" }

Update Event:
PATCH /events/<id>
Body: { "title": "Hackathon 2025" }
Response: 200 OK
{ "id": 1, "title": "Hackathon 2025" }

Delete Event:
DELETE /events/<id>
Response: 204 No Content

Error Handling:
400 Bad Request → missing title
404 Not Found → invalid event ID

Notes:
Routes use RESTful nouns
Proper status codes for each action
In-memory data storage (no DB)
Inline comments in code explain logic

Next Steps:
Integrate a real database for persistent storage
Add GET endpoints for full CRUD experience