💻 **Ubuntu 常見指令教學** 🚀

這個指導你如何在 Ubuntu 系統中使用一些常見的命令。這些指令涵蓋了日常操作、系統管理以及軟體管理等，讓你可以更有效率地使用 Ubuntu。


💻**指令：**

1. **創建使用者** : 
    ```bash
    sudo adduser <用戶名稱>
    ```
2. **創建新用戶的家目錄** : 
   ```bash
   sudo mkdir -p /home/<用戶名稱>/.ssh
   sudo chown <用戶名稱>:<用戶名稱> /home/<用戶名稱>/.ssh
   sudo chmod 700 /home/<用戶名稱>/.ssh
   ```
3. **限制用戶只允許訪問特定路徑** :
   編輯`/etc/ssh/sshd_config`這個檔案
   在檔案最下方輸入:
   ```bash
   Match User <用戶名稱>
    ChrootDirectory <你要指定該用戶可以查看的路徑>
    AllowTcpForwarding no
    X11Forwarding no
    ForceCommand internal-sftp
   ```
4. **設定目錄權限** ：
   ```bash
   sudo chown root:root <你指定的路徑>
   sudo chmod 755 <你指定的路徑>
   sudo chown -R <用戶名稱>:<用戶名稱> <你指定的路徑>/*
   ```
5. **重新啟動 SSH 服務** ：
   ```bash
   sudo systemctl restart ssh
   ```

此設定確保使用者僅能在限制性目錄內編輯文件，無法導航至文件系統的其他部分。