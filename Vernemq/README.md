💻 **Ubuntu 常見指令教學** 🚀

這個指導你如何在 Ubuntu 系統中使用一些常見的命令。這些指令涵蓋了日常操作、系統管理以及軟體管理等，讓你可以更有效率地使用 Ubuntu。


# 安裝 libssl1.1 🛠️
```bash
wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2_amd64.deb
sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2_amd64.deb
sudo apt-cache policy libssl1.1
sudo apt-get update
```

# 安裝 VerneMQ 🚀
```bash
sudo apt-get install libtinfo5
wget https://github.com/vernemq/vernemq/releases/download/1.12.6.2/vernemq-1.12.6.2.bionic.x86_64.deb
sudo dpkg -i vernemq-1.12.6.2.bionic.x86_64.deb
dpkg -s vernemq | grep Status
```

# 下載 VERNEMQ - 設定修改 ✏️
```bash
sudo nano /etc/vernemq/vernemq.conf
accept_eula=yes

# IP
# 找到 8888 官方預設 http port
# 下方加入

listener.http.default=127.0.0.1:9001
listener.ws.default=192.168.59.253:9001
listener.ws.localhost=127.0.0.1:9001
listener.tcp.localhost=127.0.0.1:1883
listener.tcp.default=192.168.59.253:1883
```

# 啟動 🚀
```bash
service vernemq start
```

# 關閉 🛑
```bash
service vernemq stop
```

# 確認啟動 ✅
```bash
sudo vmq-admin cluster show
sudo vmq-admin listener show
```

# 啟動伺服器有錯誤時檢查用 🧐
```bash
systemctl status vernemq.service
journalctl -xeu vernemq.service
```

# 檢查 config 是否有問題 🔍
```bash
vernemq config generate -l debug
```


## 版權所有 | License

[版權所有 © 2024 鑽石託管。保留所有權利。](https://discord.gg/5Fky5SEfBd)

---

### Copyright | License

[Copyright © 2024 鑽石託管. All rights reserved.](https://discord.gg/5Fky5SEfBd)