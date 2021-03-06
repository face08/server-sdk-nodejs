## 历史消息模块

### History.get(message){#get}

按小时获取历史消息日志文件 URL，包含小时内应用产生的所有消息，消息日志文件无论是否已下载，3 天后将从融云服务器删除

消息日志文件按 `小时` 生成，例如: 获取 10 - 11 点的消息， 11 点后生成

`message` 参数的**属性说明**:

| 参数   	 		|	类型		| 必填	| 说明 							|最低版本	|
| :----------------	|:--------	|:-----	|:------------------------------|:----- |
| date		  		| string 	| 	是 	| 精确到小时，例如: `2018030210` 表示获取 2018 年 3 月 2 日 10 点至 11 点产生的数据 	| 3.0.0 |

##### 请求成功

```json
{
	"code": 200,
	"url": "http://120.92.22.186/9/2018030119/5e398bf3-df16-4e75-9385-7e37c65db649.zip"
}
```

### History.remove(message){#remove}

删除历史消息日志文件

`message` 参数的**属性说明**:

| 参数   	 		|	类型		| 必填	| 说明 							|最低版本	|
| :----------------	|:--------	|:-----	|:------------------------------|:----- |
| date		  		| string 	| 	是 	| 精确到小时，例如: `2018030210` 表示删除 2018 年 3 月 2 日 10 点至 11 点产生的数据文件 | 3.0.0 |

##### 请求成功

```json
{
	"code": 200
}
```