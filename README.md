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

  This will execute the command at 2 am everyday,\n
  using /opt/backup as destination folder,\n
  backing up 'my_db' database into a 7z file,\n
  erasing backups older than 2 days.
