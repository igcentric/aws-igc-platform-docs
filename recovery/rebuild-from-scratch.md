EXAMPLE ONLY - needs to be filled properly

1. High-level architecture

Example:

AWS Organization
 ├── State Account
 ├── Platform Account
 ├── Website Account
 └── Production App Account
2. Repository map

Example:

Repo	Purpose
aws-igc-bootstrap	backend + IAM
aws-igc-platform-infra	VPC/ECS/shared infra
aws-igc-static-website-infra	website infra
igcentric-co-uk-website	website code
3. Bootstrap sequence

Exactly:

Create AWS org
Create accounts
Setup SSO
Configure Terraform backend
Setup GitHub OIDC
Clone repos
Run Terraform in order
4. Credential ownership

This is CRITICAL for non-technical continuity.

Document:

who owns domains
registrar access
GitHub org ownership
AWS root account storage
MFA device location
billing access

Not passwords themselves — but how access is controlled/recovered.

⚠️ One extremely important recommendation

Ensure:

your business partner
OR
a solicitor/executor
OR
secure company records

have access to:

AWS root recovery paths
GitHub organization ownership
domain registrar ownership

Because technically perfect infra is useless if nobody can access the accounts legally/operationally.
