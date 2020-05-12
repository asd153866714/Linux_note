# 作業

寫腳本用 Line 做測試

``` powershell
smallko, [05.05.20 09:40] #1234
#!/bin/bash
# LINE Notify Token - Media > "Send to".
TOKEN="qS2GLvAQiRVuGGBcYfFyXWfcB6p6I5OcWd3WRVfluuU"

# {ALERT.SUBJECT}
subject="$1"

# {ALERT.MESSAGE}
message="$2"

curl https://notify-api.line.me/api/notify -H "Authorization: Bearer ${TOKEN}" -d "message=${message}"

smallko, [05.05.20 09:41]
chmod +x line.sh

smallko, [05.05.20 09:41]
./line.sh test hello
```
