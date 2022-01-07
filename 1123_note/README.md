## 上課練習1
### 環境
![1](/img/20211123-1.jpg)
### SW1設定
![2](/img/20211123-2.jpg)
### SW2設定
![3](/img/20211123-3.jpg)
### SW1 設置 trunk(802.1q) (在SW1與SW2之間),同理 SW2
![4](/img/20211123-4.jpg)
### show interface trunk
![5](/img/20211123-5.jpg)
### trunk 會貼標籤
![6](/img/20211123-6.jpg)
### 延伸環境
![7](/img/20211123-7.jpg)
### ping 192.168.0.2 並無802.1q (對於native vlan來說,不須設定access即可使用)
![8](/img/20211123-8.jpg)
### 設定 SW1 native vlan 改為10
![9](/img/20211123-9.jpg)
### 設定 SW2 native vlan 改為10
![10](/img/20211123-10.jpg)
### VPC3 ping VPC5
![11](/img/20211123-11.jpg)
### VPC7 ping VPC8
![12](/img/20211123-12.jpg)

## VTP (vlan trunking protocol) 這是思科私有的技術,用於實現對於vlan的全局管理(創建,刪除,修改)


### vtp mode 能創建,刪除,修改vlan
client 不能創建,刪除,修改vlan,但能學習轉發
transparent 能創建,刪除,修改vlan,不能學習轉發 
- 資料：[VTP 虛擬區域網絡中繼協定 - Jan Ho 的網絡世界](https://www.jannet.hk/vlan-trunking-protocol-vtp-zh-hant/)

## 上課練習2
### 環境
![13](/img/20211123-13.jpg)
### SW1 設定trunk, 同理SW2
![14](/img/20211123-14.jpg)
### SW1 設定VTP server
![15](/img/20211123-15.jpg)
### show vtp status 
![16](/img/20211123-16.jpg)
### SW2 設定
![17](/img/20211123-17.jpg)
### 在 SW1 創建 vlan
![18](/img/20211123-18.jpg)
### SW2 也會出現 vlan ,但要創建 vlan 是不行的
![19](/img/20211123-19.jpg)