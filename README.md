
# DevOps Demo App

A simple Python Flask web application packaged and run using Docker.

## Features

- Returns a JSON response from the home endpoint (`/`)
- Provides a health endpoint (`/health`)
- Runs inside a Docker container
- Exposes application port 5000

## Technologies Used

- Python 3.13
- Flask
- Docker
- Git and GitHub

## Run Locally

Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

Start the application:

```bash
python app.py
```

Open http://localhost:5000

## Run with Docker

Build the image:

```bash
docker build -t devops-demo-app:1.0 .
```

Start the container:

```bash
docker run -d --name devops-demo-container -p 5000:5000 devops-demo-app:1.0
```

Open http://localhost:5000

## Health Check

Open http://localhost:5000/health

Expected response:

```json
{"status": "healthy"}
```

## Learning Outcomes

- Built a basic Flask web application
- Created a Docker image
- Ran and inspected a container
- Tested HTTP endpoints and inspected application logs
