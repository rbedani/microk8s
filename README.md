---
05/05/2023
add function for apply and delete deployments
add funciion for arguments file manifest that kubernetes

Playbook for deploy Cluster of Kubernetes
---
19/04/2023
- Update roles install ( add export config for ansible-kubectl )
- Update roles remove ( config for kubectl and table hosts )

---
15/04/2023
Roles updates:
    * remove microk8s
    * install microk8s

Install:
    ansible-playbook run.yml -e "install=true"
Remove:
    ansible-playbook run.yml -e "remove=true"

---
11/04/2023
Proximo Change: Cloudfire
---



---
10/04/2023 - Update 19/04/2023
Instalación de Microk8s
```shell
├── roles
│   ├── install_microk8s
│   │   ├── defaults
│   │   │   └── main.yml
│   │   └── tasks
│   │       ├── add_alias.yml
│   │       ├── add_groups.yml
│   │       ├── config_kubectl.yml
│   │       ├── install_microk8s.yml
│   │       ├── install_snapd.yml
│   │       ├── main.yml
│   │       ├── microk8s_addons.yml
│   │       ├── microk8s_certificates.yml
│   │       ├── microk8s_configure-HA.yml
│   │       ├── microk8s_configure_workers.yml
│   │       ├── microk8s_export_config.yml
│   │       └── microk8s_helm.yml
│   ├── remove_microk8s
│   │   ├── defaults
│   │   │   └── main.yml
│   │   └── tasks
│   │       ├── main.yml
│   │       ├── microk8s_stop.yml
│   │       ├── remove_alias.yml
│   │       ├── remove_groups.yml
│   │       ├── remove_hosts.yml
│   │       ├── remove_kubectl.yml
│   │       ├── remove_microk8s.yml
│   │       └── remove_snapd.yml
└── run.yml
```
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