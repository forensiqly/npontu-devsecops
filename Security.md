## Npontu DevSecOps Internship Assignment

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


### Security Vulnerability

#### Hardcoded Secrets:

A common security vulnerability in software development is hardcoding
secrets such as API keys, passwords or access tokens directly in source
code.

For demonstration purposes, security_example.py contains a fake API
key directly in the source code. This demonstrates what should not be
done in a real application.

If a real credential were hardcoded and the repository became publicly
accessible or was accessed by an unauthorized person, the credential
could be exposed and potentially misused.

#### Mitigation:

The secure approach is to keep secrets outside the source code and
provide them through environment variables or a secure secrets
management system.

The secure example in security_example_secure.py retrieves the value
from an environment variable:

python
import os

API_KEY = os.environ.get("API_KEY")
