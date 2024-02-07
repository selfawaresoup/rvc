# RVC

*(ReVision Control)*

A very simplified interface for Git repositories that don't require a "proper" commit history.

It's for use cases, where you just want a version history and the ability to get an answer to the question "What did I even do last week?". It was designed to be used for writing, not coding.

By default, it won't even add meaningful commit messages.

## Installation

Requirements: Ruby and Bundler <https://bundler.io>

1. Download the `rvc` script
1. put it somewhere in your `$PATH`
1. make it executable

## Usage

```sh
rvc help
```

A typical workflow could be:

```sh
rvc init

# make some changes

rvc save --all # will commit all changes and untracked files

# make some more changes

rvc status # show a simplified version of `git status`

rvc save # only commits tracked files

rvc clean # deletes untracked files

# make even more changes

rvc revert # roll back to most recent commit
```

## "Git things" it won't do

- branching
- remotes
- rebasing
- …

… and all that other stuff that Git can do.

But it's still a Git repository underneath, so use Git when you need to.