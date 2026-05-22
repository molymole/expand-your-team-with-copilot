# Mergington High School Activities

A FastAPI web application that allows students to view and sign up for extracurricular activities at Mergington High School, with teacher authentication for managing registrations.

## Features

- View all available extracurricular activities
- Filter activities by category, difficulty, day, and time
- Search activities by name or description
- Sign up for activities (requires teacher authentication)
- Unregister students from activities (requires teacher authentication)
- Teacher login and session management

## Technology Stack

- **Backend:** Python, FastAPI
- **Database:** MongoDB
- **Frontend:** HTML, CSS, JavaScript

## API Endpoints

| Method | Endpoint | Description |
| ------ | -------- | ----------- |
| GET | `/activities` | Get all activities (supports `day`, `start_time`, `end_time` query filters) |
| GET | `/activities/days` | Get a list of all days that have activities scheduled |
| POST | `/activities/{activity_name}/signup` | Sign up a student for an activity (requires `email` and `teacher_username`) |
| POST | `/activities/{activity_name}/unregister` | Remove a student from an activity (requires `email` and `teacher_username`) |
| POST | `/auth/login` | Login as a teacher (requires `username` and `password`) |
| GET | `/auth/check-session` | Check if a teacher session is valid (requires `username`) |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
