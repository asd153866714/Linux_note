# 上課內容

`userdel -r mike` 刪除帳號和使用者家目錄

`usermod -g mike` 修改主要群組

`chsh tom` 修改 shell

  `/sbin/nologin` 禁止登入

1. `cat /etc/passwd | grep 'bash$' | grep -v root | awk -F: '{print $1}' `
2. `cat /etc/passwd | grep 'bash$' | awk -F: '{if($3 >= 1000){print $1}}' `

`cat /etc/passwd | grep 'nologin$' | awk -F: '{if($3 >= 1000){print $1}}' `

`chmod 777 a.txt` 修改權限

`chown root:root a.txt` 修改擁有者和群組


 
