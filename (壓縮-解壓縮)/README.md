💻 **Ubuntu 常見指令教學** 🚀

這個指導你如何在 Ubuntu 系統中使用一些常見的命令。這些指令涵蓋了日常操作、系統管理以及軟體管理等，讓你可以更有效率地使用 Ubuntu。


# Ubuntu 壓縮與解壓縮檔案教學

## 使用壓縮檔案

### 1. 使用 `zip` 壓縮檔案
`zip` 指令可以將文件或文件夾壓縮為 `.zip` 格式。
```bash
zip -r 壓縮檔案名稱.zip 目標文件或文件夾
```
例如：
```bash
zip -r my_archive.zip my_folder
```

### 2. 使用 `tar` 壓縮檔案
`tar` 指令可以將多個文件或文件夾打包成一個 `.tar` 檔案，並且可以選擇性地進行壓縮。
```bash
tar -cvf 壓縮檔案名稱.tar 目標文件或文件夾
```
如果需要進行壓縮，可以使用 `gzip` 或 `bzip2`：
```bash
tar -cvzf 壓縮檔案名稱.tar.gz 目標文件或文件夾
```
例如：
```bash
tar -cvzf my_archive.tar.gz my_folder
```

## 使用解壓縮檔案

### 1. 解壓 `.zip` 檔案
使用 `unzip` 指令可以解壓 `.zip` 檔案。
```bash
unzip 壓縮檔案名稱.zip
```

### 2. 解壓 `.tar` 檔案
使用 `tar` 指令解壓 `.tar` 檔案：
```bash
tar -xvf 壓縮檔案名稱.tar
```
如果檔案經過壓縮，則使用以下指令：
```bash
tar -xvzf 壓縮檔案名稱.tar.gz
```

## 其他常用指令

### 1. 列出 `.zip` 檔案內容
```bash
unzip -l 壓縮檔案名稱.zip
```

### 2. 列出 `.tar` 檔案內容
```bash
tar -tvf 壓縮檔案名稱.tar
```


此設定確保使用者僅能在限制性目錄內編輯文件，無法導航至文件系統的其他部分。
