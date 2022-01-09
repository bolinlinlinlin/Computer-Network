- 資料：[STP 生成樹協定 - Jan Ho 的網絡世界](https://www.jannet.hk/spanning-tree-protocol-stp-zh-hant/)
## 上課練習1 - 單臂路由
### 環境
![1](/img/20211130-1.jpg)
### SW 設定與 R2 的連接為 trunk
![2](/img/20211130-2.jpg)
### 創建 vlan 與設置 vlan 
![3](/img/20211130-3.jpg)
### R2 設定, 一個接口設定兩個邏輯介面
![4](/img/20211130-4.jpg)
![5](/img/20211130-5.jpg)
### show ip int brief
![6](/img/20211130-6.jpg)
### VPC3 ping 皆可通
![7](/img/20211130-7.jpg)
### 抓 e0/2 封包 
![8](/img/20211130-8.jpg)
## 上課練習3
使全部皆可互通

結果
![9](/img/20211130-9.jpg)
## 上課練習4
### 環境
![10](/img/20211130-10.jpg)
### 設定 Node2 , Layer3 switch 要啟動 ip routing
![11](/img/20211130-11.jpg)
### 設定 vlan 介面
![12](/img/20211130-12.jpg)
### show ip int brief
![13](/img/20211130-13.jpg)
### VPC3 ping
![14](/img/20211130-14.jpg)



