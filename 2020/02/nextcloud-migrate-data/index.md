# Nextcloud 同步硬碟檔案


將檔案放入Nextcloud/使用者/files資料夾內

執行

```bash
cd /var/www/nextcloud #nextcloud網頁目錄
sudo -u www-data php console.php files:scan --all
```



資料來源：

https://help.nextcloud.com/t/tutorial-how-to-migrate-mass-data-to-a-new-nextcloud-server/9418
