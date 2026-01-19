# blog-api

Simple Blog Backend (CRUD) built with Node.js, Express and MongoDB.

## Author
Ankit Kumar Singh

## Features
- Create, Read, Update, Delete blog posts
- Validation: title and content are required
- Uses MongoDB for storage

## Tech Stack
- Node.js
- Express.js
- MongoDB (Mongoose)
- CORS, dotenv

## Project Structure
```
blog-api/
  ├── server.js
  ├── config/
  │    └── db.js
  ├── models/
  │    └── Post.js
  ├── routes/
  │    └── postRoutes.js
  ├── .env.example
  └── README.md
```

## Setup (Local)

1. Clone the repo or extract the ZIP.
2. Install dependencies:
```bash
npm install
```
3. Create a `.env` file (copy from `.env.example`) and set `MONGO_URI`.
4. Start the server:
```bash
npm start
```
Server will run on `http://localhost:5000` (or the port in `.env`).

## API Routes

- `GET /posts` — Get all posts
- `GET /posts/:id` — Get single post by ID
- `POST /posts` — Create a post  
  Body (JSON): `{ "title": "My Post", "content": "Body", "author": "Ankit" }`
- `PUT /posts/:id` — Update a post (send any of title/content/author)
- `DELETE /posts/:id` — Delete a post

## Example with curl

Create:
```
curl -X POST http://localhost:5000/posts \
  -H "Content-Type: application/json" \
  -d '{{"title":"Hello","content":"World","author":"Ankit"}}'
```

Get all:
```
curl http://localhost:5000/posts
```

## Notes
- Do **not** commit your `.env` file. Use `.env.example` for guidance.
- If you want, I can also provide Postman collection and deployment steps (Render/Vercel/Railway).

