# spacemesh
[Offical](https://docs.spacemesh.io/)  

[config file](https://configs.spacemesh.network/config.mainnet.json)

Windows 设置  
Set-ExecutionPolicy RemoteSigned  
netsh advfirewall firewall add rule name="spacemesh" dir=in protocol=tcp localport=7513,9093,9094,10001 action=allow  

## DIY API (miner reward)
1. 账号管理(钱包地址)
   + 账号新增
   + 账号删除
2. 余额查询
   + 账号余额总和
   + 各个账号余额
3. 奖励时间表
   + 根据账号查询奖励的时间表
   + 根据epoch 查询当前已注册的节点
   + 导入收集的奖励json文件，根据文件导入对应epoch的layer、atx、size,生成schedule
4. EPOCH时间表，CG时间表
   + 获取当前EPOCH信息(epoch、start、end、cg12h)
5. 节点管理(node) GET /nodes/
   + 新增节点(节点的smsher_id是唯一的，不可重复) POST /nodes/
   + 编辑节点 PUT /nodes/{id}
   + 节点是否注册 GET /nodes/{id}

offical public api  
[检查是否注册](https://mainnet-explorer-api.spacemesh.network/smeshers/0x{smesher_id})  
[余额信息](https://mainnet-explorer-api.spacemesh.network/accounts/sm1xxx)   
[奖励是否到账](https://mainnet-explorer-api.spacemesh.network/accounts/sm1xxx/rewards)  
[奖励详情](https://mainnet-explorer-api.spacemesh.network/rewards/65f753f6ef99155cfc20fda8)  
