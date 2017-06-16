# mongobackup
Script para respaldar bases de datos mongodb y rotar los respaldos viejos.

# Instalacion
git clone https://github.com/fulvous/mongobackup.git

# Uso

Uso: mongobackup [-f directorio_respaldo] [-d bases] [-o anterior_a] [-v]

Este script respalda bases de datos mongodb y rota sus respectivos respaldos.

   -f define el directorio en donde se respaldarán los datos.
   
   -d Bases de datos a respaldar separadas por comas.
   
   -o Se borraran los respaldos mas viejos a este numero de dias.
   
   -v Muestra informacion adicional

Ejemplo de configuracion en /etc/crontab: 

  0 2 * * * root /ruta_completa/mongobackup -f /opt/respaldos -d mi_base -o 2

  Esto ejecutara el comando todos los dias a las 2am
  
  Utilizara /opt/respaldos como el directorio de respaldos
  
  Respaldara la base mi_base y la comprimira en 7z
  
  Borrara los respaldos mayores a 2 dias




# mongobackup
Script for backing up mongo database and rotate it

# Installation
git clone https://github.com/fulvous/mongobackup.git

# Usage

Usage: mongobackup [-f backup_folder] [-d databases] [-o older_than] [-v]

This script backs up and rotate mongo databases

   -f sets the backup folder
   
   -d Databases to backup separated by commas
   
   -o Erase backups older than this number of days
   
   -v Shows verbose information

Example for /etc/crontab: 

  0 2 * * * root /full_path/mongobackup -f /opt/backup -d my_db -o 2

  This will execute the command at 2 am everyday,
  
  using /opt/backup as destination folder,
  
  backing up 'my_db' database into a 7z file,
  
  erasing backups older than 2 days.
