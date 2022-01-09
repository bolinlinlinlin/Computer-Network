## 課堂練習
### 架設環境
- ![0928test1](/img/0928test1.jpg)
### 設定Router
```
// R1
Router>enable
Router#conf t
Router(config)#int e0/0
Router(config-if)#ip addr 192.168.1.254 255.255.255.0
Router(config-if)#no shut
Router(config-if)#int e0/1
Router(config-if)#ip addr 192.168.2.254 255.255.255.0
Router(config-if)#no shut
```
### ping 192.168.1.1
- ![0928_ping1](/img/0928_ping1.jpg)
### 看arp快取(顯示路由器的位址解析協議列表)
- ![0928show_arp](/img/0928show_arp.jpg)

### 成功連接
- ![0928test1_result](/img/0928test1_result.jpg)
### 顯示接口配置信息
- ![show_ip_int_brief](/img/show_ip_int_brief.jpg)
## DHCP server 實作
### 資料:
- 參考：[Cisco DHCP Server實做](https://david50.pixnet.net/blog/post/45220440-%5B%E7%AD%86%E8%A8%98%5Dcisco-dhcp-server%E5%AF%A6%E5%81%9A)
### 設置R1
- 建立位址儲備池
```
R1(config-if)#ip dhcp pool mypool1
```
- 指定要分配的IP範圍
```
R1(dhcp-config)#network 192.168.1.0 255.255.255.0
```
- 設定預設閘道
```
R1(dhcp-config)#default-router 192.168.1.254 
```
- 設定DNS
```
R1(dhcp-config)#dns-server 8.8.8.8      
```
- 回到全域模式
```
R1(dhcp-config)#exit        
```
- 指定192.168.1.250 ~ 192.168.1.254不配發
```
R1(config)#ip dhcp excluded-address 192.168.1.250 192.168.1.254
```
### VPC1
- clear ip
- 使用 DHCP

  ![vpc1_dhcp](/img/vpc1_dhcp.jpg)
- show ip

  ![vpc1_showip](/img/vpc1_showip.jpg)
### 同理VPC2
- ping 192.168.1.1
  ![vpc2](/img/vpc2.jpg)
  ![vpc2_ping](/img/vpc2_ping.jpg)

### 新增network
 - ![0928net_type](/img/0928net_type.jpg)
 - ![0928net_type](/img/0928net_type.jpg)
### DHCP R1自動取得ip位址
- ![R1_net_dhcp](/img/R1_net_dhcp.jpg)
- no shut
- show ip int brief
![dhcp_R1_show_ip_int_brief](/img/dhcp_R1_show_ip_int_brief.jpg)    
## Cisco基本指令-啟用SSH
### 資料:
- 參考：[Cisco基本指令-啟用SSH](https://david50.pixnet.net/blog/post/45217866-%5B%E7%AD%86%E8%A8%98%5Dcisco%E5%9F%BA%E6%9C%AC%E6%8C%87%E4%BB%A4-%E5%95%9F%E7%94%A8ssh)