# Memory Game with Docker and GitHub Actions

This project is a simple memory game that has been containerized using Docker and automated with GitHub Actions for continuous integration and deployment (CI/CD).

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Running Locally](#running-locally) by [Pulling and Running the Docker Image](#pulling-and-running-the-docker-image)
- [Automation with GitHub Actions](#automation-with-github-actions)


---

## Project Overview
This project is a memory game built using HTML, JavaScript, and CSS. The game has been containerized using Docker, and the process of building and pushing the Docker image to Docker Hub has been automated using GitHub Actions.

---

## Technologies Used
- **Frontend**: HTML, CSS, JavaScript
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Web Server**: Nginx (used in the Docker container)

---

## Getting Started

### Prerequisites
Before running the project, ensure you have the following installed:
- [Docker](https://docs.docker.com/get-docker/)
- [Git](https://git-scm.com/)

### Running Locally

### Pulling and Running the Docker Image
the Docker image of this project is available on Docker Hub, you can pull and run it locally without building it from scratch.

1. Pull the Docker image from Docker Hub:
   ```bash
   docker pull maiaboelmagd/memory-game2:latest
   ```
2. Run the Docker container:
   ```bash
   docker run -d -p 8080:80 maiaboelmagd/memory-game2:latest
   ```
3. Open your browser and go to:
   ```
   http://localhost:8080
   ```
  ##### Note : insure there's no other images or applications using port 8080:80 or use another port( like 8081) .
---

## Automation with GitHub Actions
This project uses GitHub Actions to automate the process of building and pushing the Docker image to Docker Hub whenever changes are pushed to the `main` branch.

### Workflow File
The workflow file (`.github/workflows/docker-publish.yml`) contains the following steps:
1. Checkout the repository.
2. Log in to Docker Hub using GitHub Secrets.
3. Build and push the Docker image.

### How It Works
- Every push to the `main` branch triggers the workflow.
- The Docker image is built and pushed to Docker Hub automatically.

---
---


#### Contributions are welcome! 
---


# Enjoy the game! 🎮
