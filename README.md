# Twitter Clone

Twitter Clone is a real-time social media application built on the MERN (MongoDB, Express, React, Node.js) stack. It allows users to share posts, follow other users, like and comment on posts, and receive notifications.

## Branches

- **master**: Contains the deployed production-ready code that is live on the server.
- **main**: Contains the local development version of the code for running on your local machine.

## Features

- User authentication with JWT
- Follow/unfollow users
- Create, like, and comment on posts
- Real-time notifications
- Responsive UI with Tailwind CSS and DaisyUI

## Tech Stack

**Client:** React, Vite, TailwindCSS, DaisyUI

**Server:** Node, Express, MongoDB, Cloudinary, Bcrypt, JWT

## Installation

### Clone the repository
```bash
https://github.com/impushpesh/twitterClone.git
```

### Backend Setup
```bash
cd backend
npm install
npm run dev
```
Configure environment variables in `.env` file.

### Frontend Setup
```bash
cd ../frontend
npm install
npm run dev
```

## Environment Variables
Create a `.env` file in the backend directory with the following variables:

```env
MONGODB_URI=
PORT=5001
JWT_SECRET=
NODE_ENV=development
CLIENT_URL=http://localhost:5173
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
```

## API Reference

### Auth Routes
| Method | Endpoint        | Description               |
|--------|-----------------|---------------------------|
| GET    | `/api/auth/me`  | Get logged-in user info   |
| POST   | `/api/auth/signup` | Register a new user     |
| POST   | `/api/auth/login` | User login               |
| POST   | `/api/auth/logout` | User logout             |

### User Routes
| Method | Endpoint                   | Description                      |
|--------|----------------------------|----------------------------------|
| GET    | `/api/users/profile/:username` | Get user profile               |
| GET    | `/api/users/suggested`    | Get suggested users              |
| POST   | `/api/users/follow/:id`   | Follow/unfollow a user           |
| POST   | `/api/users/update`       | Update user profile              |

### Post Routes
| Method | Endpoint                   | Description                      |
|--------|----------------------------|----------------------------------|
| GET    | `/api/posts/all`          | Get all posts                     |
| GET    | `/api/posts/following`    | Get posts from followed users     |
| GET    | `/api/posts/likes/:id`    | Get liked posts                   |
| GET    | `/api/posts/user/:username` | Get posts by a specific user    |
| POST   | `/api/posts/create`       | Create a new post                 |
| POST   | `/api/posts/like/:id`     | Like/unlike a post                |
| POST   | `/api/posts/comment/:id`  | Comment on a post                 |
| DELETE | `/api/posts/:id`          | Delete a post                     |

### Notification Routes
| Method | Endpoint      | Description                       |
|--------|---------------|-----------------------------------|
| GET    | `/api/notifications` | Get all notifications          |
| DELETE | `/api/notifications` | Delete all notifications       |
