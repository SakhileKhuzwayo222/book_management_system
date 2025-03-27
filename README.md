

---

# Book & Notes Management System

## Overview

The **Book Management System** is an advanced web application designed to provide users with a comprehensive platform for managing and interacting with their book collection. Combining traditional book management features with annotation capabilities, this system offers a seamless experience for book lovers, students, researchers, librarians, and educators.

Users can track their books, manage genres and authors, make annotations, and organize their library in a way that aligns with their personal learning and reading preferences. Additionally, the system fosters a community by enabling social features like virtual book clubs and shared reading experiences.

Built with **Spring Boot** for the backend and **React.js** for the frontend, this application is ideal for users who want more than just a book tracking system—it is a complete reading and knowledge management platform.

### Key Features

- **Book Management**: Efficiently add, update, and delete books in your collection, including details like title, author, genre, and ISBN.
- **Annotation & Note-Taking**: Make text and voice annotations, write chapter summaries, and even capture handwritten notes using AR.
- **Advanced Book Discovery**: Search and add books by title, author, ISBN, or by scanning the barcode of physical books.
- **Author & Genre Management**: Manage authors' details and categorize books by their respective genres.
- **Personalized Book Tracking**: Organize books by reading status, with custom bookshelves like “To Read,” “Reading,” and “Completed.”
- **Multi-Format Support**: Support for digital books, PDFs, and audiobooks with synchronized annotations across all formats.
- **Social & Community Features**: Engage in virtual book clubs, share curated book lists, and explore book recommendations from other users.
- **Export & Integration**: Export notes and summaries to tools like Notion and Evernote, generate citations, and integrate with other research workflows.
- **User Authentication & Security**: Secure authentication using JWT, ensuring that users’ data is protected.
- **RESTful API & Swagger**: A well-documented API (via Swagger) for backend services, allowing easy integration with other tools.

## Technologies Used

- **Frontend**: React.js (for building the user interface)
- **Backend**: Spring Boot (for managing the server, database interactions, and API)
- **Database**: MySQL (for storing books, authors, genres, and user data)
- **Security**: Spring Security with JWT (for user authentication)
- **API Documentation**: Swagger (for exploring and testing API endpoints)
- **Maven**: Dependency management and build tool for the backend

## Getting Started

Follow these steps to set up and run the application locally.

### Prerequisites

- **Java** 11 or higher
- **Maven**
- **Node.js** and **npm**
- **MySQL** (or any other preferred database) for storing book data

### Backend Setup (Spring Boot)

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/book-management-system.git
   cd book-management-system/backend
   ```

2. Install the required dependencies:

   ```bash
   mvn clean install
   ```

3. Set up your MySQL database (or use an existing database) and configure the connection in `src/main/resources/application.properties`:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/book_management_db
   spring.datasource.username=root
   spring.datasource.password=yourpassword
   spring.jpa.hibernate.ddl-auto=update
   ```

4. Run the Spring Boot application:

   ```bash
   mvn spring-boot:run
   ```

   The backend will start on `http://localhost:8080`.

### Frontend Setup (React.js)

1. Go to the frontend folder:

   ```bash
   cd ../frontend
   ```

2. Install the required dependencies:

   ```bash
   npm install
   ```

3. Start the React app:

   ```bash
   npm start
   ```

   The frontend will run on `http://localhost:3000`.

4. Ensure that the frontend is correctly connected to the backend, and that API endpoints are properly configured in the React app.

### Swagger API Documentation

You can test and explore the RESTful API endpoints using **Swagger** at `http://localhost:8080/swagger-ui.html` once the backend is running.

### Database Schema

The database consists of three main tables:

- **Books**: Stores information about each book, including title, author, and genre.
- **Authors**: Stores information about authors.
- **Genres**: Stores different book genres (e.g., Fiction, Non-fiction).
- **Users**: Stores user profile information for authentication and personalized experience.

## Authentication

The system uses JWT (JSON Web Token) for secure authentication. To get started:

1. Register a new user by sending a POST request to `/api/auth/register`.
2. Log in using the POST `/api/auth/login` endpoint to receive a JWT token.
3. Use the received token for authentication in subsequent API requests by adding it to the `Authorization` header as `Bearer <token>`.

## Directory Structure

```
/backend
├── /config               # Spring Boot configurations
├── /controllers          # API Controllers (Endpoints)
├── /models               # Data models (Entity classes)
├── /repositories         # Data repositories (Database queries)
├── /services             # Business logic (Services)
├── /security             # Security and authentication classes
├── /swagger              # Swagger API documentation setup
├── /application.properties # Application configuration
├── /pom.xml              # Maven build file
├── /src                  # Java source files
└── /target               # Compiled application files (generated after build)

/frontend
├── /public               # Static files (HTML, images)
├── /src
│   ├── /components       # React components
│   ├── /services         # API services
│   ├── /App.js           # Main entry point
│   └── /index.js         # React DOM entry point
├── /package.json         # Node.js dependencies and scripts
└── /node_modules         # Installed npm modules
```

## Contributing

We welcome contributions to the project! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push your branch (`git push origin feature/your-feature`).
5. Open a pull request and describe your changes.

## License

This project is licensed under the MIT License.

## Contact

If you have any questions, feel free to reach out to me via GitHub or email me at Sakhilekhuzwayo454@gmail.com.

---
