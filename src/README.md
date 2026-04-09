# Mergington High School Activities

A website application that allows students to view and sign up for extracurricular activities at Mergington High School.

## Features

- View all available extracurricular activities
- Search activities by name
- Filter activities by category, day, time of day, and difficulty level
- Sign up for activities (requires teacher authentication)
- Unregister students from activities (requires teacher authentication)
- Teacher login and logout
- Dark mode toggle

## Tech Stack

- **Backend:** FastAPI (Python)
- **Database:** MongoDB
- **Frontend:** HTML, CSS, JavaScript

## API Endpoints

| Method | Endpoint | Description |
| ------ | -------- | ----------- |
| GET | `/activities` | Get all activities, with optional filters: `day`, `start_time`, `end_time`, `difficulty` |
| GET | `/activities/days` | Get a list of all days that have activities scheduled |
| POST | `/activities/{activity_name}/signup` | Sign up a student for an activity (requires `email` and `teacher_username` params) |
| POST | `/activities/{activity_name}/unregister` | Remove a student from an activity (requires `email` and `teacher_username` params) |
| POST | `/auth/login` | Log in as a teacher (requires `username` and `password` params) |
| GET | `/auth/check-session` | Check if a teacher session is valid (requires `username` param) |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
