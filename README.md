

---

# GitHub Implementation with Docker in Flask

This project demonstrates how to implement a **GitHub API** integration in a Flask application, and deploy it using **Docker**. The application allows you to interact with the GitHub API to fetch user profile information and display it in a user-friendly interface.

---

## Features

- **GitHub API Integration**: Fetch user data from GitHub and display it.
- **Flask Backend**: Built with Flask for handling requests and serving the frontend.
- **Dockerized**: The entire application is containerized using Docker for easy deployment and scalability.

---

## Technologies Used

- **Backend**: Flask (Python)
- **API Integration**: GitHub API
- **Containerization**: Docker
- **Environment Variables**: `.env` for storing sensitive data (like GitHub API keys)

---

## Setup Instructions

### Prerequisites

- Docker (installed on your system)
- GitHub API Key (optional, depending on API usage limits)

### Steps to Set Up:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/github-docker-flask.git
   cd github-docker-flask
   ```

2. **Create a `.env` file** in the root directory with the following content (if needed for your application):
   ```env
   GITHUB_API_KEY=your-github-api-key-here
   ```

3. **Build and run the Docker container**:
   - Build the Docker image:
     ```bash
     docker build -t github-flask-app .
     ```
   - Run the Docker container:
     ```bash
     docker run -p 5000:5000 github-flask-app
     ```
   This will start the Flask app, and it will be accessible at [http://localhost:5000](http://localhost:5000).

---

## Endpoints

- `GET /user`: Fetches data for a specific GitHub user. Example usage:
  ```
  /user?username=<github_username>
  ```

---

## Docker Commands

- **Build Docker Image**:
  ```bash
  docker build -t github-flask-app .
  ```

- **Run Docker Container**:
  ```bash
  docker run -p 5000:5000 github-flask-app
  ```

- **Stop Docker Container**:
  ```bash
  docker stop <container_id>
  ```

---

## License

MIT License

---
