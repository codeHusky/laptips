# Contributing to user.gripe
There's a few things you need to keep in mind to contribute to this site without causing problems for, well, everyone else!

---

## Folder Structure
We use a pretty simple folder structure. Generally, every folder should have an `index.md` that points people to various pages within the directory.
This is not always needed, but can be very useful.

In general, try to keep everything as generally categorized as possible. If you move a file to a new location, replace the old file with something like this...
```md
## Page Moved
This page has moved to [a new location](/laptops/legion-pro-7i-2023). Please update all references to this page ASAP.
```

These "moved" pages will be removed whenever they're annoying / clutter up a particular directory.

## File Naming
All file names should be in lowercase with alphanumeric characters and these symbols: `-_`. 

Examples of bad file names:
- `legion pro 7i.md` - Spaces are not allowed.
- `Legion-Pro-7i.md` - Capitals are not allowed.
- `legion-pro-7i-(2023).md` - Only `-` and `_` are allowed symbols.

In addition to these rules, your file names must not overlap with a folder name. 

For example, you should not have a `laptops.md` in the same folder as a `laptops/` folder. Instead, you should create a `index.md` within the `laptops/` folder.