# AwsAutoBot文档

## 使用教程

### /help
获取命令列表

### /aws_info
获取当前运行情况。包含当前使用账号，当前账号已开服务器信息，剩余账号列表。（注：已失效账号会自动从账号列表中删除，并使用下一个账号开通服务器）

### /aws_add
批量添加aws账号，多个账号用换行符分开，格式如下
```
xxx@xx.xx   (账号邮箱)
AKxxxxxxxxxxxxxx  （账号secretID, 一般为18位AK开头大写字母）
xxxxxxxxxxxxxxxx  （账号secretKey，一般为40位小写字母加下划线或斜杠，也可能为纯字母）

xxx@xx.xx
AKxxxxxxxxxxxxxx
xxxxxxxxxxxxxxxx
```

### /aws_type_get
获取当前设置的实例类型，默认为**c5.xlarge**

### /aws_type_set
设置当前实例类型。具体请参考[Aws EC2实例类型列表](https://aws.amazon.com/cn/ec2/instance-types/)， 请确认您提供的账号可以开通目标实例。

### /aws_set
选中aws账号列表的第一个为默认账号。若当前账号列表为空，执行/aws_add后会默认设置。

### /aws_exec
执行当前默认账号的开机操作。

### /aws_query
查询当前默认账号所开服务器列表。

### /aws_check
查询当前默认账号是否正常。

### /aws_gfw
查询当前默认账号所开服务器是否被墙

### /aws_cip
执行该命令会列出当前账号所开服务器的ip列表，选中某个ip后，会更换该ip所在服务器的ip地址。

### /aws_key_pair
查询当前默认账号所开服务器的ssh密钥。同一账号所有服务器共用同一个ssh密钥，用户名一般为**admin**

### /aws_del
删除当前默认账号

### /aws_clear
清空所有aws账号配置

### /aws_start
开启aws自动任务。若第一次使用，清先添加账号列表，并成功执行/aws_exec命令后再执行此命令。

### /aws_stop
停止aws自动任务



