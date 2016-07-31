# Chat.PostMessage

Available for [Users](entities/entity.user.md), 
[Forums](entities/entity.forum.md) and [Teams](entities/entity.workroom.md).

**Ryver has [already documented this](https://support.ryver.com/chatmessage-api/).**
It is best to refer to the official docs.

Method: POST

## Headers

```
Content-Type: application/json
Accept: application/json
Authorization: *see below*
```

This should be a Basic Authorization hash using a Ryver user's username
and password.

## Payload

```
{
"body":"**This is an example!**\n> *You* can use **Markdown** [here](https://en.wikipedia.org/wiki/Here).",
  "extras": {
    "from": {
      "__descriptor":"BitBucket",
      "avatarUrl":"https://example/icon.png"
    } 
  }
}
```

**Note:** The `extras.from` properties are optional. If not specified,
the message will appear to have been sent by the 
