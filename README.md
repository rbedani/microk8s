Playbook for deploy Cluster of Kubernetes

11/04/2023
Proximo Change: Cloudfire
--------


---
10/04/2023
Instalación de Microk8s

├── roles
│   └── install_microk8s
│       ├── defaults
│       │   └── main.yml
│       └── tasks
│           ├── add_alias.yml
│           ├── add_groups.yml
│           ├── config_kubectl.yml
│           ├── config_repo_helm.yml
│           ├── install_microk8s.yml
│           ├── install_snapd.yml
│           ├── main.yml
│           ├── microk8s_addons.yml
│           ├── microk8s_certificates.yml
│           ├── microk8s_configure-HA.yml
│           └── microk8s_configure_workers.yml
└── run.yml

defaults:
Contiene la plantilla de las variables globales para realizar la instalación de microk8s.
Para elevación de permisos verificar la variable de ansible_become_password.

Los addons deben ajustarse al criterio del proyecto.

Important:
Es importante especificar el grupo de Workers y Nodos Master.

About:
Se ha probado sobre entornos de laboratorio.
2 VM - Ubuntu 22.04 LTS

--------


Rodrigo Daniel Bedani
rbedani@flexxible.com
DevOps | Flexxible IT