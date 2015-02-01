This is a collection of ideas and proposals that are to rough or to early to be made into an issue.

## Idea: Log windows rewrite

There are several short comings with the current log view, amongst others performance on large amounts of lines and hard to extend.

### Proposal 1: Use the model/view framework and proxys

A base model contains all lines and handles caching, lines far away are saved on disk or similar. We then have different proxy models for things like searching, coloring, highlighting etc.

## Idea: Make more use of the log

It would be nice to be able to extract more information from the log and display it to the user. Things like incompatible mod versions or ID conflicts should be parsed.

## Patches: extract library from installer

Many "mods" are distributed as an installer that contains the actual library. Many automatically extract it, if some info is given in the JSON?