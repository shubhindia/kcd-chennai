# RDS PostgreSQL Deployment with Crossplane

This demo shows how to provision an Amazon RDS PostgreSQL instance on AWS using Crossplane, OpenSecrecy for encrypted credentials, and a custom Composition.

## Components

- **EncryptedSecret**: Securely stores AWS credentials using [OpenSecrecy](https://opensecrecy.org/docs/).
- **Provider**: Installs the AWS RDS Crossplane provider.
- **ProviderConfig**: Configures the AWS provider to use the stored credentials.
- **Instance**: Provisions a PostgreSQL database instance.
- **Composition**: Defines a complete infrastructure setup including:
  - VPC
  - Subnet
  - DBSubnetGroup
  - SecurityGroup
  - DBInstance

## Files

- `encryptedsecret.yaml` – Encrypted AWS credentials.
- `provider.yaml` – Install and configure AWS RDS provider.
- `providerconfig.yaml` – Link provider with secret credentials.
- `instance.yaml` – Deploy a standalone RDS instance.
- `composition.yaml` – Full RDS setup with networking (VPC, Subnet, SecurityGroup) and database.

