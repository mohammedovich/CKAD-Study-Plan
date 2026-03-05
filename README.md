# 🧑‍💻 CKAD Study Plan — Mohammed

> **Certified Kubernetes Application Developer**  
> 🎯 Target Exam: **Mid-May 2026** | ⏱️ Duration: **10 Weeks** | 📅 Start: Early March 2026

---

## 📋 Exam Overview

| Detail | Info |
|--------|------|
| ⏱️ Duration | 2 hours |
| 🎯 Passing Score | 66% |
| 💰 Cost | $395 USD (1 free retake included) |
| 📖 Format | Performance-based (hands-on kubectl tasks) |
| 🌐 Open Book | kubernetes.io docs allowed |
| ☸️ K8s Version | 1.30+ |

---

## 📊 Curriculum Breakdown

| Domain | Weight | Key Areas |
|--------|--------|-----------|
| Application Environment, Config & Security | 25% | ConfigMaps, Secrets, RBAC, SecurityContext |
| Application Design & Build | 20% | Containers, Jobs, multi-container pods, volumes |
| Application Deployment | 20% | Deployments, rolling updates, Helm basics |
| Services & Networking | 20% | Services, Ingress, NetworkPolicies |
| Application Observability & Maintenance | 15% | Probes, logs, debugging, API deprecations |

---

## 🗓️ 10-Week Study Timeline

### 🔵 Phase 1 — Foundations & Core Concepts (Weeks 1–3)

| Week | Focus | Key Topics |
|------|-------|-----------|
| Week 1 | Kubernetes Fundamentals & Pods | Architecture, Pods, Multi-container, ConfigMaps, Secrets |
| Week 2 | Workloads | Deployments, Jobs, CronJobs, DaemonSets, Resource Management |
| Week 3 | Storage & Configuration | Volumes, PVCs, SecurityContext, RBAC, ServiceAccounts |

### 🟡 Phase 2 — Services, Networking & Observability (Weeks 4–6)

| Week | Focus | Key Topics |
|------|-------|-----------|
| Week 4 | Services & Networking | ClusterIP/NodePort/LB, DNS, Ingress, NetworkPolicies |
| Week 5 | Observability & Debugging | Probes, Logging, kubectl describe, exec, API deprecations |
| Week 6 | Helm & Exam Readiness | Helm install/upgrade/rollback, Mock Exam #1 |

### 🟠 Phase 3 — Advanced Topics & Exam Readiness (Weeks 7–9)

| Week | Focus | Key Topics |
|------|-------|-----------|
| Week 7 | Advanced Security | Pod Security Admission, RBAC advanced, PodDisruptionBudgets |
| Week 8 | Speed & Exam Technique | kubectl mastery, shell aliases, YAML scaffolding, Mock Exam #2 |
| Week 9 | Intensive Practice | End-to-end scenarios, Mock Exam #3, cheatsheet finalisation |

### 🔴 Phase 4 — Final Week (Week 10)

| Day | Activity |
|-----|----------|
| Mon | Final Mock #4 — Target 85%+ |
| Tue | Review & polish kubectl aliases |
| Wed | Light warm-up practice only |
| Thu | **Rest Day** — no practice |
| Fri | Exam environment setup + 5 warm-up tasks |
| Sat/Sun | 🎓 **EXAM DAY** |

---

## ⏰ Daily Study Routine

| Time | Activity |
|------|----------|
| 20 min | Review yesterday's topics — flashcards/recall |
| 40 min | New concept study — docs or video |
| 45 min | Hands-on kubectl practice |
| 15 min | Update cheatsheet/notes |
| **Total** | **~2 hrs/weekday · ~3–4 hrs/weekend** |

---

## 🛠️ Essential kubectl Aliases

Add to `~/.bashrc` before exam day:

