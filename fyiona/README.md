# Fyiona

**Fyiona** is a Django-based backend API project envisioned as a Tinder-inspired social platform for our local market. The current version lays the foundation with essential features like user management, post creation, commenting, and a feed of random posts, while plans for additional Tinder-like functionalities (swiping, matching, etc.) are on the roadmap.

---

## Overview

Fyiona is designed to provide a robust backend for a social platform where users can create and share content, comment on posts, and view a feed of posts from other users. Although the current implementation focuses on basic social features, the ultimate goal is to introduce Tinder-inspired interactions tailored for our local community.

Key components include:

- **User Management:**  
  Custom user authentication using JWT, along with endpoints for registration, login, profile updates, and password management.
  
- **Posts & Comments:**  
  Users can create posts with media attachments and leave comments. The API supports creating, updating, retrieving, and deleting posts and comments.
  
- **Feed Generation:**  
  A feed endpoint retrieves a random selection of posts for the user, forming the basis for a dynamic and engaging experience.

- **API Documentation:**  
  Detailed API endpoints and usage instructions are documented using the OpenAPI standard. You can refer to the `documentation.txt` file in the repository for a comprehensive overview.

---

## Features

- **User Management:**  
  - Registration and login (via email or phone number)
  - Profile updates and password management
  
- **Content Posting:**  
  - Create, update, and delete posts with media attachments
  - Detailed post retrieval along with associated comments
  
- **Comments:**  
  - Create and delete comments on posts
  
- **Feed:**  
  - Retrieve a dynamic feed of posts (randomly selected)

- **Planned Enhancements:**  
  - Tinder-inspired features such as swiping and matching
  - Stories and messaging capabilities

---

## Installation

Fyiona can be set up either in a local development environment or using Docker. Follow the instructions below based on your preferred method.

### Local Development Setup

1. **Clone the Repository:**
  ```
  git clone https://github.com/your-username/fyiona.git
  cd fyiona
  ```

2. **Create and Activate a Virtual Environment:**
  ```
  python3 -m venv env
  source env/bin/activate  # On Windows: env\Scripts\activate
  ```

3. **Install Dependencies:**
  ```
  pip install -r requirements.txt
  ```

4. **Configure Environment Variables: Create a .env file in the project root with the following (update values as needed):**
  ```
  SECRET_KEY=your-secret-key
  DEBUG=True
  DOMAIN_NAME=your-domain.com
  POSTGRES_DB=your_db_name
  POSTGRES_USER=your_db_user
  POSTGRES_PASSWORD=your_db_password
  POSTGRES_SERVER=localhost
  EMAIL_HOST=your_email_host
  EMAIL_PORT=your_email_port
  EMAIL_HOST_USER=your_email_user
  EMAIL_HOST_PASSWORD=your_email_password
  EMAIL_USE_TLS=True
  ```
5. **Apply Migrations:**
  ```
  python manage.py migrate
  ```

6. **Run the Development Server:**

  ```
  python manage.py runserver
  ```

  Access the API at http://127.0.0.1:8000/


### Docker Setup

The project is containerized with Docker for a production-ready environment.

    Ensure Docker and Docker Compose are Installed.
    Configure the .env File: As described above, create a .env file in the project root with your configuration values.
    Build and Run the Containers:
    docker-compose up --build

    This command will:
        Build the Django application container.
        Set up a PostgreSQL database container.
        Start an Nginx container for reverse proxy and SSL certificate management.

    Access the Application: The application will be available at http://localhost:8080/ (or via your configured domain).

### API Documentation

Fyiona’s API is documented using the OpenAPI 3.0 specification. The documentation includes details for:

    User Endpoints: Registration, login, profile management, password reset, and more.
    Post Endpoints: Create, update, retrieve, search, and delete posts.
    Comment Endpoints: Create and delete comments.
    Feed Endpoint: Retrieve a random selection of posts.

You can view the full API documentation in the documentation.txt file in the repository. Developers can use this document as a guide to integrate with Fyiona’s backend services.

### Running the Tests

(If tests are implemented)
Run the following command to execute the test suite:

```python manage.py test```

### Notes:
```
  Current Status:
  This version of Fyiona provides the core backend functionalities. Tinder-inspired features and other enhancements are planned for future releases.

  Feedback:
  Any feedback or suggestions for improvement are welcome as the project evolves.
```
