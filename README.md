# 🐍 Django Dockerized Project & CI/CD Pipeline

This is a Dockerized Django project configured for local development, CI/CD pipelines, and deployment using PostgreSQL as the database.

## Features

- Django application with environment-based configuration
- PostgreSQL integrated via Docker Compose
- Gunicorn as the production WSGI server
- `.env` file support for managing secrets and environment variables
- CI/CD ready (e.g., GitLab pipelines)
- Separated `Dockerfile` and `.gitlab-ci.yml` for clean deployment workflows

## Setup Instructions

1. Create an `.env` file in the root of the project.
2. Add your environment variables:

```env
SECRET_KEY=your_django_secret_key
DJANGO_ALLOWED_HOSTS=localhost
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=db
DB_PORT=5432

```

## CI/CD Notes

> The .gitlab-ci.yml is preconfigured to build, push, and deploy your Docker image.
>
> Use your preferred runner tag in the deploy job section to control which runner handles deployment.
