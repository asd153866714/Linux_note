# ch7 使用者帳號管理

`groupadd rd` 新增使用者群組 "rd"

`cat /etc/group` 查看 group 資料(群組名稱，GID)

`useradd mike` 新增使用者 "mike"

`cat etc/passwd` 帳號資料

`echo $SHELL` **期末**

`cat /etc/passwd | grep ^user | awk -F: '{print $NF}'`
  
                        |            |            |
                        user開頭      :冒號分隔     印出最後一個
