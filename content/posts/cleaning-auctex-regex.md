---
date: 2021-12-21T08:00:00+00:00
title: Cleaning LaTeX with AucTex
authors: ["flinner"]
weight: -230
---

Yo emacs boyz how you doin?

# Cleaning (La)Tex intermediate files in emacs
invoke:
```
M-x TeX-clean

```
to clean intermdiate files, and 
```
C-u M-x TeX-clean
```
to clean both intermediate files and outputs.
or 
```
C-c C-c
```
then Choose `Clean` or `Clean All`

# How does it actually work?
1. `TeX-clean` looks into the variable `LaTeX-clean-intermediate-suffixes` for Regexs to search for files to delete when choosing `Clean` or invoking the function `TeX-clean` with no `C-u` prefix.
1. `TeX-clean` looks into the variable `LaTeX-clean-intermediate-suffixes` **AND** `LaTeX-clean-output-suffixes` for Regexs to search for files to delete when choosing `Clean All` or invoking the function `TeX-clean` **WITH** `C-u` prefix.

# Remove other files!
Sadly not all regexes are implemented by default, un-sadly you can easily add them!

```elisp
  ;; clean intermdiate tex crap
  (add-to-list 'LaTeX-clean-intermediate-suffixes '"-figure[0-9]*\\.\\(pdf\\|md5\\|log\\|dpth\\|dep\\|run\\.xml\\)")
  (add-to-list 'LaTeX-clean-intermediate-suffixes '".auxlock")
```

# End

hope it helps! and thanks for checking my glorious blog!

# Shameless keywords for better search engine indexing
- clean \usepgfplotslibrary{external} LaTeX
- clean auctex files
- clean regex to auctex clean
- idk too tired heh




