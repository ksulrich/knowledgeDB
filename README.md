# knowledgeDB

**Idea:** You have on file (maybe `$HOME/KNOW`), which has this structure:

```
---
Some know how you want to keep.
You can have many lines in one block.
A block is separated with 3 or more dashes `-`, which must begin on the first column.
In your block, you can have any text you like including ------ or other stuff.
---
Clone a git repo:
git clone <git-url>
---
Many more entries, which can be multiple lines.
This contains block, but not xxx.
---
```

Write a tool with name `know`, which reads this file and searches for matching phrases.  
E.g. you can search for `block` AND `know` like this (the order should not matter):

`know block know`

And you should only get the complete text between the 2 `---` lines when all words do match in one block (Optional: allow regular expressions):

```
-------------------------------------------------------------------------------------
Some know how you want to keep.
You can	have many lines	in one block.
A block	is separated with 3 or more dashes `-`,	which must begin on the	first column.
In your block, you can have any text you like including ------ or other stuff.
-------------------------------------------------------------------------------------
```
