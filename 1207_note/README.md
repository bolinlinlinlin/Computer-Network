- 資料：[STP 生成樹協定 - Jan Ho 的網絡世界](https://www.jannet.hk/spanning-tree-protocol-stp-zh-hant/)

## Spanning Tree Steps
### Step1: 
    選舉 Root Switch 
    找出最小 :priority(預設值32768+Vlan ID) + MAC address    
### Step2:
    選擇 Root Port 
![16](/img/20211130-16.jpg)
### Step3:
    選擇 Designated Port 與 Non-Designated Port
## 上課練習1
### 環境
![17](/img/20211130-17.jpg)
### 設定 SW1 vlan 
![18](/img/20211130-18.jpg)
### 設定 SW2 vlan 
![19](/img/20211130-19.jpg)
### 設定 SW3 vlan 
![20](/img/20211130-20.jpg)
### SW1 show spanning tree vlan 1
![21](/img/20211130-21.jpg)
### SW1 show spanning tree vlan 10 顯示不存在?(原因:要加上trunk,同理 SW2 SW3)
![22](/img/20211130-22.jpg)
### SW1 show spanning tree vlan 10
![23](/img/20211130-23.jpg)
### SW1 show spanning tree vlan 20
![24](/img/20211130-24.jpg)
### 設定 SW2 ,使他成為 vlan 20 的 root
![25](/img/20211130-25.jpg)
### show spanning tree vlan 20 
![26](/img/20211130-26.jpg)
## 上課練習2 -Etherchannel
### 環境
![27](/img/20211130-27.jpg)
### 設定 SW1 
![28](/img/20211130-28.jpg)
### 設定 SW2 
![29](/img/20211130-29.jpg)
### show etherchannel summary 產生 port-channel 1
![30](/img/20211130-30.jpg)
### show interface e0/0 單一路線頻寬 10M
![31](/img/20211130-31.jpg)
### sh inter port-channel 1 為 20M
![32](/img/20211130-32.jpg)