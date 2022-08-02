# terraform_aws_Iac

## 作成するアプリケーション
![MainImage](images/main.png)
![DetailImage](images/main2.png)


## 作成するVPC
### サブネット
作成するサブネットは以下の４つ
* (Pubilc Subnet) 192.168.1.0/24
* (Pubilc Subnet) 192.168.2.0/24
* (Private Subnet) 192.168.3.0/24
* (Private Subnet) 192.168.4.0/24
![subnet](images/subnet.png)

### ルートテーブル
作成するルートテーブルは以下の2つ
* public network
* private network
![routeTable](images/routetable.png)

### 作成するインターネットゲートウェイ
![InternetGateWay](images/internetgateway.png)