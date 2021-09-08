# Using Markdown

Dicecloud uses a system called [Markdown](https://en.wikipedia.org/wiki/Markdown) in most of its text fields \(summaries, descriptions, etc.\). Markdown lets you add formatting like **bold**, _italic_, and more to your text, to keep your features looking fresh. Note that these examples will look slightly different when used on Dicecloud, but will work more or less the same way.

{% hint style="info" %}
Keep in mind that many things in Markdown are picky about line spacing. If something isn't working properly, try putting an empty line between it and whatever is directly above/below it.
{% endhint %}

## Inline Formatting

| Formatting | Syntax |
| :--- | :--- |
| _italic_ | `*italic*` |
| **bold** | `**bold**` |
| `code` | ```code``` |
| [link](https://example.com) | `[link](https://example.com)` |
| ~~strikethrough~~ | `~~strikethrough~~` |

## Dicecloud Formulas

While Markdown is used in many places across the internet, Dicecloud adds a special feature in _formulas_; essentially, the ability to write math expressions in between curly brackets `{}` and have Dicecloud calculate it for you, using variables and functions the same way as you would when building automation functions using Dicecloud's property tree. You can see the [Parser Documentation](creating-a-library/parser-documentation.md) for more details on what all can be used in a formula.

```text
You can use this feature {barbarian.level+2} times, after which you must
complete a long rest before you can use it again.
```

## Advanced Syntax

### Headings

```text
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

### Ordered Lists

```text
1. First item
2. Second item
3. Third item
```

1. FIrst item
2. Second item
3. Third item

### Unordered Lists

```text
- First item
- Second item
- Third item
```

* First item
* Second item
* Third item

### Code Blocks

```text
`‌``

{ "firstName": "John", "lastName": "Smith", "age": 25 }

`‌``
```

```text
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

### Tables

```text
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
```

| Syntax | Description |
| :--- | :--- |
| Header | Title |
| Paragraph | Text |

### Horizontal Rules

```text
---
```

### Images

```text
![alt text](https://commons.wikimedia.org/wiki/File:Transgender_Pride_flag.svg)
```

![alt text](.gitbook/assets/image_2021-02-04_221924.png)

### HTML

Advanced users can write HTML directly in Markdown fields to do much more complex things than Dicecloud's Markdown syntax normally allows; keep in mind, though, that certain elements \(like scripts, CSS styles, etc.\) will be stripped from your HTML before it is rendered.

