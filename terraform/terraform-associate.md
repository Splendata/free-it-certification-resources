# 🏗️ Terraform Associate (003)

> The foundational Infrastructure as Code certification. Covers Terraform concepts, workflow, and best practices.

[← Back to Terraform certifications](./README.md)

---

## 📋 Exam Overview

| | |
|---|---|
| **Level** | Associate |
| **Duration** | 60 minutes |
| **Questions** | 57 questions |
| **Passing Score** | ~70% |
| **Cost** | $70.50 USD |
| **Format** | Multiple choice, multiple select, fill-in-the-blank |
| **Validity** | 2 years |

---

## 📖 Official Resources

- 📖 [Exam Page](https://www.hashicorp.com/certifications/terraform-associate) – Official exam info
- 📝 [**Exam Review Guide**](https://developer.hashicorp.com/terraform/tutorials/certification-003/associate-review-003) – **Essential** – Study this!
- 🎓 [Study Guide Tutorial](https://developer.hashicorp.com/terraform/tutorials/certification-003/associate-study-003) – Official prep
- 📝 [Sample Questions](https://developer.hashicorp.com/terraform/tutorials/certification-003/associate-questions) – From HashiCorp

---

## 📥 Free Practice Exams

- 🆓 [HashiCorp Sample Questions](https://developer.hashicorp.com/terraform/tutorials/certification-003/associate-questions) – Official samples
- 📚 [CertifHub Terraform Practice](https://certifhub.com) – Additional practice questions

---

## 🎬 Video Courses

- 🎬 [freeCodeCamp – Terraform Course (2.5 hrs)](https://www.youtube.com/watch?v=SLB_c_ayRMo) – Complete free course
- 🎬 [HashiCorp Learn Videos](https://developer.hashicorp.com/terraform/tutorials) – Official tutorials with video
- 🎬 [TechWorld with Nana – Terraform](https://www.youtube.com/watch?v=l5k1ai_GBDE) – Excellent overview

---

## 📚 Exam Topics

### 1. Understand Infrastructure as Code (IaC) Concepts
- Explain what IaC is
- Describe advantages of IaC patterns

### 2. Understand the Purpose of Terraform (vs Other IaC)
- Explain multi-cloud and provider-agnostic benefits
- Explain the benefits of state

### 3. Understand Terraform Basics
- Install and version Terraform providers
- Describe plugin-based architecture
- Write Terraform configuration using multiple providers
- Describe how Terraform finds and fetches providers

### 4. Use Terraform Outside of Core Workflow
- Describe when to use `terraform import`
- Use `terraform state` to modify state
- Describe when to enable verbose logging

### 5. Interact with Terraform Modules
- Contrast and use different module sources
- Interact with module inputs and outputs
- Describe variable scope within modules
- Set module version

### 6. Use the Core Terraform Workflow
- Describe Terraform workflow (Write → Plan → Apply)
- Initialize a Terraform working directory (`terraform init`)
- Validate a Terraform configuration (`terraform validate`)
- Generate and review an execution plan (`terraform plan`)
- Execute changes (`terraform apply`)
- Destroy Terraform-managed infrastructure (`terraform destroy`)

### 7. Implement and Maintain State
- Describe default local backend
- Describe state locking
- Handle backend and cloud integration authentication methods
- Differentiate remote state backend options
- Manage resource drift and Terraform state
- Describe `backend` block and cloud integration in configuration
- Understand secret management in state files

### 8. Read, Generate, and Modify Configuration
- Demonstrate use of variables and outputs
- Describe secure secret injection best practices
- Understand the use of collection and structural types
- Create and differentiate resource and data configuration
- Use resource addressing and resource parameters
- Use Terraform built-in functions
- Configure resource using a `dynamic` block
- Describe built-in dependency management (order of operations)

### 9. Understand HCP Terraform Capabilities
- Explain how HCP Terraform helps manage infrastructure
- Describe how HCP Terraform enables collaboration and governance

---

## 🔬 Hands-on Practice

- 🔬 [HashiCorp Learn Tutorials](https://developer.hashicorp.com/terraform/tutorials) – Free official labs
- 🔬 [Terraform Registry](https://registry.terraform.io/) – Explore real modules
- 🔬 [AWS Free Tier](https://aws.amazon.com/free/) – Practice Terraform with real infrastructure
- 🔬 [Azure Free Account](https://azure.microsoft.com/free/) – Alternative cloud for practice
- 🔬 [GCP Free Tier](https://cloud.google.com/free) – Another option for practice

---

## 💬 Communities

- 💬 [r/Terraform](https://www.reddit.com/r/Terraform/) – Active community
- 💬 [HashiCorp Discuss](https://discuss.hashicorp.com/c/terraform-core/) – Official forum

---

## 📝 Key Concepts to Master

### Terraform Workflow
```bash
terraform init      # Initialize, download providers
terraform validate  # Check syntax
terraform plan      # Preview changes
terraform apply     # Apply changes
terraform destroy   # Remove infrastructure
```

### State Management
```bash
terraform state list              # List resources in state
terraform state show <resource>   # Show resource details
terraform state mv                # Move/rename resources
terraform state rm                # Remove from state
terraform import                  # Import existing infrastructure
```

### Variables
```hcl
# variables.tf
variable "instance_type" {
  description = "EC2 instance type"
  type        = string
  default     = "t2.micro"
}

# terraform.tfvars
instance_type = "t3.small"

# Command line
terraform apply -var="instance_type=t3.medium"
```

### Outputs
```hcl
output "instance_ip" {
  description = "Public IP of the instance"
  value       = aws_instance.example.public_ip
  sensitive   = false
}
```

### Data Sources
```hcl
data "aws_ami" "ubuntu" {
  most_recent = true
  owners      = ["099720109477"]
  
  filter {
    name   = "name"
    values = ["ubuntu/images/hvm-ssd/ubuntu-focal-20.04-amd64-server-*"]
  }
}
```

---

## 💡 Study Tips

1. **Complete HashiCorp Learn tutorials** – Best free resource available
2. **Practice writing HCL** – Don't just read, actually write configurations
3. **Understand state deeply** – Remote state, locking, sensitive data
4. **Know the workflow commands** – init, plan, apply, destroy and their flags
5. **Study modules** – Sources, inputs, outputs, versioning
6. **Review built-in functions** – lookup, join, file, templatefile, etc.
7. **Understand provisioners** – And why they should be a last resort
8. **2-4 weeks of study** recommended

---

## ✅ Exam Readiness Checklist

- [ ] Completed HashiCorp Learn Associate tutorials
- [ ] Written Terraform configs for at least 2 different providers
- [ ] Understand local vs remote state backends
- [ ] Know how to use variables, outputs, and data sources
- [ ] Comfortable with modules (using and creating)
- [ ] Understand state management commands
- [ ] Know terraform import workflow
- [ ] Familiar with HCP Terraform (formerly Terraform Cloud) concepts
- [ ] Taken practice questions and scoring 80%+

---

[← Back to Terraform certifications](./README.md)
