# 作業

* 寫腳本用 Line 做測試 :

``` bash

gedit line.sh &

-----------------------------------------
# line.sh 的內容 :

#!/bin/bash
# LINE Notify Token - Media > "Send to".
TOKEN="qS2GLvAQiRVuGGBcYfFyXWfcB6p6I5OcWd3WRVfluuU"

# {ALERT.SUBJECT}
subject="$1"

# {ALERT.MESSAGE}
message="$2"

curl https://notify-api.line.me/api/notify -H "Authorization: Bearer ${TOKEN}" -d "message=${message}"
------------------------------------------

chmod +x line.sh

./line.sh test hello
```
