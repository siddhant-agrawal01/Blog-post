# Blog Post CRUD Application(https://blog-post-green.vercel.app/)

## Overview

This project is a Blog Post CRUD application built with the latest technologies. It allows users to perform CRUD (Create, Read, Update, Delete) operations on blog posts. The application uses Next.js 14 for the framework, Tailwind CSS for styling, Acenternity UI for styling, Prisma for ORM, and PostgreSQL for the database. The PostgreSQL database is hosted using NeonDB's free tier services.

## Technologies Used

- **Next.js 14**: A React framework for building server-side rendered (SSR) and static web applications.
- **Tailwind CSS**: A utility-first CSS framework for styling.
- **Acenternity UI**: A UI component library for faster design and development.
- **Prisma**: An ORM (Object-Relational Mapping) tool for interacting with the PostgreSQL database.
- **PostgreSQL**: A powerful, open-source relational database system.
- **NeonDB**: Provides free-tier PostgreSQL database services.

## Features

- **Read Posts**: View a list of blog posts to read.
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
git clone https://github.com/siddhant-agrawal01/Blog-post.git
cd Blog-post
```

### Install Dependencies

```bash
npm install
```

### DATABASE CONNECTION

To connect your application to a PostgreSQL database using NeonDB (or any PostgreSQL database), you need to follow several steps to ensure everything is configured correctly. Here’s a comprehensive guide:

### 1. **Create a PostgreSQL Database**

- **Using NeonDB**:
  1. Sign up or log in to [NeonDB](https://neon.tech/).
  2. Create a new PostgreSQL database instance.
  3. Note the connection details provided, including the host, port, username, password, and database name.

### 2. **Configure Environment Variables**

You need to set up environment variables to securely provide database credentials to your application. For a Next.js project, follow these steps:

1. **Create a `.env` File**:
   In the root directory of your project, create a file named `.env`.

2. **Add Database Connection URL**:
   Add your PostgreSQL connection string to the `.env` file. Replace the placeholders with your actual database credentials:

   ```plaintext
   DATABASE_URL=postgresql://username:password@host:port/database?sslmode=require
   ```


### 3. **Set Up Prisma**

1. **Install Prisma**:
   Ensure Prisma is installed in your project:

   ```bash
   npm install @prisma/client prisma
   ```

2. **Configure Prisma**:
   In your `prisma` folder, open the `schema.prisma` file and configure the datasource to use the `DATABASE_URL` environment variable:

   ```prisma
   datasource db {
     provider = "postgresql"
     url      = env("DATABASE_URL")
   }
   ```

3. **Generate Prisma Client**:
   After configuring your `schema.prisma`, run the following command to generate the Prisma Client:

   ```bash
   npx prisma generate
   ```

4. **Run Database Migrations**:
   If you have any migrations, run:

   ```bash
   npx prisma migrate dev
   ```

### 4. **Verify Database Connection**

1. **Start Your Application**:
   Run your application to ensure it can connect to the database:

   ```bash
   npm run dev
   ```

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
   docker run -p 3000:3000  blog-app
   ```

3. **Access the Application**

   Open your browser and navigate to `http://localhost:3000`.


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

### Note 
The project is build in my Linux ubuntu 24.04LTS machine if you face problem running locally try running with docker(specially windows users).

