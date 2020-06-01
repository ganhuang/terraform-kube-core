# terraform-kube-core

```
.
├── README.md
├── atlantis.yml                               # Configurations for Atlantis
├── azure                                      # Cloud provider
│   ├── dev                                    # Non-prod AKS related resources
│   │   ├── ad-groups                          # Azure AD groups (reader/admin/cluster-admin) for Kubernetes
│   │   └── aks                                # Aks resource
│   │       ├── addons.tf                      # Addons for AKS referencing modules, nginx-controller/newrelic-agent
│   │       ├── backend.tf                     # terraform state backend
│   │       ├── default_vault.tfvars           # Vault secrets, AD server secret
│   │       ├── kube.tf                        # Core module reference
│   │       ├── locals.tf                      # workspace based variables
│   │       ├── rbac.tf                        # RBAC policy for AD group/user
│   │       ├── shared_namespace.tf -> kube-share-namespace/shared_namespace.tf
│   │       └── vars.tf                        # terraform vars
│   └── prod                                   # Prod resources
│       ├── ad-groups
│       └── aks
├── ibm
└── kube-common
    └── shared_namespace.tf                    # Shared resource accross cloudprovider, like namespace
                                               # namespace restriction, quote/limit
```
