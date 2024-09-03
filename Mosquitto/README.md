💻 **Ubuntu 常見指令教學** 🚀

這個指導你如何在 Ubuntu 系統中使用一些常見的命令。這些指令涵蓋了日常操作、系統管理以及軟體管理等，讓你可以更有效率地使用 Ubuntu。


## 1. 更新軟件包列表
```bash
sudo apt update
```

## 2. 安裝 Mosquitto 和 Mosquitto 客戶端
```bash
sudo apt install mosquitto mosquitto-clients -y
```

## 3. 啟動並設置 Mosquitto 開機自啟
```bash
sudo systemctl start mosquitto
sudo systemctl enable mosquitto
```

## 4. 檢查 Mosquitto 是否正常運行
```bash
sudo systemctl status mosquitto
```

## 5. 修改 Mosquitto 配置文件
```bash
sudo nano /etc/mosquitto/mosquitto.conf
```
在文件中添加以下內容:
```
listener 1883 0.0.0.0
allow_anonymous true
password_file /etc/mosquitto/passwd
```

## 6. 創建帳號
```bash
sudo mosquitto_passwd -c /etc/mosquitto/passwd <用戶名>
```

## 7. 允許端口 1883
```bash
sudo ufw allow 1883
```

## 8. 重啟防火牆
```bash
sudo ufw restart
```

## 9. 重啟 Mosquitto 服務
```bash
sudo systemctl restart mosquitto
```

## 10. 測試
```bash
mosquitto_sub -h <ip> -t test/topic -u <用戶名> -P <密碼>
```


## 版權所有 | License

[版權所有 © 2024 鑽石託管。保留所有權利。](https://discord.gg/5Fky5SEfBd)

---

### Copyright | License

[Copyright © 2024 鑽石託管. All rights reserved.](https://discord.gg/5Fky5SEfBd)