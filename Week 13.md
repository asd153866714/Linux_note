# 課程

### 增量備份

* `tar` 打包和壓縮 

* `touch {01..03}` 創建要備份的檔案

* `tar cvfz backup-0925.tar.gz /home/testdir` 備份 testdir 資料夾內的檔案

* `touch timebase` 備份完成後，立即建立 "時間戳章"

* 變動備份過的檔案

* ```tar cvfz backup-0930.tar.gz `find /home/testdir -cnewer /home/testdir/timebase -type f ` ```用 find 指令找出在時間戳章之後變動的檔案，並備份

* 比較差異備份的檔案 
```
ls backup-0925.tar.gz    
vs     
ls backup-0930.tar.gz
``` 
  

* `tar xvfz backup-0925.tar.gz` 解壓縮

* `tree /home/user/testdir` 用樹狀圖比較

### 篩選內容 grep

* `grep -n user /etc/passwd` 搜尋目錄下檔案內容有 "user" 關鍵字的檔案，"-n" 顯示行數

* `cat /etc/os-release` 查詢 linux 系統

* `grep -i centos /etc/os-release &> /dev/null && echo "centos" || "not centos"` "&&" 前面指令執行成功後才執行後面

* `ifconfig enp0s8 | grep inet | grep -v inet6 | awk '{print$2}' ` "-v" 不要顯示包含該關鍵字的內容，

* `grep -A 1 -B 1 -n user /etc/passwd` "-A", "-B" -> After, Before : 顯示的結果加上前後兩行

### 正則表達式

* `grep -n ^user /etc/passwd` "^user" 顯示以 user 開頭的內容
* `user&` 顯示以 user 結尾的內容
* `^$`    顯示空白行的內容

* "通配符" -> 匹配檔名 
* "正則表達式" -> 匹配內容

### 文字編輯器 vim

* `yum install vim` 安裝

* `vim file` 開啟檔案

* 

# 作業
