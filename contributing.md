# Contributing to lap.tips
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

## Aliases
You can create aliases for quick access to resources in the `aliases.json` file. These should be created sparingly and should always point to the most up-to-date information that's relevant to the alias URL. For example, `/legion-7` should point to the current year's page for the Lenovo Legion 7.

**Aliases should generally only be used on the root level. Avoid putting more than one slash in your alias.**

This is an example file demonstrating a few aliases. If this format is confusing, please familiarize yourself with the syntax in JSON files.
```json
{
    "/miniled": "/laptops/windows-miniled",
    "/asus": "/laptops/asus/index",
    "/repaste": "/tips/laptops/repasting",
    "/repasting": "/tips/laptops/repasting"
}
```

Each alias can only have one file mapping, but multiple aliases can point to the same file. All aliases must be lowercase as request paths are processed in lowercase.