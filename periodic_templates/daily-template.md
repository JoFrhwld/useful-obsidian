#daily

weekly:: [[Weekly/<% moment(fileDate).format("YYYY-[W]WW") %>|Weekly Note]]

## Requirements

### Requires:

- [ ] [Templater](https://silentvoid13.github.io/Templater/), with folder templates enabled, and triggering templater on file creation
- [ ] [DataView](https://blacksmithgu.github.io/obsidian-dataview/)

### Useful:

- [ ] [Periodic Notes](https://github.com/liamcain/obsidian-periodic-notes)

### Goes with

- The [weekly template](weekly-template.md)

## Description 

I include a link to the weekly note for each day, not just for handy navigation, but to also leverage the inlinks shorthand from dataview. For things I did in a day that I want to be summarized in the weekly note, I specifiy it with a `d:: ` inline metadata field.

## Did

- d:: Added my periodic templates to github

