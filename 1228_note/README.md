## 上課練習1
### 環境
![1](/img/20211228-1.jpg)
### R1 設置靜態路由
![2](/img/20211228-2.jpg)
### R2 
![3](/img/20211228-3.jpg)
### R4 設置 telnet
![4](/img/20211228-4.jpg)
### R4 設置內定路由
![5](/img/20211228-5.jpg)
### R2 設置 ACL and PAT  
![6](/img/20211228-6.jpg)
### 使用靜態NAT
![7](/img/20211228-7.jpg)
### R3 telnet
![8](/img/20211228-8.jpg)
- 資料：[HSRP VRRP GLBP 第一跳冗餘協定 - Jan Ho 的網絡世界](https://www.jannet.hk/first-hop-redundancy-protocol-fhrp-zh-hant/)
## 上課練習2
### 環境
![9](/img/20211228-9.jpg)
### R3
![10](/img/20211228-10.jpg)
### R4
![11](/img/20211228-11.jpg)
### R1
![12](/img/20211228-12.jpg)
### R2
![13](/img/20211228-13.jpg)
### Hot Standby Redundancy Protocol (HSRP)
### R1
![14](/img/20211228-14.jpg)
### R1 show standby
![15](/img/20211228-15.jpg)
### R2 
![16](/img/20211228-16.jpg)
### R2 show standby
![17](/img/20211228-17.jpg)
### R1 show ip arp 
![18](/img/20211228-18.jpg)
### R1 須設定 preempt,權重較大
![19](/img/20211228-19.jpg)
### 如果 R1 的 e0/1 接口斷線, standby 的狀態還是 Active
![20](/img/20211228-20.jpg)
## 延伸上課練習2
### 環境
![21](/img/20211228-21.jpg)
### 結果
![22](/img/20211228-22.jpg)