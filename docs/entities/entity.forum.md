# Entity.Forum

This represents a Ryver forum.

## createDate

The date this forum was created.  
Format: `YYYY-MM-DDThh:mm:ss+0000`

## modifyDate

The date this forum was last edited.  
Format: see [createDate](#createDate)

## name

The name of this forum.

## nickname

The nickname of this forum, used for +mentioning. (optional)

## description

The description of the forum.

## avatar

The avatar of the forum. (optional, see [hasAvatar](#hasAvatar))

## hasAvatar

Whether the forum has an avatar or not.

## identifier

A readable identifier string for the forum. Usage unknown.

## channel

???  
A UID for the forum. Usage unknown.

## jid

???  
Some kind of Ryver-wide UUID which refers to the forum. Usage unknown.  
Format: `<account_name>+<channel>@conference.ryver.com`

## active

Whether the forum is active or archived.

## addNewMembers

???
Usage unknown.

## id

The numerical ID for the forum. This can be used to access specific
forums with `/forums(<id>)/`.

## /forums(<id>)/createUser

???
Add a guest to the forum.

## /forums(<id>)/modifyUser

???
Modify the user's membership of the forum. (member/admin)

## /forums(<id>)/securityGroup

???
Possibly to be used in the future?

## /forums(<id>)/administratorsGroup

???
Get a list of administrators?

## /forums(<id>)/moderatorsGroup

???
Possibly to be used in the future?

## /forums(<id>)/board

???
Probably related to the upcoming Task Management feature.

## /forums(<id>)/members

???
Get a list of members.

## /forums(<id>)/acl

???

## /forums(<id>)/externalLinks

???
