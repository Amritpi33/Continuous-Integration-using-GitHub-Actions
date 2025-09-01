# CPNT-302 – Continuous Integration with GitHub Actions

##  Overview
This project demonstrates **Continuous Integration (CI)** using **GitHub Actions**.  
The workflow automates building and testing a Node.js web app, then containerizes it with Docker and publishes the image to **Docker Hub**.  

Key Features:
- Node.js application containerized with Docker  
- Automated builds/tests triggered by GitHub commits  
- Secure credential storage using **GitHub Actions Secrets**  
- Successful deployment and validation of containerized app  

---

##  Equipment & Tools
- Windows PC with VMware Workstation  
- Ubuntu 22.04 VM  
- Git & GitHub account  
- Node.js runtime + npm  
- Docker Engine & Docker Hub account  

---

##  Implementation Steps

### **1. Push Code to GitHub**
- Created Node.js project and pushed repo to GitHub.  
📷 ![Push Code](push%20code%20to%20github.png)

---

### **2. Build & Test Locally**
- Ran `npm install`, `npm test`, and `npm start` to validate app locally.  
📷 ![npm Tested](npm%20tested%20and%20running.png)

---

### **3. Configure GitHub Actions**
- Created `.github/workflows/main.yml`  
- Job 1: Build & Test Node.js app  
- Job 2: Build & Push Docker image (runs only if Job 1 succeeds).  

📷 ![Build & Push Docker Image](build%20and%20push%20docker%20image.png)

---

### **4. Verify Workflow & Publish**
- Verified both jobs in GitHub Actions succeeded.  
- Docker image published to Docker Hub repository.  

📷 ![Removed Local Container](removed%20local%20container%20image.png)

---

### **5. Run Containerized Web App**
- Pulled image from Docker Hub.  
- Ran container and accessed web app at `http://localhost:3000`.  

📷 ![Web Browser Access](web%20browser%20to%20access%20the%20web%20application.png)

---

##  Marking Criteria (Self-Evaluation)
- Demo 1: Push Code to GitHub  
-  Demo 2: GitHub Actions Secrets configured  
-  Demo 3: Workflow Triggered successfully  
-  Demo 4: Build & Test Job succeeded  
-  Demo 5: Image published to Docker Hub  
-  Demo 6: Container pulled & app accessed  

**Total:** /100  

---

##  Resources
- [Containerize a Node.js application](https://docs.docker.com/language/nodejs/containerize/)  
- [GitHub Actions Docs – Node.js](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-nodejs)  
- [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)  
- [Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet/)  

---

##  Lessons Learned
- Automated workflows reduce manual testing and publishing steps.  
- GitHub Secrets ensure **secure handling** of Docker Hub credentials.  
- Understood CI pipelines and job dependencies in GitHub Actions.  
- Integrated **Node.js + Docker + GitHub Actions + Docker Hub** end-to-end.  

