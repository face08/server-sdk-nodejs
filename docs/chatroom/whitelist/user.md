## 聊天室用户白名单模块

默认聊天室成员离线 30 秒后或离线后错过 30 条消息，会被踢出聊天室

将用户加入白名单后，用户将处于被保护状态，在以上情况下将不会被踢出聊天室

白名单中用户在当前聊天室中发送消息的级别将高于 `High Level` 

聊天室销毁后，对应白名单也自动销毁

此功能需开通 [专有云服务](http://www.rongcloud.cn/deployment#proprietary-cloud)

### Whitelist.add(chatroom){#add}

将用户添加到白名单中

`chatroom` 参数的**属性说明**：

| 参数   	 |	类型		| 必填	| 说明 							|最低版本		|
| :----------|:--------	|:-----	|:------------------------------|:-------- |
|	id	 	 |	string	|	是	| 聊天室 Id					|3.0.0|
|	members	 |	string	|	是 	| 白名单列表，最多不超过 5 个| 3.0.0|

##### 请求成功

```json
{
    "code": 200
}
```

### Whitelist.remove(chatroom){#remove}

将用户从白名单中移除

`chatroom` 参数的**属性说明**：

| 参数   	 |	类型		| 必填	| 说明 							|最低版本		|
| :----------|:--------	|:-----	|:------------------------------|:-------- |
|	id	 	 |	string	|	是	|	聊天室 Id					|3.0.0|
|	members	 |	string	|	是 	| 移除白名单 Id 列表 | 3.0.0|

##### 请求成功

```json
{
    "code": 200
}
```
### Whitelist.getList(){#getList}

获取聊天室用户白名单

##### 请求成功

```json
{
	"code": 200,
	"members": [{
		"id": "mkij091"
	}]
}
```
| 参数   	 |	类型		| 说明 							|最低版本		|
| :----------|:--------	|:------------------------------|:--------  |
|	members	 |	array	| 白名单列表						|3.0.0		|
 
