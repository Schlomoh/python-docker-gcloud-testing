# Python-Docker-GCloud-Testing

This repository serves as a template for developing Python applications in Docker environments configured to authenticate via Google Cloud's Application Default Credentials. It's designed for developers looking to integrate GCP services seamlessly in both local and production environments.

## Overview

The `python-docker-gcloud-testing` project encapsulates best practices for setting up a Python development environment using Docker, facilitating the use of Google Cloud services through authenticated sessions with Application Default Credentials. This setup ensures that the local development environment mirrors the cloud configuration, reducing discrepancies between development and production.

## Prerequisites

Before you begin, ensure you have the following installed:
- **Docker**: Required for creating and managing your development container.
- **Docker Compose**: Simplifies the management of multi-container Docker applications.
- **Visual Studio Code**: Recommended for editing and managing the project files.
- **Remote - Containers Extension for VS Code**: Allows you to use a Docker container as a full-featured development environment.

## Installation

### Clone the Repository

Start by cloning the repository to your local machine:

```bash
git clone https://github.com/yourusername/python-docker-gcloud-testing.git

cd python-docker-gcloud-testing
```

## Google Cloud Configuration
Set up Google Cloud SDK if not already installed and initialized. See Google's official documentation for guidance.

Log in to your gcloud account and set it as default applicatoin credentials producing the required service account json file.

```bash
gcloud auth application-default login
```

## Development
### Opening the Project
Open the project in Visual Studio Code. You will be prompted by the Remote - Containers extension to reopen the project in a container:

- Select Remote-Containers: Open Folder in Container from the Command Palette 
  `(Ctrl+Shift+P or Cmd+Shift+P).`
  

### Working Inside the Container
Once the container is running, all operations such as running the server, executing scripts, or debugging are performed within the container environment, ensuring consistency across all development stages.

## Features
- **Isolated Development:** Using Docker and Remote - Containers in VS Code isolates your development environment, avoiding conflicts between projects.
- **Integrated GCP Authentication:** Pre-configured to authenticate with Google Cloud services using Application Default Credentials.
- **Python 3.9 Environment:** Leverages the latest stable Python release compatible with numerous libraries and frameworks.

## Contributing
Contributions are welcome! Please fork the repository, make your changes, and submit a pull request to the main branch. For major changes, please open an issue first to discuss what you would like to change.

## Support
For support, email post@moritzbecker.de or raise an issue in the GitHub issue tracker.