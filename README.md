### How to backup?
Backup continuously to S3.

```
docker run -v DIRECTORY_TO_BACKUP:/data gregory90/mysql-backup-s3 /app/run
```

##### Environment variables
TIMEOUT - how often perform backup, in seconds,  
AWS\_ACCESS\_KEY\_ID- AWS S3 access key,  
AWS\_SECRET\_ACCESS\_KEY - AWS S3 secret key,  
BUCKET - AWS S3 bucket for backup,   
DBHOST - MySQL host,  
DBUSER - MySQL user,  
DBPASS - MySQL password.  

### Restore backup
Restore database from S3.

```
docker run -v DIRECTORY_TO_RESTORE_TO:/data gregory90/mysql-backup-s3 /app/restore
```

##### Environment variables
AWS\_ACCESS\_KEY\_ID- AWS S3 access key,  
AWS\_SECRET\_ACCESS\_KEY - AWS S3 secret key,  
FILE - file to restore,  
BUCKET - AWS S3 bucket for backup,  
