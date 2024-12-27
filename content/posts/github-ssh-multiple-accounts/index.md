---
author: "Evgenii"
title: "Multiple accounts on github"
date: "2024-12-27"
description: "Article describing how to use multiple accounts on github with ssh keys"
tags: ["github", "ssh"]
categories: ["how-to"]
series: [""]
aliases: [""]
cover:
  image: ""
  caption: ""
ShowToc: false
TocOpen: true
---

1. Create `.ssh` folder in your `home` directory and go to it.

2. Generate ssh keys (how many you need) with command 

```properties
ssh-keygen -t ed25519 -C <your_email@example.com>
```
then choose file name. `-C <your_email@example.com>` part seems to be unnecessary. It is just comment.

3. Run ssh-agent in **BASH** with command

```properties
eval "$(ssh-agent -s)"
```

4. Add ssh keys to the ssh agent (not public)

```properties
ssh-add ~/.ssh/<key_name>
```

5. Copy public keys to github accounts.

![regular](/images/IMG_20200501_011326.jpg)
6.  Create `config` file in `.ssh` directory with the following content

```properties
# github <account_name>
Host github.com-<account_name> #
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/<key_name>

# github <account_name>
Host github.com-<account_name>
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/<key_name>
```

The file could contain any number of keys.



6. Clone a repository from github using ssh

```properties
git clone git@github.com-<account_name>:your_username/your_repository.git
```
Example: `git@github.com-eqslab:eqslab/website.git`. Typically, just copy line from github and add `-<account_name>` after `.com`.

More information:

- [video: How to Use Multiple GitHub Accounts on the Same Machine: Boost Your Productivity Today!](https://www.youtube.com/watch?v=lAPcvItvdy0&t)

- [article](https://www.ayyaztech.com/blog/how-to-use-multiple-github-accounts-on-the-same-machine)

- [video: Authenticating on multiple GitHub accounts using SSH](https://www.youtube.com/watch?v=N2hMGEeYR7c&t)

<!--more-->

## Headings

The following HTML `<h1>`—`<h6>` elements represent six levels of section headings. `<h1>` is the highest section level while `<h6>` is the lowest.

# H1

## H2

### H3

#### H4

##### H5

###### H6

## Paragraph

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Blockquotes

The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

#### Blockquote without attribution

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use _Markdown syntax_ within a blockquote.

#### Blockquote with attribution

> Don't communicate by sharing memory, share memory by communicating.
>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Tables

Tables aren't part of the core Markdown spec, but Hugo supports them out-of-the-box.

| Name  | Age |
| ----- | --- |
| Bob   | 27  |
| Alice | 23  |

#### Inline Markdown within tables

| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |

## List Types

#### Ordered List

1. First item
2. Second item
3. Third item

#### Unordered List

- List item
- Another item
- And another item

#### Nested Unordered list

- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese

#### Nested Ordered list

1. Fruit
    - Apple
    - Orange
    - Banana
2. Dairy
    1. Milk
    2. Cheese
3. Third item
    1. Sub One
    2. Sub Two

## Other Elements — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
