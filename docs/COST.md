# 💵 Itemized Infrastructure Cost Analysis

## 📊 Monthly Cost Breakdown (AWS eu-north-1)
* **2x t3.small EC2 Instances**: ~$23.36 / month
* **VPC Network Boundaries & Data Egress**: Free tier / minimal footprint
* **Elastic IPs / Shared NAT Routing**: ~$0.00 (leveraging pure public subnet structure)
* **Total Estimated Monthly Outlay**: **~$23.36**

## ✂️ Strategy to Halve the Infrastructure Cost
1. **Compute Optimization**: Downsize instance types from `t3.small` to `t3.micro` or switch workloads to AWS Spot Instances for a 70% savings margin.
2. **Local Engine Pivot**: Switch the staging environment to an offline multi-node K3d/KinD container topology, driving external cloud provider infrastructure costs directly down to **$0.00**.
