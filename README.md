# CI/CD Pipeline for Flask Application

## Project Overview
This project is a simple CI/CD pipeline for a Flask application using Jenkins, Docker, and Kubernetes. The pipeline includes stages for building, testing, Dockerizing, and deploying the application to a Kubernetes cluster.

## File Structure
- `app.py` - Flask application.
- `Dockerfile` - Defines the Docker image for the app.
- `Jenkinsfile` - Jenkins pipeline configuration.
- `k8s/deployment.yaml` - Kubernetes deployment and service configuration.
- `tests/test_app.py` - Unit test for the Flask app.

## Setup Instructions

1. **Docker Setup**:
    - Build and push the Docker image.
    ```bash
    docker build -t your_dockerhub_username/flask_app .
    docker push your_dockerhub_username/flask_app
    ```

2. **Jenkins Pipeline Setup**:
    - Add the `dockerhub-credentials` in Jenkins for Docker authentication.
    - Add `kubeconfig` file as a Jenkins secret for Kubernetes access.

3. **Run the Pipeline**:
    - Trigger the Jenkins pipeline to build, test, Dockerize, and deploy the Flask app.

## Testing
To run tests locally:
```bash
pip install -r requirements.txt
pytest tests
