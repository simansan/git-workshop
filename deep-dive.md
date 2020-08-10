# GIT Deep Dive

The GIT deep dive talk will showcase and cover the inner workings of GIT, in order to create a better understanding. In turn this should lead to more confidence in using GIT, both from the standpoint of using its tools as well as using it from the command line.

> Presentation note: for the full effect it is recommended to have multiple terminals open, one where the actual demo is held. Plus some which show additional data on the repository (using a watcher). Examples are, git status, filesystem, git log.

## Outline

### Setup

The setup is quick and simple, create a new 'deep-dive' directory and git init in here. Let the audience know that git repos can be nested, the first parent directory containing a `.git` dir will be used to determine which repo you are in.

    rm -rf deep-dive && \
    mkdir $_ && \
    cd $_ && \
    git init

At this point one might show proof of the existence of the `.git` directory.

### Commits are immutable

_Concept: Make a commit, show what it is, ammend it, show the new commit is not the old commit._

### Reflog

_Concept: Show the old commit still exists_

### Refs

_Concept: move the HEAD to the old commit, create a branch_

> Maybe show the reflog again?

### Squashing and cherry-picking

_Concept: show how to rewrite history_


### Change sets

_Concept: how do change sets work? Create A, Create B, Create C. Go back to A, cherry-pick C. There's now A and C without B. Add content to A; make a patch from the change; undo; Commit different content to A. Revert A to earlier commit, commit this revert. Apply patch, should work as intended as change can be applied.

