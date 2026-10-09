# Student Management System (MERN CRUD)

This project completes the practical exam requirements for Create, Read, Update, and Delete using React, Axios, Express, Mongoose, and MongoDB.

## 1. Configure MongoDB

Open `server/.env` and make sure it contains your MongoDB connection string:

```env
MONGO_URI=your_mongodb_connection_string
PORT=5000
```

Keep the real connection string private. If MongoDB Atlas is used, confirm your IP is allowed in Network Access and the database user/password are correct.

## 2. Start the backend

Open a terminal in the `mern-app/server` folder and run:

```bash
npm install
npm start
```

The backend connects to MongoDB before it starts listening at `http://localhost:5000`.

## 3. Start the frontend

Open a second terminal in `mern-app/client` and run:

```bash
npm install
npm run dev
```

Open the Vite URL printed in the terminal (normally `http://localhost:5173`). The frontend defaults to `http://localhost:5000` for the API. To change it, create `client/.env` with `VITE_API_URL=http://localhost:5000`.

## CRUD routes

- `GET /students` — retrieve students from MongoDB
- `POST /students` — create a student
- `PUT /students/:id` — update a student by MongoDB `_id`
- `DELETE /students/:id` — delete a student by MongoDB `_id`

## Final exam checklist

1. Add `Test Student`, course `BSIT`, age `20`; refresh and verify it remains.
2. Edit the same record's age to `21`; refresh and verify the change remains.
3. Delete that record; refresh and verify it stays deleted.
4. Capture screenshots of the form/list, add result, edit result, delete result, and the records in MongoDB Atlas.

Student records are not hard-coded; all records are fetched from MongoDB.
