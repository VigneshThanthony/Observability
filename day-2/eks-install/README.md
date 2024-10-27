# **Project Overview**
This project automates the deployment of an EKS cluster on AWS and configures monitoring with the kube-prometheus-stack using Pulumi.

## Prerequisites

- **Pulumi**: Install the Pulumi CLI.
- **AWS CLI**: Install and configure by running `aws configure`.
- **Python**: Install Python 3.8+ and set up a virtual environment.
- **Dependencies**: Install dependencies by running:
  ```bash
  pip install -r requirements.txt


## SetuSetup Instructions
Clone the Repository:

 ```bash
  git clone https://github.com/your-repo-name.git
  cd your-repo-name

## Pulumi Stack Setup: Initialize a Pulumi stack for the environment:

Configure Environment: Add configuration settings (e.g., region, vpcCidr) in environments/<environment>.yaml.

## Deployment Instructions

Preview Changes:

Deploy:

## Access Monitoring Tools

Use port-forwarding commands to access Prometheus and Grafana UIs. Verify deployment using:

 ```bash
kubectl get all -n monitoring

Cleanup Instructions
To delete resources:

State Management Options
Pulumi provides two ways to manage state: Pulumi Cloud or local backend.

Using Pulumi Cloud
Pulumi Cloud provides secure, collaborative state management with history tracking.

Log in:
Using Local State Management
For a local setup, Pulumi stores state files on your filesystem.

Set Local Backend:
Backup: Regularly back up the .pulumi directory, as it stores