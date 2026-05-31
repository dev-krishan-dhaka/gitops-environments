# GitOps Environments

Single source of truth for all deployments.

## Structure
- dev/    → development (auto-updated by Jenkins)
- stage/  → staging (manual PR required)
- prod/   → production (manual PR required)

## How deployments work
1. Jenkins CI builds image and updates dev/ values
2. ArgoCD detects change and deploys automatically
3. For stage/prod promote manually via PR
