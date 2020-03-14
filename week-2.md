# 第二周


## 三大虛擬機

* Virtual Box

* VMware

  * player:免費版，沒有快照功能

  * workstation:商用版，需花錢購買，功能較完善

  * 原為Oracle公司,後被Red Hat收購,隨後被IBM收購

* Hyper-V

## 指令

* Windows : 
 
    * `ipconfig /all` : 查看網路卡資訊

    * `netstat -rn` : 查看網路卡資訊
    
    * `netstat -an` : 查看實體機上哪些埠被打開

* Linux :

    * `echo` : 反映指令, 打什麼就回應什麼
    
    * `echo hello > Desktop/1.txt` : 輸出到桌面文字檔案 (內文為hello)
    
    * `Desktop/1.txt`:
    
        * 若文字檔存在 -> 清空內容
        
        * 若文字檔不存在 -> 建立文字檔
    
    * `ifconfig` : 查看網路卡資訊
    
    * **正確關機
    
      * `reboot` : 重啟
    
      * `halt-p`
    
      * `power off`
    
    * `su` : 切換為系統管理員(在Linux中為`root`,提示符號為 `#`,若身分為`user`則為 `$`)
    
    * `yum install` : 安裝軟體指令
    
    * `systemctrl stop 伺服器名稱(E.g.ssh)d` : 關閉伺服器
    
    * `systemctrl stop 伺服器名稱(E.g.ssh)d` : 啟動伺服器
    
    * `systemctrl status 伺服器名稱(E.g.ssh)d` : 檢查伺服器狀態
    
    * `netstat -tulnp | grep 22` :
      
      * `t`: 檢查TCP連線
      
      * `u`: 檢查UDP連線
      
      * `l`: Listen
      
      * `n` : 不解析
      
      * `p` : process ID
      
      * `grep` : 過濾器
      
      
