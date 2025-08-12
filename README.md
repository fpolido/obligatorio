## Introducción

Este repositorio contiene dos playbooks de Ansible:

- `nfs_setup.yml`: configura un servidor NFS en sistemas CentOS.
- `hardening.yml`: aplica medidas básicas de hardening en sistemas Ubuntu.

## Requisitos

Antes de ejecutar los playbooks, asegurarse de:

- Tener Ansible instalado.
- Contar con conectividad SSH a los hosts remotos.
- Usar un usuario con privilegios sudo (`sysadmin` en estos playbooks).
- Tener las siguientes colecciones instaladas:

    - community.general
    - ansible.posix

## nfs_setup.yml

Configura un servidor NFS en sistemas CentOS de la siguiente manera:

  - Instala nfs-utils
  - Inicia y habilita nfs-server y rpcbind
  - Permite en el firewall los servicios de:
    - nfs
    - rpcbind
    - mountd
  - Configura el puerto 13025 para el servicio mountd en /etc/nfs.conf
  - Crea el directorio /var/nfs_shared con permisos 0777
  - Añade una entrada en /etc/exports para compartir el directorio
    - Reinicia el servicio NFS si hay cambios

**Como ejecutarlo**

$ ansible-playbook nfs_setup.yml

## hardening.yml

Aplica medidas de hardening a servidores Ubuntu de la siguiente manera:

  - Actualiza todos los paquetes del sistema
    - Reinicia el sistema si es necesario
  - Configura el firewall ufw para:
    - permitir SSH (puerto 22)
    - negar todo lo demás por defecto
  - Refuerza la configuración de SSH:
    - Desactiva acceso por root
    - Habilita autenticación por clave pública
    - Reinicia SSH si hay cambios
  - Instala y habilita fail2ban

**Como ejecutarlo**

$ ansible-playbook hardening.yml
