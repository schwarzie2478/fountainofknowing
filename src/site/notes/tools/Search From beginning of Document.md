---
{"dg-publish":true,"tags":["tool/vscode/tips"],"creation_date":"2024-05-03 11:31","permalink":"/tools/search-from-beginning-of-document/","dgPassFrontmatter":true}
---

If you need to match the first line of a document the following [[Concepts/regular expression\|regular expression]] will work:
```
^(?<!\n)
```

Explanation:

Using negative lookahead  '?<!'  we tell the parser we don't want to match the beginning of a line if the previous line has an newline at the end.
This effectively only matches the first line of a document
