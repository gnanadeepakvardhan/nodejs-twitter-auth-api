# Node.js Twitter Auth API

Hey! 👋 This is a simple backend API that works like a tiny version of Twitter.  
Built with **Node.js**, **Express**, **SQLite**, and **JWT** for authentication.  
Good for learning how real login, auth, followers, tweets, likes, and replies work behind the scenes.

---

## 📌 What’s Inside

- **Register & Login** — create a user, login, get a JWT token.
- **Auth Middleware** — all private routes are protected with JWT. No token = no access.
- **Follow System** — follow/unfollow people (using follower/following tables).
- **Tweets** — post a tweet, get tweets, delete your own.
- **Likes & Replies** — like a tweet, reply to a tweet, see who liked/replied.
- **Feed** — see latest tweets from people you follow (limit 4).

---

## 🗂️ Tech Stack

- Node.js
- Express
- SQLite
- JWT (jsonwebtoken)
- bcrypt for hashing passwords
- Postman for testing

---

## 🔑 API Routes

| Method | Route | What It Does |
| ------ | ----- | ------------- |
| POST | `/register/` | Register a new user |
| POST | `/login/` | Login, get JWT |
| GET | `/user/tweets/feed/` | Get 4 latest tweets from followed users |
| GET | `/user/following/` | Who you follow |
| GET | `/user/followers/` | Who follows you |
| GET | `/tweets/:tweetId/` | Get tweet details (likes, replies, date-time) |
| GET | `/tweets/:tweetId/likes/` | Who liked the tweet |
| GET | `/tweets/:tweetId/replies/` | Replies on the tweet |
| GET | `/user/tweets/` | Get your tweets |
| POST | `/user/tweets/` | Post a new tweet |
| DELETE | `/tweets/:tweetId/` | Delete your tweet |

---

## ⚙️ How to Run

1. Clone this repo  
2. `npm install`  
3. `node app.js`  
4. Open Postman → hit endpoints → use JWT for auth routes

---

## 🧩 DB Structure

This uses **SQLite** with 5 tables:

- `user`
- `follower`
- `tweet`
- `reply`
- `like`

Proper foreign keys, relational queries, joins for followers, likes, feed, replies.

---

## 🤝 Why I Built This

Made this to practice building **secure auth**, **real SQL queries**, and **REST APIs**.  
Good practice if you want to understand how social media backends work.

---

## 📝 Author

**Gnana Deepak Vardhan** — Node.js dev in the making.  
Feel free to fork, use, or suggest improvements!

---

