# 上課內容

### 沒安裝 GuestAdditon 要複製文字到虛擬機

* 用 Putty 或 WinSCP

### 腳本

* test.sh :
```
#!/bin/bash
let result = $1 + $2
echo $1 "+" $2 "=" $result
```
* `./test.sh 2 3` 輸出 2 + 3 =8

### curl 

* `curl -- connect-timeout 1 192.116.60.133 ` 設置超時時間
  
* `後面加上 &> dev/null` 輸出結果導入黑洞，不會顯示

* `echo $?` 
  
  * 傳回 0 => 伺服器正常運作
  * 非 0 => 不正常

# 雜記

* `-h` 顯示單位

* `free` 查看記憶體使用情形

* `df` 查看磁碟空間資訊

* `top` 工作管理員

# 作業

* 寫腳本用 Line 做測試 : 
  
1. 建立 Line 群組並加入自己和 LINE Notify

2. 取得權杖並複製到文字文件

3. 編輯 line.sh

4. 測試從 CentOS 來發送通知給 Line
  
``` bash

gedit line.sh &

-----------------------------------------
# line.sh 的內容 :

#!/bin/bash
# LINE Notify Token - Media > "Send to".
TOKEN="qS2GLvAQiRVuGGBcYfFyXWfcB6p6I5OcWd3WRVfluuU"  # 權杖

# {ALERT.SUBJECT}
subject="$1"

# {ALERT.MESSAGE}
message="$2"

curl https://notify-api.line.me/api/notify -H "Authorization: Bearer ${TOKEN}" -d "message=${message}"
------------------------------------------

chmod +x line.sh

./line.sh test hello
```
