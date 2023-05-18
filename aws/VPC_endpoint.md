## VPC endpoint
- interface endpoint
    - VPC内部にENIを作成して、そのENI経由で他サービスと連携ができる
- gateway endpoint
    - S3,DynamoDBをプライベートに使用できる
    - S3,DynamoDBを利用するサービス側でVPCエンドポイントに対するルートテーブルの設定が必要

## Private Link
利用者と提供者のサービスをインターネットを経由せずにつなげるVPC endpointのまとまりのこと。

利用者側
- VPCエンドポイント作成
提供側
- VPCエンドポイントサービスの作成
    - VPCエンドポイントからの利用を承諾する必要あり

## VPC peering
- VPC同士をくっつけて、インターネットを経由せずにつなげることができる。
- クロスリージョン,クロスアカウントも可能
- CIDRブロックが被ってるとダメ

## Private LinkとVPC peeringは何が違う
- どちらもVPC間のプライベートな通信を行うために使う
- Private Linkは一方通行。peeringは双方向通信

### ユースケース
Private Link
- 取引先の特定のサービスにネットワークを介さずアクセスしたい

VPC peering
- マルチアカウントでのVPCの接続

