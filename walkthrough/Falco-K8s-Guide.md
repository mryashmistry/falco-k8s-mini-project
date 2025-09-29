# Falco on Kubernetes – Learning Curve Project (Steps 2 → 5)

This document continues from Step 1 (installation) and covers:
- **Step 2** — Understanding Falco rules
- **Step 3** — Generating custom rules
- **Step 4** — Viewing logs & alerts
- **Step 5** — Integrations and next steps

> Images referenced below are in `../images/` (repo root `images/` folder).

---

## Step 2 — Understanding Falco rules (quick)
Falco evaluates kernel events against rule files to detect suspicious activities (e.g., unexpected file reads/writes, privilege escalation, suspicious network behavior).

**Default rules:** `https://github.com/falcosecurity/rules/blob/main/rules/falco_rules.yaml`

**Example to trigger a default warning (for reference only — do not run here):**
```bash
kubectl create deployment nginx --image=nginx
kubectl exec -it $(kubectl get pods --selector=app=nginx -o name) -- cat /etc/shadow
# Check Falco logs for warnings:
kubectl logs -l app.kubernetes.io/name=falco -n falco -c falco | grep -i Warning

GUIDE
