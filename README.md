你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# forumfmt

[![https://img.shields.io/badge/star_on-GitHub-lightgrey.svg](https://img.shields.io/badge/star_on-GitHub-lightgrey.svg)](https://github.com/Southclaws/forumfmt)

Maintaining documentation is already difficult, maintaining it on two different platforms in two different formats is just annoying.

## Overview

This tool means you can simply have a single markdown readme file in your project's repo and when you post it to the forums or update the topic, all you need to do is simply run this tool over the markdown text to generate BBCode.

For example, this:

```markdown
The Swiss Army Knife of SA:MP - vital tools for any server owner or library maintainer.

## Overview

Server management and configuration tools:

* Manage your server settings in JSON format (compiles to server.cfg)
* Run the server from `sampctl` and let it worry about automatic restarts
* Automatically download Windows/Linux server binaries when you need them
```

becomes this:

```json
The Swiss Army Knife of SA:MP - vital tools for any server owner or library maintainer.

[COLOR="RoyalBlue"][size="6"][B]Overview[/B][/size][/COLOR]

Server management and configuration tools:

[LIST]

[*]Manage your server settings in JSON format (compiles to server.cfg)

[*]Run the server from [FONT="courier new"]sampctl[/FONT] and let it worry about automatic restarts

[*]Automatically download Windows/Linux server binaries when you need them

[/LIST]
```

And, as you can probably guess by now, this topic was generated using the tool!

## Installation

The app is a simple Go app so just `go get` it:

```bash
go get github.com/Southclaws/forumfmt
```

If you don't have Go installed, there are precompiled binaries available [on the releases page](https://github.com/Southclaws/forumfmt/releases).

## Usage

Then you can use the command, either by passing a file as an argument:

```bash
forumfmt README.md > README.bbcode
```

Or by piping to stdin on Unix platforms:

```bash
cat README.md | forumfmt > README.bbcode
```