```bash
alias k=kubectl
alias kn='kubectl -n'
alias kgp='kubectl get pods'
alias kgs='kubectl get svc'
alias kd='kubectl describe'
alias kl='kubectl logs'
alias ke='kubectl exec -it'
export do='--dry-run=client -o yaml'
export now='--force --grace-period=0'
```

---

## ⚡ Key Imperative Commands

```bash
# Scaffold Pod YAML
kubectl run nginx --image=nginx --dry-run=client -o yaml

# Create Deployment
kubectl create deploy myapp --image=nginx --replicas=3

# Expose as Service
kubectl expose deploy myapp --port=80 --target-port=8080

# Create ConfigMap
kubectl create cm myconfig --from-literal=key=val

# Create Secret
kubectl create secret generic mysecret --from-literal=pw=abc

# Create Role + RoleBinding
kubectl create role myrole --verb=get,list --resource=pods
kubectl create rolebinding myrb --role=myrole --sa=mynamespace:mysa

# Rollout management
kubectl rollout undo deploy/myapp
kubectl rollout status deploy/myapp

# Debug
kubectl exec -it mypod -- /bin/sh
kubectl top pod --sort-by=cpu
```

---

## 📚 Recommended Resources

### Practice Platforms
| Platform | Notes |
|----------|-------|
| [killer.sh](https://killer.sh) | Official CKAD simulator — 2 free sessions with exam purchase. Hardest available. |
| [KodeKloud](https://kodekloud.com) | Best structured course with built-in labs |
| [Killercoda.com](https://killercoda.com) | Free interactive scenarios — great for daily drills |
| [kind](https://kind.sigs.k8s.io) / [minikube](https://minikube.sigs.k8s.io) | Local free-form practice cluster |

### Study Materials
- 📗 **Primary Course:** KodeKloud CKAD (Mumshad Mannambeth)
- 📖 **Reference:** [kubernetes.io/docs](https://kubernetes.io/docs)
- 💪 **Exercises:** [dgkanatsios/CKAD-exercises](https://github.com/dgkanatsios/CKAD-exercises)
- 🎥 **YouTube:** TechWorld with Nana — Kubernetes full course
- 📘 **Book:** *Kubernetes in Action* (2nd ed.)

### Kubernetes.io Bookmarks
- [Kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
- [Pod API Reference](https://kubernetes.io/docs/reference/kubernetes-api/workload-resources/pod-v1/)
- [Configure Pods & Containers](https://kubernetes.io/docs/tasks/configure-pod-container/)
- [RBAC](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
- [Network Policies](https://kubernetes.io/docs/concepts/services-networking/network-policies/)
- [Persistent Volumes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)

---

## ✅ Progress Tracker

Rate weekly: **1** = Not started · **2** = Learning · **3** = Practising · **4** = Confident · **5** = Exam ready

| Topic | Wk2 | Wk4 | Wk6 | Wk7 | Wk9 | Exam |
|-------|-----|-----|-----|-----|-----|------|
| Pod creation & management | | | | | | |
| Multi-container patterns | | | | | | |
| Deployments & rollouts | | | | | | |
| Jobs & CronJobs | | | | | | |
| ConfigMaps & Secrets | | | | | | |
| Services (all types) | | | | | | |
| Ingress & NetworkPolicy | | | | | | |
| Persistent Volumes & Claims | | | | | | |
| SecurityContext & RBAC | | | | | | |
| Probes & Observability | | | | | | |
| Helm basics | | | | | | |
| kubectl speed & efficiency | | | | | | |

---

## ⚠️ Top 5 Reasons Candidates Fail

1. ⏰ **Running out of time** — not fast enough with kubectl
2. 🔀 **Wrong namespace** — always check the question's namespace
3. ✅ **Not verifying work** — always `kubectl get` after each task
4. 🔄 **Forgetting to switch context** — each question has a specific cluster
5. 📝 **Over-engineering YAML** — write only what the question asks for

---

> 💪 *Consistent daily practice is the key — you've got this, Mohammed!*
