---
title: Asciidoc
date: 2025-09-10 2:30:00
background: bg-[#6319bf]
tags:
  - asc
  - asciidoc
  - Markup
  - text
  - format
categories:
  - Programming
intro: This is a quick reference cheat sheet to the Asciidoc syntax.
plugins:
  - copyCode
  - runCode
---

## Markdown Quick Reference

[Source](https://powerman.name/doc/asciidoc)

### Headers (atx style)

<!-- prettier-ignore -->
```asciidoc
= h1
== h2
=== h3
==== h4
===== h5
====== h6
```

### Headers (setext style)

<!-- prettier-ignore -->
```markdown
Header 1
========

Header 2
--------
```

### Blockquotes


<!-- prettier-ignore -->
```markdown
.Optional Title
----
*Listing* Block

Use: code or file listings
----
```

or

<!-- prettier-ignore -->
```markdown
.Optional Title
[source,perl]
----
# *Source* block
# Use: highlight code listings
# (require `source-highlight` or `pygmentize`)
use DBI;
my $dbh = DBI->connect('...',$u,$p)
    or die "connect: $dbh->errstr";
----
```


or

<!-- prettier-ignore -->
```markdown
.Optional Title
==========================
*Example* Block

Use: examples :)

Default caption "Example:"
can be changed using

 [caption="Custom: "]

before example block.
==========================
```

or

<!-- prettier-ignore -->
```markdown
.Optional Title
[NOTE]
===============================
*NOTE* Block

Use: multi-paragraph notes.
===============================
```

or

<!-- prettier-ignore -->
```markdown
////
*Comment* block

Use: hide comments
////
```

### Unordered List {.row-span-2}

<!-- prettier-ignore -->
```asciidoc
.Bulleted
* bullet
  - bullet
  - bullet
* bullet
** bullet
** bullet
*** bullet
*** bullet
** bullet
* bullet
```

or

```asciidoc
- Item 1
- Item 2
```

or

```asciidoc
* [ ] Checkbox off
* [x] Checkbox on
```

### Ordered List

```asciidoc
a. Item 1
   .. Item 2a  
   .. Item 2b
      1. Test
      . Test2
```

### Links

```markdown
[link](http://google.com)

[link][google]  
[google]: http://google.com

<http://google.com>
```

### Emphasis

<!-- prettier-ignore -->
```markdown
*italic*  
_italic_

**bold**  
__bold__

`inline code`  
~~struck out~~
```

### Horizontal line

Hyphens

<!-- prettier-ignore -->
```markdown
---
```

Asterisks

<!-- prettier-ignore -->
```markdown
***
```

Underscores

<!-- prettier-ignore -->
```markdown
___
```

### Code

````markdown
```javascript
console.log('This is a block code');
```
````

<!-- prettier-ignore -->
```markdown
~~~css
.button {
  border: none;
}
~~~
```

```markdown
    4 space indent makes a code block
```

### Escaped code

Escaped code blocks can be done with more back ticks on the outside or a different symbol.

<!-- prettier-ignore -->
`````markdown
````markdown
```bash
echo hi
```
````

~~~markdown
```bash
echo hi
```
~~~

`````

#### Inline code

```markdown
`Inline code` has back-ticks around it
```

### Tables

```markdown
| Left column | Center column | Right column |
| :---------- | :-----------: | -----------: |
| Cell 1      |   Centered    |        $1600 |
| Cell 2      |    Cell 3     |          $12 |
```

Simple style

<!-- prettier-ignore -->
```markdown
Left column | Center column | Right column
:----------:|:-------------:|:-----------:
   Cell 1   |   Centered    |    $1600
   Cell 2   |    Cell 3     |     $12
```

A markdown table generator: [tableconvert.com](https://tableconvert.com/)

### Images {.col-span-2}

```markdown
![GitHub Logo](/images/logo.png)

![Alt Text](url)
```

#### Image with link

```markdown
[![GitHub Logo](/images/logo.png)](https://github.com/)

[![Alt Text](image_url)](link_url)
```

#### Reference style

```markdown
![alt text][logo]

[logo]: /images/logo.png 'Logo Title'
```

### Backslash escapes

| Characters        | Escape                | Description           |
| ----------------- | --------------------- | :-------------------- |
| <code>\\</code>   | <code>\\\\</code>     | Backslash             |
| <code>\`</code>   | <code>\\\`</code>     | Backtick              |
| <code>\*</code>   | <code>\\\*</code>     | Asterisk              |
| <code>\_</code>   | <code>\\\_</code>     | Underscore            |
| <code>\{\}</code> | <code>\\\{\\\}</code> | Curly braces          |
| <code>\[\]</code> | <code>\\\[\\\]</code> | Square brackets       |
| <code>\(\)</code> | <code>\\\(\\\)</code> | Parentheses           |
| <code>\#</code>   | <code>\\\#</code>     | Hash mark             |
| <code>\+</code>   | <code>\\\+</code>     | Plus sign             |
| <code>\-</code>   | <code>\\\-</code>     | Minus sign \(hyphen\) |
| <code>\.</code>   | <code>\\\.</code>     | Dot                   |
| <code>\!</code>   | <code>\\\!</code>     | Exclamation mark      |

{.show-header}
