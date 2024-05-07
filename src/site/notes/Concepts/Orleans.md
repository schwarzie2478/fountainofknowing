---
{"status":"planted","dg-publish":true,"tags":["concept/SRE/cloud/azure"],"creation_date":"2024-05-05 01:13","definition":"Orleans is a cross-platform framework for building robust, scalable distributed applications.","ms-learn-url":"https://learn.microsoft.com/en-us/dotnet/orleans/","url":"undefined","permalink":"/concepts/orleans/","dgPassFrontmatter":true}
---


| MetaData   |                                              |
| ---------- | -------------------------------------------- |
| Definition | `VIEW[{definition}][text(renderMarkdown)]`   |
| MS Learn   | `VIEW[{ms-learn-url}][text(renderMarkdown)]` |
Orleans scales from a single on-premises server to hundreds to thousands of distributed, highly available applications in the cloud.

Orleans is based on the "[[Concepts/Actor model\|Actor model]]".
Orleans notably invented the _Virtual Actor_ abstraction, wherein actors exist perpetually.


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/concepts/grain/#what-is-a-grain" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What is a grain

The [[Concepts/grain\|grain]] is one of several Orleans primitives.
In terms of the actor model, a grain is a [[Concepts/virtual actor\|virtual actor]].
Grains are entities comprising user-defined identity, behavior, and state.

</div></div>


