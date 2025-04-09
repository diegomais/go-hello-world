# 🐳 Docker Compose: Go + PostgreSQL

## 📦 Requirements

- Docker
- Docker Compose

## 🚀 How to run the project

1. Clone this repository

2. Create a `.env` file in the root with the following variables:

```env
POSTGRES_USER=myuser
POSTGRES_PASSWORD=mypassword
POSTGRES_DB=mydb
```

3. Also create the `app/.env` file with:

```env
DB_HOST=postgres
DB_USER=myuser
DB_PASSWORD=mypassword
DB_NAME=mydb
```

4. Run:

```bash
docker-compose up --build
```

5. Go to http://localhost:3000 to test the connection to the database.
