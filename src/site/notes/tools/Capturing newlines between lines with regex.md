---
{"status":"planted","dg-publish":true,"tags":["tool/vscode"],"creation_date":"2024-05-07 13:00","definition":"undefined","ms-learn-url":"undefined","url":"undefined","aliases":null,"permalink":"/tools/capturing-newlines-between-lines-with-regex/","dgPassFrontmatter":true}
---


| MetaData   |                                              |
| ---------- | -------------------------------------------- |
| Definition | `VIEW[{definition}][text(renderMarkdown)]`   |
| Homesite   | `VIEW[{url}][text(renderMarkdown)]`          |
| MS Learn   | `VIEW[{ms-learn-url}][text(renderMarkdown)]` |

Example of [[Concepts/Regular Expression\|Regular Expression]] 
Regex Tester: https://regex101.com/r/vPo9Cs/1

Input:
```
- Create and manage container images for solutions

- Publish an image to Azure Container Registry
```
Regex:
```
(- .*\n)\s*(?=\n-)
```

Replace 
```
$1
```

Expected result
```
- Create and manage container images for solutions
- Publish an image to Azure Container Registry
```

Actual Result
```
$1
```

VS Code uses ripgrep ( or Rust Regular Expressions)
