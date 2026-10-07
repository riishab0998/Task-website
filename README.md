# Docker Full-Stack Task Manager

A beginner-friendly full-stack web application using:

- Frontend: HTML, CSS, JavaScript + Nginx
- Backend: Node.js + Express
- Database: PostgreSQL
- Containerization: Docker + Docker Compose

## Architecture

Browser
   |
   v
Nginx Frontend :8080
   |
   v
Express API :5000
   |
   v
PostgreSQL :5432

## Run the application

Make sure Docker Desktop is running.

From this project folder:

```bash
docker compose up --build
```

Then open:

http://localhost:8080

## Check containers

```bash
docker compose ps
```

You should see:

- taskmanager-frontend
- taskmanager-backend
- taskmanager-db

## Stop

```bash
docker compose down
```

## Stop and delete database volume

WARNING: this deletes the PostgreSQL data:

```bash
docker compose down -v
```

## API endpoints

GET /api/health
GET /api/tasks
POST /api/tasks
PUT /api/tasks/:id
DELETE /api/tasks/:id

## GitHub

Create a new GitHub repository, then:

```bash
git init
git add .
git commit -m "Initial full-stack Docker application"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```
