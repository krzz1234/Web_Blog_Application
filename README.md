# 📝 Simple Blog Web Application

A clean, full-stack blog application built with a separate front-end and a RESTful API backend using Node.js and Express. This project serves as a great example of a two-part web application architecture.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-9B59B6?style=for-the-badge&logo=ejs&logoColor=white)

---

## ✨ Features

- ✅ **Full CRUD Functionality**: Create, Read, Update, and Delete blog posts.
- ✅ **Two-Server Architecture**: A dedicated front-end server that communicates with a separate backend API.
- ✅ **RESTful API**: A well-structured API for managing blog post data.
- ✅ **Dynamic Rendering**: Uses EJS for server-side rendering of blog posts.
- ✅ **Modern & Clean UI**: A simple and intuitive user interface styled with custom CSS.

---

## 🛠️ How It Works

This application operates with two distinct servers running concurrently:

1.  **Backend API Server (`index.js`)**:
    -   Runs on `localhost:4000`.
    -   Built with Express.js, it exposes a set of RESTful endpoints to perform CRUD operations.
    -   Acts as the single source of truth for all blog post data, which is stored in-memory for this project.

2.  **Frontend Server (`server.js`)**:
    -   Runs on `localhost:3000`.
    -   Also built with Express.js, its primary role is to serve the user-facing pages.
    -   It uses **EJS** templates to dynamically render HTML.
    -   When a user visits the site, this server makes HTTP requests (using `axios`) to the Backend API to fetch, create, update, or delete posts, and then renders the results.

---

## 📁 Project Structure
```
.
├── public/
│   └── styles/
│       └── main.css      # All styles for the application
├── views/
│   ├── index.ejs         # Main page template to display all posts
│   └── modify.ejs        # Template for creating and editing posts
├── index.js              # The backend REST API server
├── server.js             # The front-end server
├── package.json          # Project dependencies and scripts
└── README.md             # This file
```
## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

Make sure you have the following installed:
- [Node.js](https://nodejs.org/en/) (which includes npm)

### Installation & Setup

1.  **Clone the Repository**
    ```bash
    git clone <your-repository-url>
    cd <repository-directory>
    ```

2.  **Install Dependencies**
    Install the required npm packages for the project.
    ```bash
    npm install
    ```

3.  **Start the Backend API Server**
    In your terminal, run the following command:
    ```bash
    node index.js
    ```
    The API will now be running on `http://localhost:4000`.

4.  **Start the Frontend Server**
    Open a **new terminal window** and run this command:
    ```bash
    node server.js
    ```
    The frontend will now be running on `http://localhost:3000`.

5.  **Launch the Application**
    Open your browser and navigate to `http://localhost:3000`. Enjoy!

---

## 📡 API Endpoints

The backend API provides the following endpoints for managing posts:

| Method | Endpoint          | Description                                  |
| :----- | :---------------- | :------------------------------------------- |
| `GET`  | `/posts`          | Retrieves all blog posts.                    |
| `GET`  | `/posts/:id`      | Retrieves a single post by its ID.           |
| `POST` | `/posts`          | Creates a new blog post.                     |
| `PATCH`| `/posts/:id`      | Partially updates an existing post by its ID.|
| `DELETE`| `/posts/:id`     | Deletes a post by its ID.                    |

---

## 🔮 Future Improvements

Here are some ideas for enhancing the application:

-   [ ] **Connect to a Database**: Replace the in-memory data store with a persistent database like MongoDB or PostgreSQL.
-   [ ] **User Authentication**: Add user accounts and authentication to allow multiple authors.
-   [ ] **Add a Search Feature**: Implement a search bar to find posts by title or content.
-   [ ] **Pagination**: If the number of posts grows, add pagination to the main page.
-   [ ] **Rich Text Editor**: Replace the basic `<textarea>` with a rich text editor for better post formatting.

---

## 📄 License

This project is licensed under the ISC License. See the `package.json` file for details.
