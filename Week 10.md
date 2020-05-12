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
