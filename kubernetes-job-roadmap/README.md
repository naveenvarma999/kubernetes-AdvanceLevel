# Kubernetes Job-Level Roadmap

A hands-on 6–8 month roadmap for learning Kubernetes from fundamentals to production-level skills.

## Career Targets

This repository is designed for preparation toward roles such as:

- Junior DevOps Engineer
- Junior Cloud Engineer
- Kubernetes Support Engineer
- Junior Platform Engineer
- Junior Site Reliability Engineer
- MLOps Engineer Intern / Junior MLOps Engineer
- Cloud Operations Engineer

## Study Method

Recommended daily study time: **2–3 hours**

- 30% theory
- 70% hands-on practice
- One troubleshooting session every week
- One project milestone every month

## Roadmap Progress

| Month | Focus | Status |
|---|---|---|
| 1 | Linux, networking, Git, YAML and Docker | Not started |
| 2 | Kubernetes fundamentals | Not started |
| 3 | Networking, storage and scheduling | Not started |
| 4 | Cluster administration and troubleshooting | Not started |
| 5 | Helm, Kustomize, CI/CD and GitOps | Not started |
| 6 | Monitoring, logging and security | Not started |
| 7 | Cloud Kubernetes, Terraform and production deployment | Not started |
| 8 | Advanced Kubernetes, MLOps, interview preparation | Not started |

## Repository Structure

```text
kubernetes-job-roadmap/
├── month-01-foundations/
├── month-02-kubernetes-core/
├── month-03-networking-storage/
├── month-04-cluster-administration/
├── month-05-cicd-gitops/
├── month-06-observability-security/
├── month-07-cloud-terraform/
├── month-08-advanced-mlops/
├── projects/
├── manifests/
├── helm-charts/
├── terraform/
├── scripts/
├── docs/
└── README.md
```

## Major Projects

1. Containerised FastAPI application
2. Kubernetes application deployment
3. Multi-node kubeadm cluster
4. CI/CD and Argo CD GitOps platform
5. Cloud Kubernetes deployment using Terraform
6. MLOps model-serving platform

## Rules for This Repository

- Every topic must include notes and a practical lab.
- Every lab must include commands and expected output.
- Do not store passwords, tokens, kubeconfig files or cloud credentials.
- Use versioned Docker image tags instead of `latest`.
- Document errors and their solutions.
- Commit progress regularly.
- Write a clear README for every major project.

## Useful Commands

```bash
git status
git add .
git commit -m "Complete Kubernetes service lab"
git push
```

## Completion Standard

You should be able to:

- Containerise an application
- Deploy it to Kubernetes
- Configure networking and persistent storage
- Package it with Helm
- Build a CI/CD pipeline
- Deploy through Argo CD
- Monitor it using Prometheus and Grafana
- Secure it using RBAC and NetworkPolicy
- Provision cloud infrastructure using Terraform
- Troubleshoot application and cluster failures
