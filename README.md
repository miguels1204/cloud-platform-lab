# cloud-platform-lab

A small platform built from scratch, in public, to practise and demonstrate production-style infrastructure: infrastructure as code, Kubernetes, GitOps, observability and SLOs.

> **Status: planning.** The roadmap below is the plan; boxes get ticked as pieces land.
> Everything here is built on my personal accounts. No employer code, names or data.

## Goals

- Reproducible infrastructure: one command to create it, one to destroy it.
- Changes only through pull requests, with a plan and checks before apply.
- Observable by default: metrics, dashboards and alerts tied to SLOs.
- Every decision written down, so the repo explains itself.

## Planned layout

```
terraform/      reusable modules and environments
gitops/         ArgoCD applications and cluster config
observability/  Prometheus rules, Grafana dashboards, SLO definitions
scripts/        Python tooling, with tests
docs/           architecture diagram, decision records, runbooks, postmortems
.github/        CI/CD workflows
```

## Roadmap

**Foundations**
- [ ] Repo skeleton, README and architecture diagram
- [ ] Terraform modules with remote state
- [ ] Local cluster with kind for cheap development

**Platform**
- [ ] Kubernetes cluster on AWS (EKS) with autoscaling
- [ ] GitOps with ArgoCD
- [ ] CI/CD: plan on pull request, apply on merge

**Observability and reliability**
- [ ] Prometheus and Grafana dashboards
- [ ] OpenTelemetry tracing
- [ ] SLOs and alerts based on burn rate
- [ ] Game day and a written postmortem

**Extras**
- [ ] Ansible for node configuration
- [ ] Python tools for AWS automation, with pytest

## Cost and safety

- Local clusters by default. AWS pieces are optional and destroyed after each session.
- Budget alerts enabled on the AWS account.
- Secret scanning enabled on the repository.

## Decisions

Architecture decision records will live in `docs/decisions/`.

## License

MIT