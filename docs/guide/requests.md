# Making requests

Making requests is fairly easy. You can retrieve a list of all forums 
with `/forums`, a list of all teams with `/workrooms` and a list of 
all users with `/users`. You can alo use brackets (see 
[formats](#formats)).

## Formats

When retrieving data using the API, the results will be in `d.results`.  
See the 
[OData URI Conventions](http://www.odata.org/documentation/odata-version-2-0/uri-conventions/) 
page for more information. You can narrow results down in a couple of 
ways:

### Queries

You can use OData query strings to filter and sort collections:

* `/forums?$select=name,id,description` will return a collection of 
objects which contain the name, ID and description of each forum, plus 
the forum's metadata.
* `/users?$select=username,id&$orderby=createDate desc&$top=4` will 
return a collection containing the username and ID of the four most 
recently added users.
* `/workrooms?$filter=year(createDate) eq 2016 and month(createDate) eq 07` 
should return a collection containing the teams created in July 2016
according to the OData specifications, but Ryver doesn't implement the
*year* or *minute* functions. **(I may be wrong about this!)**

### Brackets

You can use () brackets to select individual objects:

* `/forums(184392)` will return the forum with the ID of 184392.
* `/workrooms(1743)` will return the team with the ID of 1743.

Note that you can combine these:

* `/forums(1019004)?$select=nickname` will return an object which 
contains *only* the nickname for the room with an ID of 1019004.
* `/users(23875926)?$select=emailAddress,timeZone` will return an 
object which contains *only* the email address and timezone of the 
user with an ID of 23875926.