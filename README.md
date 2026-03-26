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

     <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/cdfcda77-dd71-4c70-8364-0399feed8c10" />

   ##  Task 4: Only Push on Main
   
Add a condition so the push step only runs on the main branch — not on feature branches or PRs.

Test it: push to a feature branch and verify the image is built but NOT pushed.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/55c75041-2fad-4184-ba47-1330c690dae2" />

## Task 5: Add a Status Badge

  1. Get the badge URL for your docker-publish workflow from the Actions tab
  2. Add it to your README.md
  3. Push — the badge should show green



