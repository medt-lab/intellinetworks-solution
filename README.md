# IntelliNetworks Solutions

Professional website for **IntelliNetworks Solutions**.

> Network • Infrastructure • Cybersecurity • DevOps

## 📋 Description

IntelliNetworks Solutions is a professional website presenting services and expertise in:

* Network Engineering
* Cybersecurity
* Infrastructure
* Cloud & DevOps

## 🛠️ Technologies

* HTML5
* CSS3
* JavaScript
* Nginx
* Docker
* Git
* GitHub

## 📁 Project Structure

```text
intellinetworks-solution/
│
├── .git/
├── .gitignore
├── .kilo/
│
├── 50x.html
├── Dockerfile
├── README.md
├── index.html
│
├── css/
│   └── style.css
│
├── js/
│   └── script.js
│
└── images/
    └── favicon.svg
```

## 🌐 Run the Website Locally

The website can be served directly from the local project or through Docker.

### Local project

Open `index.html` in a web browser.

### Docker

Build the Docker image:

```bash
docker build -t intellinetworks-solution:1.3 .
```

Run the container:

```bash
docker run -d \
  --name intellinetworks-web \
  -p 8081:80 \
  intellinetworks-solution:1.3
```

The website is then available at:

```text
http://localhost:8081
```

## 🔍 Docker Verification

Check the running container:

```bash
docker ps
```

Check the container port:

```bash
docker port intellinetworks-web
```

Test the website:

```bash
curl -I http://localhost:8081
```

Expected result:

```text
HTTP/1.1 200 OK
```

View Nginx logs:

```bash
docker logs intellinetworks-web
```

Test the website from inside the container:

```bash
docker exec intellinetworks-web wget -qO- http://localhost
```

## 🐳 Docker Architecture

```text
                 Mac Host
                    │
                    │ HTTP :8081
                    ▼
            ┌─────────────────┐
            │ Docker          │
            │                 │
            │  :8081 → :80    │
            │       │         │
            │       ▼         │
            │  ┌───────────┐  │
            │  │   Nginx   │  │
            │  │ Container  │  │
            │  └─────┬─────┘  │
            │        │        │
            │        ▼        │
            │ /usr/share/     │
            │ nginx/html       │
            └─────────────────┘
                    │
                    ▼
                index.html
```

## 🔀 Git Workflow

The project uses Git for version control and GitHub as the remote repository.

Basic workflow:

```text
Modify
  ↓
git status
  ↓
git add
  ↓
git commit
  ↓
git push
  ↓
GitHub
```

### Main Git Commands

Check the status:

```bash
git status
```

Add changes:

```bash
git add .
```

Create a commit:

```bash
git commit -m "Description of the change"
```

Push to GitHub:

```bash
git push
```

Pull changes from GitHub:

```bash
git pull
```

Display the commit history:

```bash
git log --oneline
```

## 🌿 Branches

The project uses the `main` branch and has also used a `develop` branch for development.

Create a development branch:

```bash
git switch -c develop
```

Switch to another branch:

```bash
git switch main
```

List branches:

```bash
git branch
```

## 📦 Project Versions

### Version 1.0

Initial Docker image of the IntelliNetworks Solutions website.

```text
intellinetworks-solution:1.0
```

### Version 1.1

Updated website and Docker image.

```text
intellinetworks-solution:1.1
```

### Version 1.2

Updated homepage branding.

```text
intellinetworks-solution:1.2
```

### Version 1.3

Project professionalization:

* README documentation
* favicon
* footer branding consistency
* HTML/CSS/JS verification
* Docker documentation

```text
intellinetworks-solution:1.3
```

## 🧪 Tests

HTTP test:

```bash
curl -I http://localhost:8081
```

Test homepage content:

```bash
curl -s http://localhost:8081
```

Test the favicon:

```bash
curl -I http://localhost:8081/images/favicon.svg
```

Check Nginx configuration:

```bash
docker exec intellinetworks-web nginx -T
```

## 🔄 Development Workflow

The complete workflow is:

```text
                  Developer
                      │
                      ▼
                Modify Website
                      │
                      ▼
                  Git Status
                      │
                      ▼
                   Git Add
                      │
                      ▼
                  Git Commit
                      │
                      ▼
                   Git Push
                      │
                      ▼
                    GitHub
                      │
                      ▼
                 Docker Build
                      │
                      ▼
                 Docker Image
                      │
                      ▼
                 Docker Run
                      │
                      ▼
                  Nginx
                      │
                      ▼
              http://localhost:8081
```

## 🎯 DevOps Lab Roadmap

Future steps of the lab:

```text
Git / GitHub              ✅
      ↓
Docker                    ✅
      ↓
Docker Compose            Next
      ↓
GitHub Actions / CI
      ↓
Docker Registry
      ↓
CD / Deployment
      ↓
Monitoring
      ↓
DevSecOps
      ↓
Kubernetes
```

---

**Project:** IntelliNetworks Solutions
**Domain:** Network • Infrastructure • Cybersecurity • DevOps
