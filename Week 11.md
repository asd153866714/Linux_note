

### 符號連結 :

* `ln -s 目標 連結名稱` 

  * 權限全開
  * 檔案大小不變
  * inode 不同

### 硬連結 :

* `ln 目標 連結名稱`

  * 權限一樣
  * 大小一樣
  * 連結數增加
  * inode 相同

* **課本 5-8 表格 期末必考**

### Linux 的執行檔 :

* 附檔名沒有特別規定( 只要有 Execute 權限 )

### 環境變數

 * `echo $PATH` : 顯示 PATH 變數
 
 * `export PATH=$PATH:/home/user/exec` : 加入 PATH 變數
 
 * 讓 PATH 變數永遠生效 : 
 
   1. 到家目錄 cd ..
   2. `gedit .bashrc` 編輯
   3. 加上 `export PATH=$PATH:/home/user/exec`

* `df -h` : 顯示磁碟分割區， -h 顯示單位

* `du` : 


# 雜記

* 大括號用法 :

  `touch {1 .. 10}` : 一次產生10個檔案

  `gedit {1 .. 10}` : 一次編輯10 個檔案
  
 * `mkdir -p 1` : -p 若資料夾不存在就新增，反之則不做動作
 
 * `ls -ld /data` : 顯示資料夾權限
 
  * r : 可讀取 ls
  * x : 可進入 cd
  * w : 可新增或刪除檔案 touch, rm
  
 * `stat 1` : 查詢檔案詳細資料 (使用，修改，建立)
  
   * 參考 : https://www.itread01.com/content/1543589762.html
 
 * `lsattr` 
  
   * 參考 : https://www.runoob.com/linux/linux-comm-lsattr.html
 
 
 * `file` : 顯示檔案或指令詳細資訊
 
 * `type` : 是否為 shell 指令
