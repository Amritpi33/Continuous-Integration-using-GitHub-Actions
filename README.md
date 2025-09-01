# Continuous-Integration-using-GitHub-Actions
Proof-of-concept demonstrating CI using GitHub Actions to build and test a Node.js app, then containerize and publish it to Docker Hub. Includes workflow automation, Dockerfile, and CI/CD validation steps.
# CPNT-302 – Continuous Integration using GitHub Actions

## 📌 Overview
This project demonstrates **Continuous Integration (CI)** using **GitHub Actions**.  
The goal is to automate the build and test process of a simple Node.js web application, and upon success, containerize the app and publish it to **Docker Hub**.  

Key Highlights:
- Node.js application containerized with Docker  
- GitHub Actions workflow to automate build, test, and image publishing  
- Secure usage of GitHub Actions Secrets for Docker Hub credentials  
- Final container image pulled and run successfully from Docker Hub  

---

## ⚙️ Equipment and Materials
- Windows PC with VMware Workstation 16/17  
- Ubuntu Linux 22.04 VM  
- Node.js runtime + npm  
- Docker Engine  
- Git and GitHub account  
- Docker Hub account (with access token for automation)  

---

## 🛠️ Procedure

### Part A – Create Node.js Web App
1. Installed Node.js and npm on Ubuntu VM.  
2. Created `app.js` and Dockerfile for Node.js app.  
3. Verified app locally with `npm install`, `npm test`, and `npm start`.  
4. Initialized Git repo and pushed code to GitHub.  
5. Created Docker Hub repository and generated an **access token** for GitHub Actions.  

📷 *Screenshots:*  
- [Implementation Step 1](implementation-step-1.png)  
- [Implementation Step 2](implementation-step-2.png)  
- [Implementation Step 3](implementation-step-3.png)  
- [Implementation Step 4](implementation-step-4.png)  

---

### Part B – GitHub Actions Workflow
1. Added a workflow file under `.github/workflows/main.yml`.  
2. Configured **Job 1**: Build & Test Node.js App (triggered on push).  
3. Configured **Job 2**: Build & Publish Docker Image to Docker Hub (runs only if Job 1 succeeds).  
4. Stored Docker Hub username + token as **GitHub Actions Secrets**.  
5. Verified successful workflow execution.  

📷 *Screenshots:*  
- [Workflow Files](mariadb%20and%20nodeapp.png)  
- [NodeApp Running in Browser](nodeapp%20running%20in%20browser.png)  

---

### Part C – Demonstration
- **Demo 1:** Pushed commit to GitHub → workflow triggered.  
- **Demo 2:** Verified GitHub Actions Secrets for Docker Hub credentials.  
- **Demo 3:** GitHub Actions build & test job executed.  
- **Demo 4:** Workflow built and published image to Docker Hub.  
- **Demo 5:** Pulled and ran image from Docker Hub → web app accessible at `http://localhost:3000`.  

---

## 📊 Marking Criteria (Self-Evaluation)
- Demo 1: Push Code → ✅  
- Demo 2: GitHub Actions Secrets → ✅  
- Demo 3: Workflow Trigger → ✅  
- Demo 4: Build & Test Job → ✅  
- Demo 5: Publish to Docker Hub → ✅  
- Demo 6: Run Container & Access Web App → ✅  

**Total:** /100  

---

## 📚 Resources
- [Containerize a Node.js application](https://docs.docker.com/language/nodejs/containerize/)  
- [GitHub Actions Docs – Node.js Build & Test](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-nodejs)  
- [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)  
- [GitHub Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet/)  

---

## 🙋 Lessons Learned
- Setting up a **CI pipeline** with GitHub Actions improved automation.  
- Learned how to securely handle credentials using **GitHub Secrets**.  
- Understood job dependencies (build/test before publish).  
- Successfully integrated **Node.js + Docker + GitHub Actions + Docker Hub** for a full CI flow.  

