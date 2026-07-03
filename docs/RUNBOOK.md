# 📖 Phoenix Capstone Project Runbook

## 🏗️ Infrastructure Layer (Terraform)
The infrastructure is provisioned on AWS (`eu-north-1`) using custom modules:
* **VPC Network**: 10.0.0.0/16 mesh with an active public gateway channel.
* **Compute**: Multi-node architecture tracking Ubuntu 22.04 LTS AMIs.
* **Firewalls**: Port 22 locked down safely, ports 80/443 exposed for user access. 

## 🚀 Deployment Layer (Kubernetes)
The applications are deployed natively on a lightweight multi-node cluster configuration:
* **Database**: StatefulSet PostgreSQL deployment matching high-availability volumes.
* **Workloads**: Multi-replica deployments for both backend and frontend tiers.
* **Service Mesh**: Internal cluster discovery routing traffic cleanly using service abstractions.

## 🔍 Validation Commands
```bash
# Check overall cluster component topology status
kubectl get nodes -o wide

# Check live workload rollout metrics
kubectl get pods -n taskapp -o wide
```
