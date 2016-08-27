# Chat.History

Available for [Users](../entities/entity.user.md), 
[Forums](../entities/entity.forum.md) and [Teams](../entities/entity.workroom.md).

Method: GET

## Description

Retrieve the chat history for a user, team or forum.

## Headers

```
Content-Type: application/json
Accept: application/json
Authorization: *see below*
```

This should be a Basic Authorization hash using a Ryver user's username
and password.

## Response

### `d.results`

An array containing the found results. These will be referred to as 
`result`.

#### `result.from` and `result.to`

Information about the sender and recipient. Contains name, entity type, 
id and jid for each.

#### `result.body`

The contents of the message.

#### `result.id`

???  
Most likely a unique ID for the message which can be used to 
[mark messages as read](markasread.md).

#### `result.when`

Timestamp for when the message was sent.

#### `result.modifyDate`

Timestamp for when the message was last edited.

#### `result.messageType`

???  
The type of content this is? This might be worth investigating to see 
if embeds and post notifications have a different value here, as well as 
whether user-to-user messages have a different value.
