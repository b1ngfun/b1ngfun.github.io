# 樹莓派安裝 Resilio Sync


### 1. 新增軟體源

##### 	建立文件

```bash
touch /etc/apt/sources.list.d/resilio-sync.list
nano /etc/apt/sources.list.d/resilio-sync.list
```

### 2. 加入以下內容

```bash
deb http://linux-packages.resilio.com/resilio-sync/deb resilio-sync non-free
```

編輯完畢後按Ctrl+x，Y儲存。

### 3. 加入公鑰

```bash
wget -qO - https://linux-packages.resilio.com/resilio-sync/key.asc | sudo apt-key add -
```

### 4. 更新軟體源

```bash
sudo dpkg --add-architecture armhf
sudo apt-get update
```

### 5. 在  /etc/apt/sources.list  中新增

```bash
deb [arch=armhf] http://linux-packages.resilio.com/resilio-sync/deb resilio-sync non-free
```

### 6. 開始安裝

```bash
sudo apt-get update
sudo apt-get install resilio-sync
```

### 7. 安裝完成移除軟體源

```bash
rm /etc/apt/sources.list.d/resilio-sync.list
```

### 8. 設定開機啟動

```bash
sudo systemctl enable resilio-sync
```

##### 	開啟瀏覽器 預設port為8888

##### 	ex. 192.168.0.100:8888



### 9. 資料夾權限錯誤解決辦法

```bash
chown -R rslsync /資料夾路徑
```



資料來源

https://www.jianshu.com/p/db301108383b

https://totoro.ink/bash/raspberry-resilio-sync.html

https://dietpi.com/phpbb/viewtopic.php?t=2086
