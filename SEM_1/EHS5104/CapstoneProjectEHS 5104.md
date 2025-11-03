# Capstone Project - Progress Report - 1


**Author:** Sombaran Gupta<br>
__Email:__ sombaran_pa2507mte92@iitp.ac.in<br>
__Date:__ November 1, 2025<br>
__Location:__ Hyderabad, Telangana, India<br>
__Course:__ EMTech - Cloud Computing<br>
__Subject Code:__ EHS 5104<br>
__Project Type:__ Capstone project with CI/CD with Github Actions


##  Overview

`ct-recon` is a C++ project designed for modular, containerized development and deployment. It integrates modern C++ practices with a streamlined CI/CD pipeline using GitHub Actions and Docker.<br>
GitHub Actions is often chosen over Jenkins for modern CI/CD pipelines because it offers native GitHub integration, easier setup, and lower maintenance overhead—especially for cloud-native and open-source projects.<br>

- The project is hosted on GitHub, so Actions integrates seamlessly.
- No need to manage Jenkins infrastructure.
- YAML workflows are version-controlled alongside the code.
- Docker and Conan steps are easily automated with reusable actions.
- Ideal for a capstone project with limited deployment complexity.
---

## Github Repository

[Click here for view github repository](https://github.com/Sombaran/ct-recon)

---

##  Key Technologies

| Category         | Tools/Technologies                     |
|------------------|----------------------------------------|
| Language         | C++ (C++11 and beyond)                 |
| Build System     | CMake (cmake version 3.22.1)                                 |
| Package Manager  | Conan (Conan version 2.22.1)                                  |
| CI/CD            | GitHub Actions                         |
| Containerization | Docker                                 |
| Scripting        | Shell, Python                          |

---

## Project Structure

- `source/`, `include/`, `test/` – Core source and test files
- `.github/workflows/` – GitHub Actions CI/CD definitions
- `conanfile.py` – Conan dependency management
- `Dockerfile` – Docker image definition
- `run.sh` – Local test script
- ![Project tree structure](https://raw.githubusercontent.com/Sombaran/mtechDocumentsSlides/main/SEM_1/EHS5104/projectTreeStructure.png)

---

## CI/CD Workflow Diagram (PlantUML)

![Click here for sequence diagram](https://raw.githubusercontent.com/Sombaran/mtechDocumentsSlides/main/SEM_1/EHS5104/capstoneSequenceDiagramProgressReport.png)

```plantuml
@startuml
title CI/CD Workflow for ct-recon

actor Developer

box "Build Preparation" #DDDDDD
participant "Conan"
participant "CMake"
end box

box "Source Control" #EEEEEE
participant "GitHub"
end box

box "Automation" #DDDDDD
participant "GitHub Actions"
end box

box "Deployment" #EEEEEE
participant "Docker Hub"
end box

Developer -> Conan : Install dependencies
Conan -> CMake : Generate build files
CMake -> GitHub : Push source code
GitHub -> GitHub Actions : Trigger CI workflow
GitHub Actions -> GitHub Actions : Build Docker image
GitHub Actions -> Docker Hub : Push image
Docker Hub -> Developer : Image available for use

@enduml
```
---

## Docker Usage

```bash
# Build Docker image
docker build . -t ct-recon:<commit-hash-or-version>

# Login to Docker Hub
docker login -u usomgupta

# Run the container
docker run ct-recon:v1 ./ct-recon --input data.txt --verbose

# Shell into the container
docker run -it [image ID] bash

# Link to Docker Hub:
[Docker Hub: usomgupta/ct-recon](https://hub.docker.com/r/usomgupta/ct-recon)
```

---

## CI/CD Workflow

The CI/CD pipeline is triggered on code push and automates the build and deployment process using GitHub Actions and Docker Hub.

- Uses: ubuntu-latest image
- Checkout from repository
- Login into Docker Hub
- Set up Docker Build
- Build and push Docker image
- Upload build artifacts
```yaml
name: CI for docker/build-push-action

on:
  push:
    branches:
      - main

permissions:
  contents: write
  issues: write
  pull-requests: write

jobs:
  build-and-push:
    runs-on: ubuntu-22.04  # Pin to a stable runner version
    permissions:
      contents: write
      pull-requests: read

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4
        with:
          fetch-depth: 1  # Shallow clone for faster checkout

      - name: Log in to Docker Hub
        uses: docker/login-action@v3
        with:
          registry: ${{ env.REGISTRY }}
          username: ${{ secrets.DOCKER_USERNAME }}
          password: ${{ secrets.DOCKERHUB_TOKEN }}

      - name: Set up Docker Buildx
        uses: docker/setup-buildx-action@v3
        with:
          driver: docker-container
          driver-opts: |
            image=moby/buildkit:latest

      - name: Build and push Docker image
        uses: docker/build-push-action@v5
        with:
          builder: ${{ steps.buildx.outputs.name }}
          platforms: linux/amd64  # Use single platform unless multi-arch is needed
          context: .
          push: true
          tags: ${{ secrets.DOCKER_USERNAME }}/repo:v1
          cache-from: type=gha
          cache-to: type=gha,mode=max

      - name: Upload C++ build artifacts
        uses: actions/upload-artifact@v4
        with:
          name: cpp-build-artifacts
          path: |
            build/libmylib.so
            build/myprogram
```

---

##  Local Testing

To run the project locally:

```bash
sh run.sh
```

---

## Testing the docker artifact

![Gemini logo](https://raw.githubusercontent.com/Sombaran/mtechDocumentsSlides/main/SEM_1/EHS5104/testingTheImage.png)

---

## Summary

The CI/CD pipeline is triggered on every code push. It automates build, test, and deployment using GitHub Actions, and publishes Docker images to Docker Hub for seamless distribution.<br>
`Future work`: __I will try to deploy artifacts in jfrog__

---
