# `ct-recon` Repository Report

##  Overview

`ct-recon` is a C++ project designed for modular, containerized development and deployment. It integrates modern C++ practices with a streamlined CI/CD pipeline using GitHub Actions and Docker.

---

##  Key Technologies

| Category         | Tools/Technologies                     |
|------------------|----------------------------------------|
| Language         | C++ (C++11 and beyond)                 |
| Build System     | CMake                                  |
| Package Manager  | Conan                                  |
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
![alt text](image.png)

---

##  Local Testing

To run the project locally:

```bash
sh run.sh
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

### CI/CD Workflow Diagram (PlantUML)

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

## Github Link

[Click here for view github repository](https://github.com/Sombaran/ct-recon)
