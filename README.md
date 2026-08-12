# Jenkins CI/CD Demo Project

My first serious project with Jenkins. This is where I learned how to build automated pipelines, run tests automatically, and deploy without touching the server manually.

## What this is

A demonstration of CI/CD pipeline setup using Jenkins. It covers the basics of continuous integration and continuous deployment.

## Technology stack

- **CI/CD**: Jenkins
- **Frontend**: HTML
- **Version Control**: Git

## What the pipeline does

1. **Triggers on push** — Every time code is pushed, Jenkins wakes up
2. **Pulls latest code** — Gets the fresh version from the repository
3. **Runs tests** — Automated tests to catch issues early
4. **Builds the application** — Compiles and packages everything
5. **Deploys** — Pushes to the server automatically

## How it's set up

The Jenkins pipeline is defined in `Jenkinsfile` at the root of the repository.

### Pipeline stages

```
Source Control → Build → Test → Deploy → Notify
```

## Getting started with Jenkins

1. Install Jenkins on your machine or server
2. Set up a new pipeline job in Jenkins
3. Point it to this repository
4. Jenkins will automatically find the `Jenkinsfile`
5. Configure your deployment target

## What I learned

- How Jenkins pipelines work
- Declarative vs scripted pipelines
- Webhook integration with GitHub
- Build artifacts and deployment
- Logging and debugging pipeline issues
- How automation saves manual work

## The pipeline file

Everything is in `Jenkinsfile`. It's readable and well-commented so you can understand each step.

## Next things to explore

- Add docker image building to the pipeline
- Deploy to a cloud platform automatically
- Add more sophisticated testing stages
- Implement rollback strategies
- Add notifications (Slack, Email)

---

Last updated: February 2026