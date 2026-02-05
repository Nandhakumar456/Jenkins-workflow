# Jenkins CI/CD Pipeline Workflow

## 📖 Project Overview
This project demonstrates a fully automated **Continuous Integration and Continuous Deployment (CI/CD)** pipeline. The goal is to eliminate manual deployment errors and streamline the software delivery process using industry-standard DevOps tools.

## 🏗️ Architecture Diagram
Below is the visual representation of the automated workflow I designed:

![Jenkins Architecture Diagram](.jenkins-architecture.png.png)

## 🚀 Workflow Steps
As illustrated in the diagram above, the pipeline follows these four critical stages:

1.  **Source Code Management (SCM):**
    * **Action:** The developer writes code and pushes it to the **GitHub Repository**.
    * **Tool:** Git & GitHub.

2.  **Automated Trigger:**
    * **Action:** A **GitHub Webhook** automatically detects the new commit and triggers the build process on the Jenkins server.
    * **Benefit:** Eliminates the need to manually start builds.

3.  **Build & Test:**
    * **Action:** Jenkins pulls the latest code and compiles it (e.g., using **Maven** for Java). It then runs unit tests to ensure code quality.
    * **Logic:** If the tests fail, the pipeline stops, and the developer is notified.

4.  **Deployment:**
    * **Action:** Once the build is successful ("Green Build"), Jenkins automatically deploys the artifact to the target server (e.g., **AWS EC2** or **Apache Tomcat**).

## 🛠️ Tools Used
* **Jenkins:** For automation orchestration.
* **GitHub:** For version control and source code management.
* **Maven:** For building Java applications.
* **Tomcat/AWS:** For hosting the application.
