# ☸️ CKA – Certified Kubernetes Administrator

> The standard certification for Kubernetes administrators. Hands-on exam testing cluster management skills.

[← Back to Kubernetes certifications](./README.md)

---

## 📋 Exam Overview

| | |
|---|---|
| **Level** | Professional |
| **Duration** | 2 hours |
| **Questions** | 15-20 performance-based tasks |
| **Passing Score** | 66% |
| **Cost** | $395 USD (includes 2 free killer.sh sessions) |
| **Format** | Hands-on terminal – real Kubernetes clusters |
| **Retake** | 1 free retake included |

---

## 📖 Official Resources

- 📖 [Exam Page](https://www.cncf.io/training/certification/cka/) – Official exam info
- 📝 [Exam Curriculum](https://github.com/cncf/curriculum/blob/master/CKA_Curriculum_v1.30.pdf) – Official topics
- 📚 [Kubernetes Documentation](https://kubernetes.io/docs/) – **Allowed during exam**
- 📚 [Candidate Handbook](https://docs.linuxfoundation.org/tc-docs/certification/lf-handbook2) – Exam rules

---

## 📥 Practice Resources

- 🎮 [**killer.sh**](https://killer.sh/) – 2 free sessions with exam purchase – **Essential!**
- 🔬 [Killercoda CKA Scenarios](https://killercoda.com/killer-shell-cka) – Free practice
- 🔬 [KodeKloud CKA Labs](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/) – Free practice labs

---

## 🎬 Video Courses

- 🎬 [TechWorld with Nana – K8s Full Course](https://www.youtube.com/watch?v=X48VuDVv0do) – Excellent foundation
- 🎬 [freeCodeCamp – K8s Course](https://www.youtube.com/watch?v=d6WC5n9G_sM) – Complete free course
- 🎬 [KodeKloud CKA Course](https://kodekloud.com/) – Popular paid option with labs

---

## 📚 Exam Topics (Curriculum Domains)

### Cluster Architecture, Installation & Configuration (25%)
- Manage role-based access control (RBAC)
- Use Kubeadm to install a cluster
- Manage a highly-available Kubernetes cluster
- Provision underlying infrastructure for cluster deployment
- Perform a version upgrade on a Kubernetes cluster using Kubeadm
- Implement etcd backup and restore

### Workloads & Scheduling (15%)
- Understand deployments and rolling updates/rollbacks
- Use ConfigMaps and Secrets to configure applications
- Know how to scale applications
- Understand resource limits and Pod scheduling
- Understand manifest management and templating tools

### Services & Networking (20%)
- Understand host networking configuration on cluster nodes
- Understand ClusterIP, NodePort, LoadBalancer service types
- Know how to use Ingress controllers and Ingress resources
- Know how to configure and use CoreDNS
- Choose an appropriate container network interface (CNI) plugin

### Storage (10%)
- Understand storage classes and persistent volumes
- Understand volume modes, access modes, and reclaim policies
- Understand persistent volume claims
- Know how to configure applications with persistent storage

### Troubleshooting (30%)
- Evaluate cluster and node logging
- Understand how to monitor applications
- Manage container stdout & stderr logs
- Troubleshoot application failure
- Troubleshoot cluster component failure
- Troubleshoot networking

---

## 🔬 Hands-on Practice

- 🔬 [**Killercoda**](https://killercoda.com/) – Free browser-based practice
- 🔬 [Play with Kubernetes](https://labs.play-with-k8s.com/) – Free 4-hour playground
- 🔬 [Minikube](https://minikube.sigs.k8s.io/) – Local cluster
- 🔬 [kind](https://kind.sigs.k8s.io/) – Local clusters in Docker

---

## ⌨️ Essential Commands to Master

```bash
# Aliases (set in .bashrc)
alias k=kubectl
alias kn='kubectl config set-context --current --namespace'
export do="--dry-run=client -o yaml"

# Cluster management
kubeadm init / join
kubectl get nodes
kubectl drain <node> --ignore-daemonsets
kubectl cordon/uncordon <node>

# ETCD backup/restore
ETCDCTL_API=3 etcdctl snapshot save <file> \
  --endpoints=https://127.0.0.1:2379 \
  --cacert=/etc/kubernetes/pki/etcd/ca.crt \
  --cert=/etc/kubernetes/pki/etcd/server.crt \
  --key=/etc/kubernetes/pki/etcd/server.key

# Quick YAML generation
kubectl run nginx --image=nginx $do > pod.yaml
kubectl create deployment nginx --image=nginx $do > deploy.yaml
kubectl expose deployment nginx --port=80 --type=NodePort $do > svc.yaml

# Troubleshooting
kubectl describe pod <pod>
kubectl logs <pod> -c <container>
kubectl exec -it <pod> -- /bin/sh
kubectl get events --sort-by=.metadata.creationTimestamp
```

---

## 💬 Communities

- 💬 [r/kubernetes](https://www.reddit.com/r/kubernetes/) – Active community
- 💬 [Kubernetes Slack](https://slack.k8s.io/) – #cka-prep channel

---

## 💡 Study Tips

1. **Practice, practice, practice** – This is a hands-on exam, not theory
2. **Master kubectl** – Speed matters, use aliases and shortcuts
3. **Learn to navigate the docs** – kubernetes.io/docs is allowed during exam
4. **Do killer.sh sessions** – Closest to real exam difficulty
5. **Practice under time pressure** – 2 hours goes very fast
6. **Know vim/nano basics** – You'll edit YAML files constantly
7. **Understand etcd backup/restore** – Commonly tested
8. **6-10 weeks of study** recommended with daily hands-on practice

---

## ✅ Exam Readiness Checklist

- [ ] Completed a structured CKA course
- [ ] Can deploy a cluster with kubeadm from memory
- [ ] Comfortable with RBAC (Roles, RoleBindings, ClusterRoles)
- [ ] Know how to backup and restore etcd
- [ ] Can create deployments, services, ingress from scratch
- [ ] Understand PV, PVC, StorageClass configuration
- [ ] Can troubleshoot pod failures, network issues, node problems
- [ ] Completed both killer.sh sessions (score 80%+)
- [ ] Practiced with Killercoda scenarios

---

## 🚨 Exam Day Tips

- Use the notepad provided in the exam environment
- Skip hard questions and come back
- Use `kubectl explain` for quick field references
- Copy/paste from docs when possible
- Set namespace context per question: `kubectl config set-context --current --namespace=<ns>`
- Don't overthink – most tasks are straightforward

---

[← Back to Kubernetes certifications](./README.md)
