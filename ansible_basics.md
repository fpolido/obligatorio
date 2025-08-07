# Ansible - Tarea 5

## 1. ¿Qué es Ansible? Mencione dos actividades que se puedan hacer con Ansible

Ansible es una herramienta de automatización de software de código abierto que permite gestionar configuraciones, instalar paquetes, desplegar aplicaciones y manejar servicios en múltiples sistemas desde un único punto de control.

Dos actividades que se pueden hacer con Ansible son:

- Instalar y configurar automáticamente servicios como Apache, NFS, MySQL, etc.
- Aplicar políticas de seguridad y hardening en servidores Linux.

## 2. ¿Qué es un playbook de Ansible?

Un playbook de Ansible es un archivo escrito en formato YAML que describe una serie de tareas a ejecutar sobre grupos o equipos específicos. Es la forma principal de definir automatizaciones reutilizables, detallando qué se debe hacer, en qué orden y sobre qué sistemas.

## 3. ¿Qué información contiene un inventario de Ansible?

El inventario de Ansible contiene la lista de hosts y grupos de hosts que se van a administrar. Puede incluir información adicional como direcciones IP, nombres de usuario, variables específicas para cada host o grupo, etc.

## 4. Explique que es un módulo de Ansible y dé un ejemplo.

Un módulo de Ansible es una unidad de código reutilizable que realiza una acción específica en los sistemas administrados por Ansible, cómo instalar un paquete, copiar un archivo o gestionar servicios. Los módulos son esenciales para la operación de Ansible, ya que definen las tareas que se ejecutan en los playbooks.
Ejemplo: el módulo apt permite gestionar paquetes en sistemas basados en Debian/Ubuntu.

## 5. ¿Que ventajas tiene Ansible sobre otros métodos de automatización?

- Es más simple: Es simple de leer y escribir gracias al uso de YAML por lo que no se necesita saber otro lenguaje
- Es más poderoso: Puede desplegar aplicaciones, gestionar configuraciones, manejar servicios.
- Es más segura: Utiliza una arquitectura sin agentes, utiliza SSH, no hay software que actualizar o que introduzca vulnerabilidades
