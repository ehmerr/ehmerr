<h1 align="center">Hi, I'm Ahmar Rahmani</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1200&center=true&vCenter=true&width=640&lines=DevOps+Intern+%40+BytePe;Kubernetes+on+GKE+%C2%B7+Helm+%C2%B7+Terraform;GitLab+CI%2FCD+%C2%B7+Grafana+%C2%B7+Loki;Self-hosting+LLMs+on+GPUs" alt="DevOps Intern at BytePe. Kubernetes on GKE, Helm, Terraform. GitLab CI/CD, Grafana, Loki. Self-hosting LLMs on GPUs." />
</p>

<p align="center">
  <a href="https://linkedin.com/in/ahmarrahmani"><img src="https://img.shields.io/badge/LinkedIn-ahmarrahmani-0A66C2?style=for-the-badge" alt="LinkedIn" /></a>
  <a href="mailto:ahmarrahmanicse@gmail.com"><img src="https://img.shields.io/badge/Email-Get%20in%20touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://img.shields.io/badge/Open%20to-DevOps%20%C2%B7%20Cloud%20%C2%B7%20SRE-2EA44F?style=for-the-badge" alt="Open to DevOps, Cloud and SRE roles" />
</p>

---

I'm a DevOps Intern at **BytePe**, a fintech startup, where I run services on **Google Cloud with Kubernetes**. I like infrastructure that's boring in production: reproducible with Terraform, shipped through pipelines, and visible in dashboards.

## What I work on at BytePe

| | |
| --- | --- |
| **VM → Kubernetes** | Migrated a 10-service backend from VMs to **GKE Autopilot** with my lead, all on one shared **Helm** chart |
| **Pipelines** | **GitLab CI/CD** to dev and a new staging environment, with migration Jobs, immutable image tags and automatic rollback |
| **Infrastructure as code** | **Terraform** for GKE Gateway, Cloud Armor, Workload Identity and IAM |
| **Cost** | About **64% fewer** non-production compute hours by scaling to zero outside working hours |
| **Reliability** | Tuned HPA autoscaling and health probes; **k6** load tests for the platform and its Cloud Armor rules |
| **AI infrastructure** | Self-hosted **NVIDIA Nemotron on vLLM** on a GKE GPU node, with a RAG proof of concept |

A simplified view of how a change ships:

```mermaid
flowchart LR
    push["git push"] --> ci["GitLab CI/CD"]
    ci -->|"build and push image"| ar[("Artifact Registry")]
    ci -->|"helm upgrade"| gke["GKE Autopilot<br/>10 services, one Helm chart"]
    ar --> gke
    users["Users"] --> gw["GKE Gateway<br/>+ Cloud Armor"] --> gke
    tf["Terraform"] -.->|"provisions"| gw
    tf -.->|"provisions"| gke
```

BytePe's code lives in private company repositories. Everything below is my own.

## Featured project

### [docker-logging-stack](https://github.com/ehmerr/docker-logging-stack)

Collects logs from every Docker container into one place. **Grafana Alloy** discovers containers through the Docker socket, labels each stream by container name and ships it to **Loki**; **Grafana** searches it all with LogQL.

`Docker Compose` `Grafana` `Loki` `Grafana Alloy` `LogQL`

## Right now

- Setting up monitoring for our GKE platform with **Google Cloud Managed Service for Prometheus** and **Grafana**
- Preparing for **AWS Certified Cloud Practitioner** (December 2026)
- Learning **Argo CD** and GitOps

## Tech stack

**Cloud: Google Cloud**

![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Compute Engine VMs](https://img.shields.io/badge/Compute%20Engine%20VMs-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Managed Instance Groups](https://img.shields.io/badge/Managed%20Instance%20Groups-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![GKE](https://img.shields.io/badge/GKE%20Autopilot-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Cloud SQL](https://img.shields.io/badge/Cloud%20SQL-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Memorystore Redis](https://img.shields.io/badge/Memorystore%20Redis-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Cloud Storage](https://img.shields.io/badge/Cloud%20Storage-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Artifact Registry](https://img.shields.io/badge/Artifact%20Registry-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Cloud Load Balancing](https://img.shields.io/badge/Cloud%20Load%20Balancing-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Cloud Armor](https://img.shields.io/badge/Cloud%20Armor-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![IAM and Workload Identity](https://img.shields.io/badge/IAM%20%26%20Workload%20Identity-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Secret Manager](https://img.shields.io/badge/Secret%20Manager-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

**Containers & orchestration**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)

**Infrastructure as code**

![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)

**CI/CD & version control**

![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**Observability**

![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F46800?style=flat-square)
![Grafana Alloy](https://img.shields.io/badge/Grafana%20Alloy-F46800?style=flat-square)

**Linux & networking**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![SSH](https://img.shields.io/badge/SSH-333333?style=flat-square)
![Networking](https://img.shields.io/badge/TCP%2FIP%20%C2%B7%20DNS%20%C2%B7%20TLS%20%C2%B7%20VPC-555555?style=flat-square)

**Databases**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)

**Testing & load testing**

![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)

**AI infrastructure**

![NVIDIA](https://img.shields.io/badge/NVIDIA%20GPUs-76B900?style=flat-square&logo=nvidia&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-30A2FF?style=flat-square)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Open WebUI](https://img.shields.io/badge/Open%20WebUI-111111?style=flat-square)

**Learning**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Argo CD](https://img.shields.io/badge/Argo%20CD-EF7B4D?style=flat-square&logo=argo&logoColor=white)

## Other projects

- [Strandly](https://github.com/ehmerr/Strandly-Your-Friendly-Hair-Fall-Tracker): a full-stack MERN app for tracking hair fall and visualising trends
- [Cure Connect](https://github.com/ehmerr/DoctorAppointmentBookingSystem): doctor appointment booking, [live demo](https://cure-connect-nine.vercel.app)
- [MovieRecSystem](https://github.com/ehmerr/MovieRecSystem): content-based movie recommendations with cosine similarity
- [DSA_QUESTIONS](https://github.com/ehmerr/DSA_QUESTIONS): LeetCode and GFG problems I've solved in C++

<p align="center"><i>Learning in public, one cluster at a time.</i></p>
