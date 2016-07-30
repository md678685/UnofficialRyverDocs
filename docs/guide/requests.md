# Making requests

Making requests is fairly easy. You can retrieve a list of all forums 
with `/forums`, a list of all teams with `/workrooms` and a list of 
all users with `/users`. You can alo use brackets (see 
[formats](#formats)).

## Formats

When simply listing data with `/forums`, `/workrooms`, or `/users`, 
`d.results` will be an array (assuming you are requesting JSON) which
contains all of the returned results. You can narrow these results 
down in a couple of ways:

### Queries

You can append `?$` to filter your results using a somewhat SQL-like
syntax:

* `/forums?$select=name,id,description` will return an array of 
objects containing the name, ID and description of all of the forums, 
plus metadata.

### Brackets

You can use () brackets to select individual objects:

* `/forums(184392)` will return an object which represents the forum 
with the ID of 184392.
* `/teams(173)` will return an object which represent the team with 
ID of 173.

Note that you can combine these:

* `/forums(1019004)?$select=nickname` will return an object which 
contains *only* the nickname for the room with an ID of 1019004.
* `/users(23875926)?$select=emailAddress,timeZone` will return an 
object which contains *only* the email address and timezone of the 
user with an ID of 23875926.