# Working assumptions

These assumptions support the Engineering Manager / Senior Manager take-home submission; they are not confirmed facts from the scenario.

1. **Existing CI/CD pipeline:** An existing build and deployment pipeline can be extended with automated tests and release checks.

2. **Application rollback capability:** Previous application versions are retained and can be redeployed, subject to database compatibility. Rollback does not reverse completed payments or wallet credits; these require reconciliation and approved corrections.

3. **Staging environment:** A separate testing environment and payment-provider sandboxes are available. Verify that their configuration represents the target region closely enough to test critical payment journeys.

4. **Versioned deployments and controlled rollout:** Releases are versioned, with a way to limit exposure during rollout through health checks and a recovery path. Confirm the deployment method; containers, Kubernetes, or replacement servers are possible approaches, not requirements. Rollback supports recovery; controlled rollout limits exposure to a new release.

5. **Ticketing system:** An existing tool can track engineering work, defects, incident follow-up actions, owners, and deadlines. Assess its data quality before using it for delivery metrics.

6. **Production access and observability:** Authorised engineers can access production logs, monitoring, deployment history, and financial records needed to investigate incidents and reconcile transactions. Validate access and identify gaps.

Validate all six assumptions in week one. Where capabilities are missing, establish the minimum safeguards needed and reassess launch scope, capacity, and timing.
