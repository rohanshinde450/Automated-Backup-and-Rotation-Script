# Automated-Backup-and-Rotation-Script

## 1) First we done a ubuntu server setup on my windows 11.
## 2) Updated Ubuntu server for smooth processing.

![Image](https://github.com/user-attachments/assets/7e6ad859-46a6-4869-8cfa-5e38a34c6bfb)

## 3) Then installed GIT & Rclone.

![Image](https://github.com/user-attachments/assets/223885a0-4460-42b0-b938-5474b5a4d2e2)

## 4) Configured Rclone using following commands.
   1. Rclone config
   2. Press n andn give a name gdrive
   3. Choose number 18 for google drive access
   4. Kept client ID & Secret as it is.
   5. Scope=1
   6. Advance config selected as n(default)
   7. Auto config selected as y(default)
   8. Completed Rclone configuration in google drive.
   9. mkdir ~/mydirectory
   10. Given permision to folder
       sudo chmod 755 ~/mydirectory
   11. Rclone mounted in the folder
       rclone mount newgdrive_backup: ~/mydirectory
       
![Image](https://github.com/user-attachments/assets/17ac9d9a-8939-4c82-bec1-53e191da9101)
![Image](https://github.com/user-attachments/assets/0354a3c2-e511-44f3-a6e7-7d5eed95f6ff)
![Image](https://github.com/user-attachments/assets/a1fab909-dc33-4389-8935-2ec81b837bc3)
![Image](https://github.com/user-attachments/assets/1f682c75-7434-48b8-a457-fcc528b17759)

## 5) Cloned github repository in our local machine

    git clone https://github.com/rohanshinde450/Automated-Backup-and-Rotation-Script.git
    
![Image](https://github.com/user-attachments/assets/c0241135-6f21-40de-88df-6d63bfa32748)
![Image](https://github.com/user-attachments/assets/c06e8088-1a87-4301-950f-8eb47fd78219)

## 6) Full permission given to file
   sudo chmod +x backup.sh
## 7) Executed script ./backup.sh

![Image](https://github.com/user-attachments/assets/b25575cc-d873-4f9d-a5af-6bee5d046943)

## 8) Key Points of Retention Processs Links
    -The first line deletes all .zip files older than a certain number of days specified by $RETENTION_DAYS.
    -The second line identifies files where the date in the filename corresponds to a Sunday, but it doesn’t perform any deletion or retention       action by itself.
    -The third line identifies files where the date in the filename is the 1st of the month, but again, it doesn’t perform any retention or         deletion action directly.
## 9) Result-
   Here we can see the backups that basically store in the Google Drive.
   
![Image](https://github.com/user-attachments/assets/1c322998-5eba-4c14-8833-3be57e1d1050)

   Here we get notification using curl to the webhook's dashboard.
   
![Image](https://github.com/user-attachments/assets/894ca72d-0480-42ef-b612-54460bfcc5ee)
