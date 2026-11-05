<h1 align="center">Hi, I'm Piyush Kasle</h1>

<p align="center">
  Backend and full stack engineer · MS Software Engineering, Florida Institute of Technology
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1200&color=2F81F7&center=true&vCenter=true&width=620&lines=Backend+and+full+stack+engineer;MS+Software+Engineering%2C+FIT+(May+2026);ML+serving+and+drift+monitoring+for+a+health+center+app;Available+to+start+immediately" alt="Backend and full stack engineer. MS Software Engineering, FIT. Available to start immediately." />
</p>

<p align="center">
  I build backend and full stack systems, with a lean toward the infrastructure around ML: serving, deployment and monitoring.
</p>

<p align="center">
  <a href="mailto:kaslepiyush07@gmail.com"><img src="https://img.shields.io/badge/Email-kaslepiyush07%40gmail.com-blue?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://www.linkedin.com/in/piyush-kasle"><img src="https://img.shields.io/badge/LinkedIn-Piyush%20Kasle-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=python,java,js,nodejs,express,fastapi,flask,react,postgres,mysql,redis,docker,aws,githubactions,linux,pytorch,git&theme=dark&perline=9" />
    <source media="(prefers-color-scheme: light)" srcset="https://skillicons.dev/icons?i=python,java,js,nodejs,express,fastapi,flask,react,postgres,mysql,redis,docker,aws,githubactions,linux,pytorch,git&theme=light&perline=9" />
    <img src="https://skillicons.dev/icons?i=python,java,js,nodejs,express,fastapi,flask,react,postgres,mysql,redis,docker,aws,githubactions,linux,pytorch,git&perline=9" alt="Python, Java, JavaScript, Node.js, Express, FastAPI, Flask, React, PostgreSQL, MySQL, Redis, Docker, AWS, GitHub Actions, Linux, PyTorch, Git" />
  </picture>
</p>

---

## Projects

### [Mental Health MLOps](https://github.com/HumbleFool02/mental-health-mlops)

ML side of a university health center's student check in app: a DistilBERT classifier served with FastAPI on AWS, with drift monitoring and a dashboard.

[![Tests](https://github.com/HumbleFool02/mental-health-mlops/actions/workflows/test.yml/badge.svg)](https://github.com/HumbleFool02/mental-health-mlops/actions/workflows/test.yml)
[![Docker Build and Push](https://github.com/HumbleFool02/mental-health-mlops/actions/workflows/docker-build.yml/badge.svg)](https://github.com/HumbleFool02/mental-health-mlops/actions/workflows/docker-build.yml)

<details>
<summary><b>Architecture</b></summary>

```mermaid
graph LR
  A[Student check in app] --> B[FastAPI on EC2]
  B --> C[DistilBERT classifier]
  C --> D[(PostgreSQL logs)]
  D --> E[Drift monitor]
  E --> F[Streamlit dashboard]
  S[(S3 model store)] --> G[Docker build]
  G --> B
```

</details>

### [Smart Parking Management System](https://github.com/HumbleFool02/Parking-Management-Sytem)

Campus smart parking: YOLOv8 slot detection on camera footage plus a Flask booking app.

<details>
<summary><b>Architecture</b></summary>

```mermaid
graph LR
  A[Campus camera feed] --> B[YOLOv8 and OpenCV detection]
  B --> C[Slot status]
  C --> D[Flask booking app]
  U[Users] --> D
  D --> E[(Database)]
```

</details>

### [Security Shift Manager](https://github.com/HumbleFool02/security-shift-manager)

Three role Flask app for scheduling a campus security workforce: fair roster generation, leave workflow and payroll.

<details>
<summary><b>Architecture</b></summary>

```mermaid
graph LR
  M[Manager] --> F[Flask app]
  S[Security staff] --> F
  A[Admin] --> F
  F --> R[Roster generator]
  F --> P[Payroll]
  F --> O[SQLAlchemy]
  O --> DB[(MySQL)]
```

</details>
