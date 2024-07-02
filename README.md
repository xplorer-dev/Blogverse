# BlogVerse

Welcome to BlogVerse! This project is an implementation of a blogging platform using a modern tech stack. This README provides an overview of the project, the tech stack used, and instructions for setting up and running the project locally.

## Table of Contents

1. [Tech Stack](#tech-stack)
2. [Features](#features)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
5. [Configuration](#configuration)
6. [Running the Project](#running-the-project)
7. [Project Structure](#project-structure)
8. [Contributing](#contributing)
9. [License](#license)

## Tech Stack

- **Frontend**: React
- **Backend**: Cloudflare Workers
- **Validation**: Zod
- **Language**: TypeScript
- **ORM**: Prisma
- **Database**: PostgreSQL
- **Authentication**: JSON Web Tokens (JWT)

## Features

- User authentication with JWT
- Create, read, update, and delete blog posts
- User profile management
- Input validation with Zod
- Type inference for frontend types
- Connection pooling with Prisma ORM

## Prerequisites

Ensure you have the following installed on your machine:

- Node.js (v14 or higher)
- npm or yarn
- PostgreSQL

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/blogverse.git
    cd blogverse
    ```

2. Install frontend dependencies:

    ```bash
    cd frontend
    npm install
    ```

3. Install backend dependencies:

    ```bash
    cd ../backend
    npm install
    ```

## Configuration

### Environment Variables

Create a `.env` file in the root of the backend directory and add the following environment variables:

```
DATABASE_URL=postgresql://user:password@localhost:5432/blogverse
JWT_SECRET=your_jwt_secret
```

Replace `user`, `password`, and `your_jwt_secret` with your PostgreSQL user, password, and a secret key for JWT respectively.

## Running the Project

### Backend

1. Run the PostgreSQL database:

    ```bash
    sudo service postgresql start
    ```

2. Apply database migrations:

    ```bash
    npx prisma migrate dev
    ```

3. Start the backend server:

    ```bash
    npm start
    ```

### Frontend

1. Start the frontend development server:

    ```bash
    cd frontend
    npm start
    ```

2. Open your browser and navigate to `http://localhost:3000`.

## Project Structure

```bash
blogverse/
├── backend/
│   ├── src/
│   │   ├── index.ts
│   │   ├── routes/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── models/
│   │   └── utils/
│   ├── prisma/
│   │   └── schema.prisma
│   ├── package.json
│   └── tsconfig.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   ├── services/
│   │   └── utils/
│   ├── public/
│   ├── package.json
│   └── tsconfig.json
├── README.md
└── .gitignore
```

## Contributing

We welcome contributions to BlogVerse! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Happy coding! If you have any questions, feel free to open an issue or contact the project maintainers.
