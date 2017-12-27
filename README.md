# forumfmt

[On GitHub](https://github.com/Southclaws/forumfmt)

Maintaining documentation is already difficult, maintaining it on two different platforms in two different formats is just annoying.

This tool means you can simply have a single markdown readme file in your project's repo and when you post it to the forums or update the topic, all you need to do is simply run this tool over the markdown text to generate BBCode.

For example, this:

```markdown
The Swiss Army Knife of SA:MP - vital tools for any server owner or library
maintainer.

## Overview

Server management and configuration tools:

* Manage your server settings in JSON format (compiles to server.cfg)
* Run the server from `sampctl` and let it worry about automatic restarts
* Automatically download Windows/Linux server binaries when you need them
```

becomes this:

The Swiss Army Knife of SA:MP - vital tools for any server owner or library maintainer.

```json
[COLOR="RoyalBlue"][size="6"][B]Overview[/B][/size][/COLOR]

Server management and configuration tools:

[LIST]

[*]Manage your server settings in JSON format (compiles to server.cfg)
[*]Run the server from [FONT="courier new"]sampctl[/FONT] and let it worry about automatic restarts
[*]Automatically download Windows/Linux server binaries when you need them

[/LIST]
```

## Installation and Usage

The app is a simple Go app so just `go get` it:

```bash
go get github.com/Southclaws/forumfmt
```

Then you can use the command, either by passing a file as an argument:

```bash
forumfmt README.md > README.bbcode
```

Or by piping to stdin on Unix platforms:

```bash
cat README.md | forumfmt > README.bbcode
```
