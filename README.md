# UnofficialRyverDocs
Welcome to the Unofficial Ryver API Docs!

This project aims to document the Ryver API for developers. This is not
an official Ryver documentation. Unknown entries are marked with a *???*.

Ryver's API is built around the OData.org protocol. You can write
queries for a number of purposes, including getting data about forums
and users. For more information, please see the 
[OData documentation](http://www.odata.org/documentation/).

If you'd like to contribute, feel free to send a PR to the 
[GitHub repo](http://github.com/MD678685/UnofficialRyverDocs/). You can
also [join us on Ryver](http://ryverdocs.ryver.com/application/signup/members/3D1ijKmGWhCmpRO)!

This unofficial documentation was written by MD678685 and is licensed
under the [CC0 license](https://raw.githubusercontent.com/md678685/UnofficialRyverDocs/master/LICENSE) 
(public domain).

## Notes

### Entities

Entities are how OData represents objects on the server.

### URIs

When you see a URI like this: `/forums(<id>)/`, it is relative to 
`<account_name>.ryver.com/api/1/odata.svc/`.

### Placeholders

When you see a format with <>s used as brackets, they are placeholders.
In most cases, they will be properties of the entity and/or will be 
linked to. However, `<account_name>` refers to the name of your Ryver 
account (the part between the *https://* and *.ryver.com*).
