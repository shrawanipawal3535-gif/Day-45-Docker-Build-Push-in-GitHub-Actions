# Day-45-Docker-Build-Push-in-GitHub-Actions

## Challenge Tasks

### Task 1: Prepare

   1. Use the app you Dockerized on Day 36 (or any simple Dockerfile)
   2. Add the Dockerfile to your github-actions-practice repo (or create a minimal one)
   3. Make sure DOCKER_USERNAME and DOCKER_TOKEN secrets are set from Day 44

  <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/5218f136-ae95-4680-aec6-e8920ed7989c" />

 ##  Task 2: Build the Docker Image in CI
 
Create .github/workflows/docker-publish.yml that:

   1. Triggers on push to main
  2. Checks out the code
  3. Builds the Docker image and tags it

     <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/1d8cf17d-4157-480e-8653-a2d98fc2d9e1" />

     ## Task 3: Push to Docker Hub
     
Add steps to:

  1. Log in to Docker Hub using your secrets
  2. Tag the image as username/repo:latest and also username/repo:sha-<short-commit-hash>
  3. Push both tags
