# ch7 使用者帳號管理

`groupadd rd` 新增使用者群組 "rd"

`cat /etc/group` 查看 group 資料(群組名稱，GID)

`useradd mike` 新增使用者 "mike"

`cat etc/passwd` 帳號資料

`echo $SHELL` 查看帳號 shell **--期末**

`cat /etc/passwd | grep ^user | awk -F: '{print $NF}'`
  
                          |            |            |
                          user開頭     :冒號分隔     印出最後一個
                          
`id jack` 查看帳號 jack 的資訊

`useradd -g user jack` 建立新帳號 jack 並加入 user 群組

# 雜記

### awk 

# 作業

### 安裝新硬碟

參考課本 6-5 頁

### 掛載 FAT32 USB

參考課本 6-14 頁

### 掛載 NTFS USB

參考 -- https://codertw.com/%E4%BC%BA%E6%9C%8D%E5%99%A8/378866/
