# Planning my Kubernetes Architecture

Thursday, 29 February 2024. 16:56:20GMT

I want to start using and becoming proficient with Kubernetes. And the only real way of doing that is to start
actually using it in the real world.

## Planned Architecture

### Resources to use on Digital Ocean

These will be managed by Terraform:

- Kubernetes single node cluster.
- Nginx Ingress Controller via Helm.
- Managed database cluster
- Container Registry for Building Containers
- Load Balancer (created when using Nginx Ingress Controller)

## Per-website deployment flow

1. Create any resources needed in Terraform:
    - New database in existing database cluster.
    - New subdomain A record for existing domain in Digital Ocean.
    - New Spaces S3 bucket.
2. Commit to a specified branch in Github.
3. Github Action CI/CD 
    - Linting and testing the codebase.
    - Run the "deploy.yml" file on K8s ckuster.
