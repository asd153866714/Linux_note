# 上課內容

* `userdel -r mike` 刪除帳號和使用者家目錄 **-- 期末**

* `usermod -g mike` 修改主要群組
      
|選項|用法| 
|---|---|
|-g|主要群組|
|-G|附加群組|
|-u|UID 編號|
|-d|家目錄 |
|-c|註解|
|-e|日期|

* `chsh tom` 修改 shell

    * `/sbin/nologin` 禁止登入

* `cat /etc/passwd | grep 'bash$' | grep -v root | awk -F: '{print $1}' ` 列出可登入的 user (扣除 root)

* `cat /etc/passwd | grep 'bash$' | awk -F: '{if($3 >= 1000){print $1}}' ` 同上，利用 Uid 的特性

* `cat /etc/passwd | grep 'nologin$' | awk -F: '{if($3 >= 1000){print $1}}' ` 列出無法登入的 user

`chmod 777 a.txt` 修改權限

`chown root:root a.txt` 修改擁有者和群組

# 雜記

### sed

全名 : stream editor 

用串流的方式，一次讀取一行

`sed -i '5,10d' a.txt` 刪除 5~10 行

`sed -n '5,10d' a.txt` 顯示刪除後的結果，但沒有真的刪除

* `sed -i '/.*\$/d' a.txt` 刪除以 '/'結尾的段落
   
      * '.' 任意個字元
      * '*' 重複多次
      * '\' 跳脫字元

`sed -i '/^$/d' a.txt ` 刪除空白行

`sed -i '40,45/^named/d' a.txt ` 刪除 40~45 行以 named 開頭的

# 作業
f
