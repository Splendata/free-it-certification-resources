# ☸️ Kubernetes (CNCF) Certifications

> Free resources for Kubernetes certification preparation from the Cloud Native Computing Foundation.

[← Back to all providers](../README.md)

---

## 🌐 General Kubernetes Resources

### Official Resources
- 📖 [CNCF Certifications](https://www.cncf.io/training/certification/) – Official exam info
- 📚 [Kubernetes Documentation](https://kubernetes.io/docs/) – **Essential** for the exam
- 📝 [Exam Curriculum (GitHub)](https://github.com/cncf/curriculum) – Official exam topics
- 🔬 [Kubernetes Tutorials](https://kubernetes.io/docs/tutorials/) – Official hands-on guides

### Learning Platforms
- 🎬 [TechWorld with Nana](https://www.youtube.com/c/TechWorldwithNana) – Excellent K8s tutorials
- 🎬 [KodeKloud](https://kodekloud.com/) – Popular K8s training (free intro courses)
- 🎬 [freeCodeCamp K8s Course](https://www.youtube.com/watch?v=d6WC5n9G_sM) – Full free course
- 📚 [Kubernetes The Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way) – Deep learning

### Communities
- 💬 [r/kubernetes](https://www.reddit.com/r/kubernetes/) – Active Reddit community
- 💬 [Kubernetes Slack](https://slack.k8s.io/) – Official community Slack
- 💬 [CNCF Slack](https://slack.cncf.io/) – Cloud native community

---

## 📜 Certifications

| Certification | Level | Resources |
|--------------|-------|-----------|
| **CKA – Certified Kubernetes Administrator** | Professional | [View Resources →](./cka.md) |
| **CKAD – Certified Kubernetes Application Developer** | Professional | [View Resources →](./ckad.md) |
| **CKS – Certified Kubernetes Security Specialist** | Advanced | [View Resources →](./cks.md) |
| **KCNA – Kubernetes and Cloud Native Associate** | Foundational | [View Resources →](./kcna.md) |
| **KCSA – Kubernetes and Cloud Native Security Associate** | Foundational | [View Resources →](./kcsa.md) |

---

## 🗺️ Recommended Learning Path

```
KCNA (Foundational - Optional)
         ↓
    CKA or CKAD
    (depends on role)
         ↓
    ┌────┴────┐
    ↓         ↓
  CKAD       CKA
(if dev)  (if ops)
    ↓         ↓
    └────┬────┘
         ↓
        CKS
  (Security - Advanced)
```

**Which to take first?**
- **Administrators/DevOps**: CKA → CKAD → CKS
- **Developers**: CKAD → CKA → CKS

---

## 💡 Kubernetes Certification Tips

- **These are hands-on exams** – You work in a real terminal, not multiple choice
- **kubectl speed is critical** – Practice until commands are muscle memory
- **Documentation is allowed** – Learn to navigate kubernetes.io/docs quickly
- **Use aliases and shortcuts** – Set up kubectl aliases to save time
- **Time management is key** – 2 hours goes fast, don't get stuck on one question
- **killer.sh is essential** – 2 free sessions included with exam purchase

---

## 🔬 Free Practice Environments

- 🔬 [**Killercoda**](https://killercoda.com/) – Free browser-based K8s environments
- 🔬 [Play with Kubernetes](https://labs.play-with-k8s.com/) – Free 4-hour playground
- 🔬 [Minikube](https://minikube.sigs.k8s.io/) – Local K8s cluster
- 🔬 [kind (Kubernetes in Docker)](https://kind.sigs.k8s.io/) – Local clusters using Docker
- 🔬 [k3s](https://k3s.io/) – Lightweight K8s for practice

---

## ⌨️ Essential kubectl Commands

```bash
# Set alias (add to .bashrc)
alias k=kubectl

# Quick tips
kubectl explain pod.spec.containers  # Built-in docs
kubectl run nginx --image=nginx --dry-run=client -o yaml > pod.yaml  # Generate YAML
kubectl get pods -o wide  # More info
kubectl describe pod <name>  # Detailed info
kubectl logs <pod> -f  # Follow logs
kubectl exec -it <pod> -- /bin/sh  # Shell into pod
```

---

[← Back to all providers](../README.md)
