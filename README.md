<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1a1f35,100:0ea5e9&height=190&section=header&text=Fady%20Mounir%20Zaghloul&fontSize=40&fontColor=e2e8f0&fontAlignY=38&desc=IT%20and%20Security%20%7C%20Platform%20and%20Infrastructure%20Engineering%20%7C%20DevSecOps&descSize=14&descAlignY=59&descColor=94a3b8" alt="Fady Mounir Zaghloul" />

<img src="./assets/infra-flow.svg" width="900" alt="Animated engineering delivery flow from source control to platform operations" />

<img src="./assets/coding.gif" width="480" alt="Coding animation" />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=15&pause=1000&color=0EA5E9&center=true&vCenter=true&width=780&lines=Design+for+rollback%2C+not+only+deployment;Short-lived+OIDC+credentials+over+stored+cloud+keys;Signed+artifacts+%2B+policy+before+runtime;SLOs+and+runbooks+before+dashboard+decoration;Public+evidence%2C+private+operational+detail)](https://git.io/typing-svg)

[![Portfolio](https://img.shields.io/badge/Portfolio-0ea5e9?style=for-the-badge&logo=githubpages&logoColor=white)](https://fadyy2k.github.io/portfolio/)
[![Engineering Case Studies](https://img.shields.io/badge/Case_Studies-Architecture_%7C_Reliability-34d399?style=for-the-badge&logo=readthedocs&logoColor=111827)](https://github.com/fadyy2k/engineering-case-studies)
[![Selected Engineering Delivery](https://img.shields.io/badge/Delivery_Board-Selected_Engineering_Work-2563eb?style=for-the-badge&logo=github&logoColor=white)](https://github.com/users/fadyy2k/projects/1)
[![Engineering Lab Roadmap](https://img.shields.io/badge/Lab_Roadmap-Platform_%7C_DevSecOps-a78bfa?style=for-the-badge&logo=github&logoColor=white)](https://github.com/users/fadyy2k/projects/2)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/fady-mounir-601331b6/)
[![Credly](https://img.shields.io/badge/Credly-FF6B35?style=for-the-badge&logo=credly&logoColor=white)](https://www.credly.com/users/fady-mounir-zaghloul)

</div>

---

## `whoami`

```yaml
name: Fady Mounir Zaghloul
current_role: IT & Security Manager @ AsusCard FinTech
location: Cairo, Egypt
experience: 12+ years across infrastructure, cloud, operations and security

engineering_focus:
  - platform and infrastructure engineering
  - cloud architecture and migration
  - DevSecOps and software supply-chain security
  - observability, SLOs and operational reliability
  - identity, endpoint and infrastructure security

open_to:
  - Infrastructure / Platform Lead
  - Cloud / Platform Engineer
  - DevOps / SRE
  - Security Architecture / Operations
```

## 🧭 Engineering principles

- **Rollback is a feature.** A deployment path is incomplete until the known-good recovery path is documented and tested.
- **Identity before static credentials.** Prefer short-lived OIDC/workload identity and least privilege over stored cloud keys.
- **Security belongs in delivery.** Scan source/configuration, generate provenance/SBOM, sign artifacts, then enforce policy at admission/runtime.
- **Operate from signals.** SLOs, error budgets, runbooks and recovery tests matter more than decorative dashboards.
- **Public evidence ≠ public infrastructure.** Production write-ups are sanitized; credentials, live endpoints, private network plans and customer data stay private.

---

## 🚀 Current flagship — AWS EKS Platform Engineering

<a href="https://github.com/fadyy2k/platform-engineering-eks-gitops">
  <img src="https://img.shields.io/badge/Platform_Engineering-EKS_%7C_Terraform_%7C_Argo_CD-844FBA?style=for-the-badge&logo=terraform&logoColor=white" alt="AWS EKS Platform Engineering" />
</a>

A production-style public reference implementation that now covers:

`Terraform` · `AWS EKS` · `GitHub OIDC` · `Argo CD` · `Cosign` · `Kyverno` · `Falco` · `Trivy Operator` · `Prometheus/Grafana` · `SLOs` · `OpenCost` · `VPA recommendations` · `backup/game-day patterns` · `DR architecture`

- Seven staged engineering releases from baseline through live-readiness and local runtime evidence
- protected `main`, required security checks and signed commits
- project-owned container supply chain with provenance, SBOM, scanning and keyless signing
- policy/runtime security, reliability and cost controls separated into reviewable layers
- real Kubernetes 1.36 local runtime evidence: Argo CD, Kyverno admission, Prometheus/SLOs, Trivy, Falco, VPA, OpenCost and a controlled recovery game day
- live-cloud activation deliberately kept explicit rather than pretending unprovisioned infrastructure is running

**→ [Documentation](https://fadyy2k.github.io/platform-engineering-eks-gitops/) · [Local Runtime Evidence](https://fadyy2k.github.io/platform-engineering-eks-gitops/LOCAL_RUNTIME/) · [Repository](https://github.com/fadyy2k/platform-engineering-eks-gitops) · [v0.7.0](https://github.com/fadyy2k/platform-engineering-eks-gitops/releases/tag/v0.7.0)**

---

## 🏗️ Sanitized production engineering

Long-form production details no longer live in this profile. They are separated into sanitized case studies so the engineering decisions are public without publishing a real environment's attack surface.

| Pattern | Focus |
| --- | --- |
| [Multi-tenant SaaS platform](https://github.com/fadyy2k/engineering-case-studies/blob/main/case-studies/01-multi-tenant-saas-platform.md) | isolation, releases, backups, observability, capacity |
| [Cross-site PostgreSQL replication](https://github.com/fadyy2k/engineering-case-studies/blob/main/case-studies/02-cross-site-postgresql-replication.md) | private connectivity, replication health, rollback |
| [Cloud migration with rollback](https://github.com/fadyy2k/engineering-case-studies/blob/main/case-studies/03-cloud-migration-with-rollback.md) | replication-first cutover, DNS, failback |
| [Observability baseline](https://github.com/fadyy2k/engineering-case-studies/blob/main/case-studies/04-observability-baseline.md) | signals, alerts, runbooks |
| [Identity hardening](https://github.com/fadyy2k/engineering-case-studies/blob/main/case-studies/05-identity-security-hardening.md) | MFA, mail security, DLP, rollout safety |
| [Local-first internal AI](https://github.com/fadyy2k/engineering-case-studies/blob/main/case-studies/06-local-first-ai-platform.md) | data boundaries, RBAC, RAG, plugin/network risk |

**→ [Engineering Case Studies](https://github.com/fadyy2k/engineering-case-studies)**

---

## 🧰 Engineering stack

<details>
<summary><b>Cloud, platform, automation and security</b></summary>

### Cloud / Infrastructure
`AWS` · `OCI` · `Linux` · `Terraform` · `Kubernetes / EKS / K3s` · `Argo CD` · `Nginx` · `Proxmox` · `VMware`

### Delivery / Automation
`GitHub Actions` · `Jenkins` · `Docker / BuildKit` · `Ansible` · `Bash` · `Python` · `PM2`

### Security
`Microsoft Defender` · `FortiGate` · `CodeQL` · `Gitleaks` · `Trivy` · `Cosign` · `Kyverno` · `Falco` · `Tailscale`

### Observability / Reliability
`Prometheus` · `Grafana` · `SLO / error-budget alerts` · `OpenCost` · `game-day / recovery testing`

### Data / Application
`PostgreSQL` · `MySQL / MariaDB` · `SQL Server` · `Redis` · `Node.js` · `NestJS` · `FastAPI` · `.NET`

</details>

---

## 🏅 Credentials

<details>
<summary><b>Selected certifications and training</b></summary>

| Vendor | Selected credentials |
| --- | --- |
| Microsoft | **SC-100** Cybersecurity Architect Expert · **SC-200** Security Operations Analyst |
| AWS | **SAA-C03** Solutions Architect Associate · **CLF-C02** Cloud Practitioner |
| Cisco | **CCNA** · **CyberOps Associate** |
| IBM | Cloud Professional Architect · Cloud SRE · SkillsBuild Cybersecurity |
| Google | IT Support Professional · Security in Google Cloud |
| NTI / MCIT | DEPI Cisco Cybersecurity Engineer · Post Graduate Diploma AI & Modern Technologies |

**30+ verifiable credentials → [Credly](https://www.credly.com/users/fady-mounir-zaghloul)**

</details>

---

## 🔬 Featured engineering repositories

<div align="center">

<a href="https://github.com/fadyy2k/platform-engineering-eks-gitops"><img src="https://img.shields.io/badge/01_Platform_Engineering-EKS_%7C_GitOps_%7C_SRE-844FBA?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Platform engineering" /></a>
<a href="https://github.com/fadyy2k/depi-mind-app-v2"><img src="https://img.shields.io/badge/02_MIND_DevSecOps-Jenkins_%7C_Argo_CD-326CE5?style=for-the-badge&logo=jenkins&logoColor=white" alt="MIND DevSecOps" /></a>
<a href="https://github.com/fadyy2k/depi-helloapp-infra-v2"><img src="https://img.shields.io/badge/03_AWS_EKS_IaC-Terraform_%7C_IAM-844FBA?style=for-the-badge&logo=terraform&logoColor=white" alt="AWS EKS infrastructure" /></a>

<a href="https://github.com/fadyy2k/notesapp-multi-ec2-ansible"><img src="https://img.shields.io/badge/04_Ansible_Automation-AWS_%7C_Nginx-EE0000?style=for-the-badge&logo=ansible&logoColor=white" alt="Ansible automation" /></a>
<a href="https://github.com/fadyy2k/depi-devsecops-showcase"><img src="https://img.shields.io/badge/05_Architecture_Showcase-React_%7C_Vite-61DAFB?style=for-the-badge&logo=react&logoColor=111827" alt="Architecture showcase" /></a>
<a href="https://github.com/fadyy2k/engineering-case-studies"><img src="https://img.shields.io/badge/06_Case_Studies-Architecture_%7C_Operations-34d399?style=for-the-badge&logo=readthedocs&logoColor=111827" alt="Engineering case studies" /></a>

</div>

---

## 📊 GitHub activity

<div align="center">

<img src="https://img.shields.io/github/followers/fadyy2k?style=for-the-badge&logo=github&label=Followers" alt="GitHub followers" />
<img src="https://img.shields.io/github/last-commit/fadyy2k/platform-engineering-eks-gitops?style=for-the-badge&logo=github&label=Platform%20last%20commit" alt="Platform last commit" />
<img src="https://img.shields.io/github/v/release/fadyy2k/platform-engineering-eks-gitops?style=for-the-badge&logo=github&label=Platform%20release" alt="Platform release" />

<br/><br/>

<img src="https://streak-stats.demolab.com?user=fadyy2k&theme=github-dark-blue&hide_border=true&background=0d1117&ring=0ea5e9&fire=34d399&currStreakLabel=94a3b8&sideLabels=94a3b8&dates=475569" alt="GitHub contribution streak" />

</div>

---

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0ea5e9,50:1a1f35,100:0d1117&height=100&section=footer" alt="footer" />

*Build for the failure path. Document the recovery path.*
</div>
