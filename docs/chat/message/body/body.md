# 消息主体Message body

## 示例

```json
{
    "metadata": {
        "id": "b20cefb5-e14e-49f7-b95d-9ef69a200da7",
        "contentType": "text/plain",
        "lang":"en",
        "sendAt": "2024-06-01T12:00:00Z",
        "sender": {
            "id": "2minRain",
            "nickname": "Rylin"
        },
        "editedAt": null
    },
    "content": {
        "text": "This is a plain text message body."
    }
}
```

## 结构

消息主体分为两个部分, `metadata`与 `content`

### metadata

消息的元数据.

#### id

`必须`

id为一个uuidv4规范的字符串, 与数据库索引中的id应相同.

#### contentType

`非必须`

内容类型, 由服务端识别并将消息交由相应的消息预处理器 `message-processor`处理, 返回的 `metadata`中新增 `viewType`字段, 指定显示消息要使用的视图.

若不填写, 默认使用`text/plain`类型

#### lang

`非必须`

消息使用的语言.

#### sendAt

`必须`
