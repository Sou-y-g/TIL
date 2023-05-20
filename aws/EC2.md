### InsufficientInstanceCapacity error
region,AZで特定のEC2インスタンスの需要量が供給量を上回った場合に発生します
回避方法
- 別のregion,AZを試す
- 別のインスタンスタイプを選ぶ

### 停止
EC2を停止して再起動すると、物理的に別のコンピュータでEC2が起動する(100%ではない)
Personal Health checkでAWSの物理リソースに問題があった際に使えるかも？
