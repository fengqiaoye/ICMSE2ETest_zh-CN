# <a name="message-replyall"></a>消息︰ 全部答复

答复邮件的所有收件人。 然后在已发送邮件文件夹中保存邮件。

## <a name="prerequisites"></a>先决条件
需执行此 API 之一以下**范围**︰ *Mail.Send*
## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /users/me/messages/<id>/replyAll
POST /users/<id | userPrincipalName>/messages/<id>/replyAll
POST /me/mailFolders/<id>/messages/<id>/replyAll
POST /users/<id | userPrincipalName>/mailFolders/<id>/messages/<id>/replyAll
```
## <a name="request-headers"></a>请求标头
| 名称       | 类型 | 说明|
|:---------------|:--------|:----------|
| 授权  | string  | 持有者<token>。 必需。 |
| 内容类型 | string  | 正文中的实体数据的性质。 必需。 |

## <a name="request-body"></a>请求正文
在请求正文中，使用以下参数中提供的 JSON 对象。

| 参数    | 类型   |说明|
|:---------------|:--------|:----------|
|批注|String|要包含的注释。 可以为空字符串。|

## <a name="response"></a>响应
如果成功，此方法返回`202, Accepted`响应代码。 它不返回任何响应正文中。

## <a name="example"></a>示例
这里是如何调用此 API 的示例。
##### <a name="request"></a>请求
下面是示例请求。
<!-- {
  "blockType": "request",
  "name": "message_replyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/<id>/replyAll
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```


##### <a name="response"></a>响应
这里是响应的示例。
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: replyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
