## Hi there 👋

# I'm Sonal Kumar

**DevOps Engineer** | Building reliable, scalable infrastructure with Terraform, Kubernetes, and AWS

I work on infrastructure reliability — designing systems that are resilient, observable, and self-healing. I specialize in Infrastructure as Code, Kubernetes platform engineering, and CI/CD pipeline design.

---

## Case Studies: Real Infrastructure Challenges I've Solved

### [The Silent Infrastructure Drift That Terraform Couldn't See](https://your-hashnode-url-here)

A deep investigation into how three independent bugs — a Kubernetes immutable CRD field, a 6-year-old Terraform Plugin SDK default behavior, and an unmaintained community provider — combined to create invisible state drift that masked a production-impacting failure.

**What I did:**
- Diagnosed a cross-stack dependency failure where an NLB Target Group ARN changed but the Kubernetes TargetGroupBinding wasn't updated
- Traced the root cause through Kubernetes admission webhooks, Terraform state files, and the Plugin SDK source code
- Discovered that the `gavinbunney/kubectl` provider silently corrupts Terraform state when Kubernetes rejects an update (documented in [terraform-plugin-sdk#476](https://github.com/hashicorp/terraform-plugin-sdk/issues/476))
- Designed a permanent fix using `terraform_data` + `lifecycle { replace_triggered_by }` to force DELETE + CREATE on immutable field changes
- Implemented CI/CD pipeline ordering via Spacelift trigger policies to prevent cross-stack timing issues

**Tech:** Terraform, Kubernetes, AWS (EKS, NLB, SSM, PrivateLink), Helm, Spacelift, AWS Load Balancer Controller

---

## What I Work With

**Infrastructure as Code:** Terraform, Spacelift, CloudFormation

**Container Orchestration:** Kubernetes (EKS), Helm, Kustomize

**Cloud Platforms:** AWS (EKS, NLB/ALB, SSM, PrivateLink, IAM, EC2, S3)

**CI/CD:** GitLab CI, Spacelift, GitHub Actions

**Monitoring & Observability:** Datadog, CloudWatch, Prometheus

**Service Mesh & Networking:** AWS Load Balancer Controller, TargetGroupBinding, gRPC, PrivateLink

---

## Recent Technical Writing

| Article | Topics | Link |
|---------|--------|------|
| The Silent Infrastructure Drift That Terraform Couldn't See | Terraform, Kubernetes, State Drift, CRDs | [Read on Hashnode](https://hashnode.com/edit/cmr0f0o78000109jh4j78e672) |

---

## Connect

- [Hashnode Blog](https://devopswork.hashnode.dev/)
- [LinkedIn](https://www.linkedin.com/in/sonal-a-kumar/)

