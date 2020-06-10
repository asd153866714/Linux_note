# 上課內容

`userdel -r mike` 刪除帳號和使用者家目錄

`usermod -g mike` 修改主要群組

* `chsh tom` 修改 shell

  `/sbin/nologin` 禁止登入

* `cat /etc/passwd | grep 'bash$' | grep -v root | awk -F: '{print $1}' ` 列出可登入的 user (扣除 root)

* `cat /etc/passwd | grep 'bash$' | awk -F: '{if($3 >= 1000){print $1}}' ` 同上，利用 Uid 的特性

* `cat /etc/passwd | grep 'nologin$' | awk -F: '{if($3 >= 1000){print $1}}' ` 列出無法登入的 user

`chmod 777 a.txt` 修改權限

`chown root:root a.txt` 修改擁有者和群組


 
