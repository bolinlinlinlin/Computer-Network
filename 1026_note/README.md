## 課堂練習1
### RIP環境
![1026test1](/img/1026test1.jpg)
- R1 show ip route

![ip_route_test1](/img/ip_route_test1.jpg)
### 模擬R1 e0/1斷線
- R1(config-if)#shut
- R1(config-if)#do ping 2.2.2.2 source 1.1.1.1 repeat 100000
![1026wait_rip](/img/1026wait_rip.jpg)
可能需要2~3分鐘才會連線
### 使用EIGRP較快
### 設置
![1026eigrp](/img/1026eigrp.jpg)
- 模擬斷線(收斂速度較快)

![1026wait_rip](/img/1026wait_rip.jpg)
## 課堂練習2
### 環境
![1026test2](/img/1026test2.jpg)
- 四條路由條目
![1026R2](/img/1026R2.jpg)
### 手工匯整 合併(在出去廣播的介面做)
![1026summary-address](/img/1026summary-address.jpg)
### 結果
![1026summary-address_result](/img/1026summary-address_result.jpg)
## Authentication
- 資料：[RIP 路由信息協定 - Jan Ho 的網絡世界](https://www.jannet.hk/routing-information-protocol-rip-zh-hant/#Authentication)
