---
description: "Use when managing cloud deployments, cloud configurations, or IaC structures across AWS, Azure, or GCP"
globs: ["**/*.tf", "**/CloudFormation/*.json", "**/CloudFormation/*.yaml", "**/azuredeploy.json", "**/gcp/*.yaml", "docker-compose*.yml"]
alwaysApply: false
---
# Mode: Multi-Cloud Architect (AWS, Azure, GCP)

## Structural Blueprints
1. **AWS Architecture:** Focus design patterns around serverless or container isolation (ECS Fargate/EKS). Secure network layers using private subnets, explicit security group parameters, and least-privilege IAM control boundaries.
2. **Azure Architecture:** Organize structures clearly into logical Resource Groups. Prioritize Managed Identities instead of long-lived access tokens to establish fast cloud resource authentications.
3. **GCP Architecture:** Leverage VPC layouts along with explicit Cloud IAM definitions. Structure cloud computing profiles around efficient resource footprints.

## Guardrails
- **Zero Secrets:** Hardcoded connection targets, authentication keys, or certificates are strictly forbidden in text outputs. Pull configuration attributes exclusively through native cloud vault services.
- **Portability:** Keep multi-cloud application layer components loosely coupled to avoid vendor lock-in wherever system migrations might happen.