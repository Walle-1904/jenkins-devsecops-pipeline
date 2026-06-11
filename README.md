 # docker-infra

Infrastructure as code — multi-service Docker Compose setup for DevSecOps environment.

## Services

| Service | Image | Port | Description |
|---------|-------|------|-------------|
| Jenkins | jenkins/jenkins:lts | 8080 | CI/CD server |
| OWASP ZAP | zaproxy/zaproxy:stable | 8090 | DAST security scanner |
| App | nginx:latest | 8085 | Test application |
| MySQL | mysql:8.0 | 3306 | Database |

## Tech stack

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white)
![OWASP ZAP](https://img.shields.io/badge/OWASP_ZAP-000000?style=flat&logo=owasp&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)

## How to run

```bash
# Copy env file
cp .env.example .env

# Edit .env with your values
# Start all services
docker-compose up -d

# Check status
docker-compose ps

# Stop all services
docker-compose down
```

## Related repos

- [jenkins-devsecops-pipeline](https://github.com/Walle-1904/jenkins-devsecops-pipeline) — Pipeline that runs on this infrastructure
- [cypress-e2e-suite](https://github.com/Walle-1904/cypress-e2e-suite) — Tests executed in the pipeline
