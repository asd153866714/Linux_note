### 指令的輸出入

編號 | 訊息
-----|------
0|標準輸入
1|標準輸出
2|錯誤訊息

* `hello > 1.txt` 把 hello 輸出到 1.txt (會覆蓋掉原本內容)

* `hi >> 1.txt` 附加訊息

* `ls /home &> ouput.txt` "&" = "1, 2" 輸出正確和錯誤訊息到同一個檔案

* `cat < 1.txt` 標準輸入

* `cat 1.txt | tee 4.txt`

* `|` 通道:

  * 前方輸入為後方輸出
  * `wc < 1.txt` "wc" 統計資料 
 
### 搜尋系統

* `which ifconfig` 搜尋 PATH 目錄裡，是否有執行檔

* `whereis ifconfig` 用完整檔名搜尋，獲得檔案位置

* `find` :

  * `find /home -name jack` 搜尋 /home 目錄下檔名為 jack 的檔案
  
  * `find /home -iname jack` 不分大小寫
  
  * `find /home -name "*.txt"` "\*" 為通配符號 
  
    1. \*
    2. ?
    3. []
  
  * `find . -type f -name a` "-type"為檔案類型 
  
    * f : 檔案
    * d : 資料夾
    
  * `find . ype f -perm 777` "-perm" 為檔案權限 
  
  * `find . -name "*.txt" -type f -exec rm -f {}\; ` "-exec" 找到後執行指令，將搜尋到的檔案放入{ }並刪除
  
  * `find . -tyoe d -empty -exec rmdir {}\; ` 將空資料夾刪除
  
  * `find . -mtime -7 ` 7天內有修改過的檔案
  
  * `find . -size +5M ` 大於 5MB 的檔案
