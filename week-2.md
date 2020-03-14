# 第二周


## 三大虛擬機

* Virtual Box

* VMware

  * player:免費版，沒有快照功能

  * workstation:商用版，需花錢購買，功能較完善

  * 原為Oracle公司,後被Red Hat收購,隨後被IBM收購

* Hyper-V

## 指令

 ### Windows : 

     * `ipconfig /all` : 查看網路卡資訊

     * `netstat -rn` : 查看網路卡資訊

     * `netstat -an` : 查看實體機上哪些埠被打開

### Linux :

    * `echo` : 反映指令, 打什麼就回應什麼
    
    * `echo hello > Desktop/1.txt` : 輸出到桌面文字檔案 (內文為hello)
    
    * `Desktop/1.txt`:
    
        * 若文字檔存在 -> 清空內容
        
        * 若文字檔不存在 -> 建立文字檔
    
    * `ifconfig` : 查看網路卡資訊
    
    * **正確關機**
    
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
      
 ### 遠端桌面連線方式

* 開啟方式 : `開始 → 搜尋列上輸入"mstsc"`

* 輸入欲連線到的電腦IP後加上冒號+埠號。

    -E.g.192.168.1.150:5566(從實體機遠端登入虛擬機時的練習)
    
### 再製

1. 完整再製 : 浪費磁碟空間但效能好

2. 連結再製 : 節省磁碟空間但效能差

### 網卡模式

1. `NAT`: network address translation

   * centos可看到Internet上的機器，但Internet上的機器看不到centos。
   
   * 在Virtualbox內，centos看不到windows，windows也看不到centos。(但在VMware下，centos和windows可互相看到。)

2. `Host-only模式`

   * centos和windows可互相看到，但centos不能看到Iternet上的機器。
   
3. `Bridge`:橋切設定

   * 一般不會開，除非要測試。

4. `內部網路`

   * 虛擬機內部網路名稱相同就可以相連。
    
### Linux提供的三種標準I/O

1. standard input (STDIN) 代號 0：標準輸入，預設為鍵盤

2. standard output (STDOUT) 代號 1：標準輸出，預設為終端機視窗

3. standard error (STDERR) 代號 2：標準錯誤輸出，預設為終端機視窗

