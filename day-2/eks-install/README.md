# **Project Overview**
This project automates the deployment of an EKS cluster on AWS and configures monitoring with the kube-prometheus-stack using Pulumi.

## Prerequisites
Pulumi: Install Pulumi CLI.
AWS CLI: Install, then configure with aws configure.
Python: Install Python 3.8+ and set up a virtual environment.
Dependencies: Install with:

```Copy code```
pip install -r requirements.txt
Environment Setup
Clone the Repository:


```Copy code```
git clone https://github.com/your-repo-name.git
cd your-repo-name
Pulumi Stack Setup:

Initialize a Pulumi stack for the environment:

```Copy code```
pulumi stack init dev
Configure Environment:

Add configuration settings (e.g., region, vpcCidr) in environments/<environment>.yaml.
Running the Code
Preview Changes:


```Copy code```
pulumi preview
Deploy:


```Copy code```
pulumi up
Access Monitoring Tools
Use port-forwarding commands to access Prometheus and Grafana UIs. Verify deployment using:


```Copy code```
kubectl get all -n monitoring
Cleanup
To delete resources:


```Copy code```
pulumi destroy

State Management Options
Pulumi provides two ways to manage state: Pulumi Cloud or local backend.

Using Pulumi Cloud
Pulumi Cloud provides secure, collaborative state management with history tracking.

Log in:

```Copy code```
pulumi login

Pulumi Cloud automatically saves the stack state online for collaborative use.
Using Local State Management
For a local setup, Pulumi stores state files on your filesystem.

Set Local Backend:
```Copy code```
pulumi login --local

Backup: Regularly back up the .pulumi directory, as it stores all stack state files.