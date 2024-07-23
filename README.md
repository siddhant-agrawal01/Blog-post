# Blog Post CRUD Application

## Overview

This project is a Blog Post CRUD application built with the latest technologies. It allows users to perform CRUD (Create, Read, Update, Delete) operations on blog posts. The application leverages Next.js 14 for the framework, Tailwind CSS for styling, Acenternity UI for components, Prisma for ORM, and PostgreSQL for the database. The PostgreSQL database is hosted using NeonDB's free tier services.

## Technologies Used

- **Next.js 14**: A React framework for building server-side rendered (SSR) and static web applications.
- **Tailwind CSS**: A utility-first CSS framework for styling.
- **Acenternity UI**: A UI component library for faster design and development.
- **Prisma**: An ORM (Object-Relational Mapping) tool for interacting with the PostgreSQL database.
- **PostgreSQL**: A powerful, open-source relational database system.
- **NeonDB**: Provides free-tier PostgreSQL database services.

## Features

- **Read Posts**: View a list of blog posts with options to read more details.
- **Create Post**: Add new blog posts with a title and content.
- **Update Post**: Edit existing blog posts.
- **Delete Post**: Remove blog posts from the application.
- **Next.js File-Based Routing**: Utilize Next.js's file-based routing for easy navigation.
- **App Routing**: Leverage Next.js's app routing features for improved organization.
- **Server-Side Rendering**: Enhance performance and SEO with server-side rendering.

## Getting Started

Follow these steps to run the project locally:

### Prerequisites

- **Node.js**: Ensure you have Node.js installed. You can download it from [nodejs.org](https://nodejs.org/).
- **Docker**: Docker should be installed and running on your machine. Download from [docker.com](https://www.docker.com/).

### Clone the Repository

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a `.env` file in the root directory of the project and add the following environment variables:

```
DATABASE_URL=postgresql://your-username:your-password@ep-your-database-url/your-database-name?sslmode=require
```

Replace the placeholders with your actual database credentials from NeonDB.

### Running Locally

#### Without Docker

1. **Run the Development Server**

   ```bash
   npm run dev
   ```

2. **Access the Application**

   Open your browser and navigate to `http://localhost:3000`.

#### With Docker

1. **Build the Docker Image**

   ```bash
   docker build -t blog-app .
   ```

2. **Run the Docker Container**

   ```bash
   docker run -p 3000:3000 --env-file .env blog-app
   ```

3. **Access the Application**

   Open your browser and navigate to `http://localhost:3000`.

### Running Tests

To run tests, use the following command:

```bash
npm test
```

### Building for Production

To build the application for production, use:

```bash
npm run build
```

Then you can start the production server with:

```bash
npm start
```

### Deployment

For deployment, follow the instructions provided by your hosting provider. This project is compatible with platforms like Vercel and other cloud providers.

### Project Structure

- **`pages/`**: Contains the file-based routes for Next.js.
- **`components/`**: Reusable UI components.
- **`prisma/`**: Prisma schema and migration files.
- **`public/`**: Static assets like images.
- **`styles/`**: Tailwind CSS configuration and other styles.

### Troubleshooting

- **Database Connection Issues**: Ensure that your `DATABASE_URL` in the `.env` file is correct and that your NeonDB database is accessible.
- **Build Errors**: Make sure all dependencies are properly installed and that there are no syntax errors in your code.

### Contributing

If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Create a new Pull Request.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to modify any sections as needed to better fit your project specifics!
