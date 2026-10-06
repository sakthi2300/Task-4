Task 4 - Version-Controlled DevOps Project with Git
Overview
This project was completed as part of the DevOps Internship Task 4. The objective is to demonstrate Git and GitHub best practices, including repository management, branching, commits, pull requests, .gitignore, and documentation.
Technologies Used
•	Git
•	GitHub
•	Node.js
•	Express.js
•	Docker
•	GitHub Actions
•	Docker Hub
Project Structure
Task-4/
├── .github/
│   └── workflows/
│       └── main.yml
├── .gitignore
├── .dockerignore
├── Dockerfile
├── package.json
├── package-lock.json
├── README.md
└── server.js
Application
This project contains a lightweight Node.js application using Express.js.
Endpoints
•	GET /
Returns: Hello! Node.js CI/CD is working.
•	GET /health
Returns: { "status": "OK" }
Git Branching Strategy
The project follows a feature-based Git workflow.
•	main - Production-ready branch
•	dev - Development and integration branch
•	feature/add-health-endpoint - Feature development branch
Git Workflow
feature/add-health-endpoint
            |
            | Pull Request
            v
           dev
            |
            | Pull Request
            v
           main
Git Workflow Demonstrated
1. Initialized a Git repository.
2. Created the main branch.
3. Created the dev branch.
4. Created a feature branch.
5. Made meaningful Git commits.
6. Pushed branches to GitHub.
7. Created a Pull Request from the feature branch to dev.
8. Merged the feature branch into dev.
9. Created a Pull Request from dev to main.
10. Merged dev into main.
11. Added a .gitignore file.
12. Maintained project documentation using Markdown.
Pull Requests
Pull Request 1
feature/add-health-endpoint → dev
Purpose: Add the /health endpoint and demonstrate feature-branch development and Pull Request based merging.
Pull Request 2
dev → main
Purpose: Promote tested development changes to the production branch and demonstrate the complete Git workflow.
.gitignore
The project uses .gitignore to prevent unnecessary or sensitive files from being committed.
node_modules/
.env
*.log
Docker
The project includes a Dockerfile for containerizing the Node.js application.
Build: docker build -t task-4-nodejs .
Run: docker run -d -p 3000:3000 --name task-4-app task-4-nodejs
Application: http://localhost:3000
Health check: http://localhost:3000/health
CI/CD
A GitHub Actions workflow is included in .github/workflows/main.yml. The workflow demonstrates automated CI/CD using GitHub Actions and Docker.
Git Commands Used
git init
git branch -m main
git add .
git commit
git branch
git checkout -b dev
git checkout -b feature/add-health-endpoint
git push
git pull
git log
git status
Learning Outcomes
•	Git version control
•	GitHub repository management
•	Branching strategies
•	Feature branches
•	Pull Requests
•	Branch merging
•	Commit management
•	.gitignore
•	GitHub Actions
•	Docker integration
•	DevOps workflow
Repository
GitHub Repository: https://github.com/sakthi2300/Task-4
Task Status
Task 4 Completed
Git workflow demonstrated: Git Repository → Feature → Pull Request → Dev → Pull Request → Main
