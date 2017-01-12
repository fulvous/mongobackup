# mongobackup
Script for backing up mongo database and rotate it

# Installation
git clone https://github.com/fulvous/mongobackup.git

# Usage

Usage: mongobackup [-f backup_folder] [-d databases] [-v]

This script backs up and rotate mongo databases

   -f sets the backup folder
   -d Databases to backup separated by commas
   -v Shows verbose information

Example for /etc/crontab: 

  0 2 * * * root /usr/local/sbin/./mongobackup -f /opt/backup -d my_db
