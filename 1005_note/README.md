## Cisco Router設定檔備份與還原(使用TFTP)
### 資料:
- 參考：[Cisco Router設定檔備份與還原(使用TFTP)](http://yearlin101.blogspot.com/2017/08/cisco-routertftp.html)
## TFTP 伺服器
### 資料:
- 參考：[TFTP 伺服器](http://blog.itist.tw/2016/09/install-a-tftp-server-on-centos-7.html)
## 序列埠配置環境
![1005test1_s](/img/1005test1_s.jpg)
- clock rate 64000
![1005clock_rate](/img/1005clock_rate.jpg)
- 時派需同步
- result
![1005test1_s_result](/img/1005test1_s_result.jpg)
## 設置靜態路由
- R1(config)#ip route 23.1.1.0 255.255.255.0 12.1.1.2 (下一跳)
or R1(config)#ip route 23.1.1.0 255.255.255.0 s1/0 (自己的出口)
- ping R2 23.1.1.2 成功 ping R3失敗
- R3(config)#ip route 12.1.1.1 255.255.255.0 s1/0
### 默認路由
- ip route 0.0.0.0 0.0.0.0 [下一跳or出口]