Markdown
========

[Markdown](http://daringfireball.net/projects/markdown/) is a lightweight markup language created by John Gruber allowing writers to create HTML in a way that is as easy-to-read and easy-to-write as is feasible—it's optimized for readability.

The beauty of Markdown's syntax is you can learn it quickly just by looking at a few examples. And this deck has lots of examples.

## Philosophy

### The Purpose of Markdown's Syntax

*Writing* on the web. The idea for Markdown is to make it easy to read, write, and edit prose.

This is why Markdown only supports a subset of HTML.

### Markdown is optimized for what, above all else?

Readability

### What are Markdown's influences?

John Gruber:

> the single biggest source of inspiration for Markdown’s syntax is the format of plain text email.

Other influences:

- [Setext](http://docutils.sourceforge.net/mirror/setext.html)
- [atx](http://www.aaronsw.com/2002/atx/)
- [Textile](http://textism.com/tools/textile/)
- [reStructuredText](http://docutils.sourceforge.net/rst.html)
- [Grutatext](http://www.triptico.com/software/grutatxt.html)
- [EtText](http://ettext.taint.org/doc/)

### Markdown is composed entirely of...

Puntuation characters.

## Inline HTML

### What is the purpose of Markdown's inline HTML feature?

To use HTML tags in a document that Markdown doesn't support.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

### What are the two restrictions to using inline HTML?

The two restrictions to using inline HTML:

1. block-level HTML elements — e.g. `<div>`, `<table>`, `<pre>`, `<p>`, etc. — must be separated from surrounding content by blank lines
2. the start and end tags of the block should not be indented with tabs or spaces

### Can you use `*emphasis*` inside inline HTML?

No. Markdown is not processed if it's inside block-level HTML elements.

That said, Fletcher Penny's variant [MultiMarkdown](http://fletcherpenney.net/multimarkdown/) supports tables, so you wouldn't have to use HTML, so you could use Markdown inside a table.

## Section Headings

### How do you make an `<h1>`, `<h2>`, `<h3>`, `<h4>`, or `<h5>`?

Use the pound symbol:

    # This is a heading level 1

    ## This is a heading level 2

    ### This is a heading level 3

    #### This is a heading level 4

    ##### This is a heading level 5

Also, you can use underlines for `<h1>` and `<h2>`:

    This is a heading level 1
    =========================

    This is a heading level 2
    -------------------------

Further reading
---------------

Documentation by John Gruber, author of Markdown:

- [Markdown: Main](http://daringfireball.net/projects/markdown/)
- [Markdown: Basics](http://daringfireball.net/projects/markdown/basics)
- [Markdown: Syntax](http://daringfireball.net/projects/markdown/syntax)

[GitHub-flavored Markdown (GFM)](http://github.github.com/github-flavored-markdown/)

Fletcher Penny's [MultiMarkdown](http://fletcherpenney.net/multimarkdown/)