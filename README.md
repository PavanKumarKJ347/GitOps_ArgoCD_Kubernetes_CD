# End to End CD Pipeline Project GitOps ArgoCD

## This Project Can be Used to Build an End to End CD Pipeline GitOps ArgoCD.

## CD Pipeline Stages

- Checkout Code from GitHub.
- Update Docker Image Tag in Kubernetes Manifest.
- Push Updated Kubernetes Deployment File to GitHub.
- Send CICD Pipeline Execution Status to Slack.

### Tools and Technologies Used are Java, Git, GitHub, Maven, SonarQube, Sonatype Nexus, Jenkins, Docker, AWS ECR Registry, Kubernetes and Amazon Web Services.

# Project Execution
## Git Checkout
```bash
  git branch: 'main', url: 'https://github.com/PavanKumarKJ347/GitOps_ArgoCD_Kubernetes_CD.git'
```

## Update Docker Image Tag in Kubernetes Manifest
```bash
  sed -i 's/${application_Name}.*/${application_Name}:${buildNumber}/g' Deployment.yaml
```

## Push Updated Kubernetes Deployment File to GitHub
```bash
  git config --global user.name "DevOpsCloudAutomation"
  git config --global user.email "Pavankumarkj347@gmail.com"
  git add Deployment.yaml
  git commit -m "Updated Build Number in Deployment Manifest File"
  git push https://github.com/DevOpsCloudAutomation/GitOps_ArgoCD_Kubernetes_CD main
```

## Kubernetes Deployment Files are Used to Deploy Application into Kubernetes Cluster.