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

## 作成するセキュリティグループ

作成するセキュリティグループは以下の４つ

* Webサーバー用  
  → http/httpsが入ってくる  
  ← TCP3000（アプリケーションサーバー）が出ていく
* APサーバー用  
  → TCP3000が入ってくる  
  ← http/httpsがS3に出ていく  
  ← Mysql向けポート(TCP3306)に出ていく  
*  DBサーバー用  
  → Mysql向けポート(TCP3306)が入ってくる
* 運用管理用  
  → SSHが入ってくる  
  → TCP3000が入ってくる  
  ← HTTP/HTTPSが出ていく

  ![SGImage](images/sg.png)

### プレフィックスリスト
  S3向けのプレフィックスリストを取得

  ![PlefixImage](images/plefix.png)

## 作成するRDS
![RDSImage](images/rds.png)