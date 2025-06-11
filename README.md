# Trabajo Práctico Integrador

## Participantes
- Lisandro Santoro
- Manuel Lopez Ventura
- Tomas Juarez

## Descripción
Este repositorio contiene la documentación y los archivos comprimidos correspondientes al Trabajo Práctico Integrador de la materia Administración de Sistemas Operativos, realizado en una máquina virtual Debian 11.

## Estructura de directorios comprimidos

Los siguientes directorios del sistema fueron comprimidos individualmente en formato `.tar.gz`:

- `/root` → `root.tar.gz`
- `/etc` → `etc.tar.gz`
- `/opt` → `opt.tar.gz`
- `/proc` → `proc.tar.gz`
- `/www_dir` → `www_dir.tar.gz`
- `/backup_dir` → `backup_dir.tar.gz`

El directorio `/var` fue dividido en partes más pequeñas para cumplir con las limitaciones de GitHub:

- `var_part_aa`, `var_part_ab`, `var_part_ac`, ...

## Script de Backup

En el directorio `/opt/scripts` se encuentra el script `backup_full.sh`, que realiza backups comprimidos con las siguientes características:

- Permite indicar origen y destino como parámetros.
- Valida que los sistemas de archivos estén montados.
- Incluye una opción `-help` para mostrar ayuda.
- Genera backups con nombres fechados (formato YYYYMMDD).
- Está programado en el cron para:
  - Ejecutarse todos los días a las 00:00 para `/var/logs`.
  - Lunes, miércoles y viernes a las 23:00 para `/www_dir`.

## Configuraciones realizadas

- Configuración de red con IP estática.
- Apache instalado y configurado con PHP 7.4.
- Archivo `index.php` y `logo.png` alojados en `/www_dir`.
- MariaDB instalado y configurado.
- Servicio SSH configurado con acceso por clave pública/privada al usuario root.
- Creación y montaje automático de las particiones `/www_dir`, `/backup_dir` y `/var/logs`.

---

📌 **Nota:** Todos los archivos fueron extraídos desde la máquina virtual y están disponibles para revisión y restauración.
