# Npontu DevSecOps Internship Assignment

### Project Overview

This project was developed as part of the DevSecOps Officer Internship
application at Npontu Technologies.

The project demonstrates the development, testing, containerization,
continuous integration, continuous deployment, and staging deployment
of a simple Flask web application.

### Technologies Used

1. Python 3.12
2. Flask
3. Pytest
4. Docker
5. Git
6. GitHub
7. GitHub Actions
8. Render
9. Linux / WSL

### Application

The application is a simple Flask web application with two endpoints:

- / returns a message confirming that the application is running.
- /health provides a basic health check for the application.

### Testing

The application includes automated tests written using Pytest.

The tests verify that the application's main and health check endpoints
return the expected responses.

Run the tests with:
pytest

The tests currently pass successfully.


### Docker

The application is containerized using Docker.

Build the Docker image with:
docker build -t npontu-devsecops .

Run the container with:
docker run -d -p 5000:5000 --name npontu-app npontu-devsecops

The application can then be accessed at:
http://localhost:5000


### CI/CD Pipeline

GitHub Actions is used to automate the CI/CD process.

The pipeline performs the following steps:

1. Runs the automated tests.
2. Builds the Docker image if the tests pass.
3. Deploys the application to the Render staging environment if the Docker build succeeds.

This ensures that failed tests prevent the application from progressing
to the build and deployment stages.

### Staging Environment

The application is deployed to a Render staging environment.

Staging URL:
https://npontu-devsecops.onrender.com

Health check:
https://npontu-devsecops.onrender.com/health

The health endpoint returns the application's current health status.