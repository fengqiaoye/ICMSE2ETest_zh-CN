# <a name="event-snoozereminder"></a>事件︰ snoozeReminder

直到新时间推迟提醒。

## <a name="prerequisites"></a>先决条件
需执行此 API 之一以下**范围**︰ *Calendars.ReadWrite*
## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/<id>/snoozeReminder
POST /users/<id | userPrincipalName>/events/<id>/snoozeReminder
POST /groups/<id>/events/<id>/snoozeReminder

POST /me/calendar/events/<id>/snoozeReminder
POST /users/<id | userPrincipalName>/calendar/events/<id>/snoozeReminder
POST /groups/<id>/calendar/events/<id>/snoozeReminder

POST /me/calendars/<id>/events/<id>/snoozeReminder
POST /users/<id | userPrincipalName>/calendars/<id>/events/<id>/snoozeReminder

POST /me/calendargroup/calendars/<id>/events/<id>/snoozeReminder
POST /users/<id | userPrincipalName>/calendargroup/calendars/<id>/events/<id>/snoozeReminder

POST /me/calendargroups/<id>/calendars/<id>/events/<id>/snoozeReminder
POST /users/<id | userPrincipalName>/calendargroups/<id>/calendars/<id>/events/<id>/snoozeReminder
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
|newReminderTime|DateTimeTimeZone|新的日期和时间触发提醒。|

## <a name="response"></a>响应
如果成功，此方法返回`200, OK`响应代码。 它不返回任何响应正文中。

## <a name="example"></a>示例
这里是如何调用此 API 的示例。
##### <a name="request"></a>请求
下面是示例请求。
<!-- {
  "blockType": "request",
  "name": "event_snoozereminder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/<id>/snoozeReminder
Content-type: application/json
Content-length: 97

{
  "newReminderTime": {
    "dateTime": "dateTime-value",
    "timeZone": "timeZone-value"
  }
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
  "description": "event: snoozeReminder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
