## 上課問題1 
![1](/img/20211116-1.jpg)

VPC2 如何 ping 成功 VPC3

有兩種解法:

1.解:

更改192.168.4.254/24為192.168.5.254/24,VPC3的內定路由器改為192.168.5.254

2.在不動到ip 192.168.4.254 和 192.168.5.1 的情況下,把兩個ip放到同個網路?

解:超網化  

在VPC3設定 ip 192.168.5.1 255.225.254.0 192.168.4.254
![2](/img/20211116-2.jpg)

同理,在R1設定 ip addr 192.168.4.254 255.255.254.0 

![3](/img/20211116-3.jpg)

### 下載kali linux(https://kali.download/virtual-images/kali-2021.3/kali-linux-2021.3-vmware-amd64.7z)
### 下載DC1 靶機 (https://www.vulnhub.com/entry/dc-1,292/)

- 資料：[Vulnhub靶机实战——DC-1_冠霖L的博客-CSDN博客](https://blog.csdn.net/weixin_43583637/article/details/101542749)

## VLAN主要目的:把一個網路進行細分,提高效能、網路安全性

## 上課練習1
### 環境
![4](/img/20211116-4.jpg)
### show vlan brief
![5](/img/20211116-5.jpg)
### 創建vlan
![6](/img/20211116-6.jpg)
### show vlan brief
![7](/img/20211116-7.jpg)
### 設定access port(與一般pc進行連接):送出的封包不會打上標籤
![8](/img/20211116-8.jpg)

其他接口同理
![9](/img/20211116-9.jpg)
### 同一 vlan 可互 ping ,不同則否
## 上課練習2
### 環境
![10](/img/20211116-10.jpg)
### 同時設定兩個接口,套用同樣設定
![11](/img/20211116-11.jpg)
### access port 封包不會貼上任何標籤
![12](/img/20211116-12.jpg)