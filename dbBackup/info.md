# Backups and Restore

### Taking backup from local database. Remember to change the file name to current date.

pg_dump -h localhost -p 5432 -U postgres --format=c leikur > D:\strapi-projects\leikur-strapi\dbBackup\local\2021-07-16.dump

### Restoring local backup to Heroku:

heroku pg:backups:restore '<ClodinaryURL for the backup>' DATABASE_URL -a leikur-strapi

### Getting backup from Heroku:

1. Navigate in the terminal to:
   D:\strapi-projects\leikur-strapi\dbBackup\heroku
2. Run in the terminal:
   heroku pg:backups:capture -a leikur-strapi
3. Run in the terminal:
   heroku pg:backups:download -a leikur-strapi
