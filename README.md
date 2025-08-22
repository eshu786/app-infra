# app-infra Repo

## Rollout Demo Branch

This branch (rollout-demo) is for testing Argo Rollouts.

### Updating Image Tags

1. Jenkins builds new Docker images → push to ECR.
2. Update image field in frontend-rollout.yaml or backend-rollout.yaml.
3. Commit & push → ArgoCD automatically syncs and performs the rollout.

### Rollout Strategy

- Frontend: 20% → 50% → 100%
- Backend: 30% → 60% → 100%
