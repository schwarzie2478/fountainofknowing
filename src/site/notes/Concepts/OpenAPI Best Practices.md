---
{"status":"planted","dg-publish":true,"tags":["concept/SRE/cloud"],"creation_date":"2024-05-06 16:15","definition":"undefined","ms-learn-url":"undefined","url":"https://learn.openapis.org/best-practices.html","aliases":null,"permalink":"/concepts/open-api-best-practices/","dgPassFrontmatter":true}
---


| MetaData   |                                              |
| ---------- | -------------------------------------------- |
| Definition | `VIEW[{definition}][text(renderMarkdown)]`   |
| Homesite   | `VIEW[{url}][text(renderMarkdown)]`          |
| MS Learn   | `VIEW[{ms-learn-url}][text(renderMarkdown)]` |

- [ ] Review OPENAPI Best Practices
## **Best Practices**

- Use a Design-First Approach. ...
- Keep a Single Source of Truth. ...
- Add OpenAPI Descriptions to Source Control. ...
- Make the [[Concepts/OpenAPI Descriptions\|OpenAPI Descriptions]] Available to the Users. ...
- There is Seldom Need to Write OpenAPI Descriptions by Hand. ...
- Describing Large APIs. ...
	- Links to External Best Practices.

## See also [[unsorted/RESTful web API design\|RESTful web API design]]
- Organize the API design around resources

> [!tip]
> Avoid requiring resource URIs more complex than _collection/item/collection_.

## Get with body discussion
https://stackoverflow.com/questions/978061/http-get-with-request-body

Possible solution for caching issue:

> [!hint] 
> For caching just add hash of body to url