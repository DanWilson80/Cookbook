Welcome to the Cookbook wiki! 
======
A list of markdown features
------
This is the basics of using markdown within Github. There is more information available at [GitHub Flavoured Markdown Spec](https://github.github.com/gfm/) and [here in the help files](#https://help.github.com/en/articles/basic-writing-and-formatting-syntax) also [here is an extensive guide](https://www.markdownguide.org/basic-syntax/).  
For extra information on Tables go to [the help files for tables.](https://help.github.com/en/articles/organizing-information-with-tables)

Other useful sources:

[Creating and highlighting code blocks](https://help.github.com/en/articles/creating-and-highlighting-code-blocks)

[Autolinked references and URLs](https://help.github.com/en/articles/autolinked-references-and-urls)

[Working with saved replies](https://help.github.com/en/articles/working-with-saved-replies)

[Guide to Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

Index
------

[Headers](#Headers)

[Emphasis](#Emphasis)

[Styling_Text](#Styling_Text)

[Linebreak](#Linebreak)

[Lists](#Lists)

[Nested_Lists](#Nested_Lists)

[Task_List](#Task_List)

[Links](#Links)

[Images](#Images)

[Blockquotes](#Blockquotes)

[Horizontal_Rule](#Horizontal_Rule)

[Code_and_Syntax_Highlighting](#Code_and_Syntax_Highlighting)

[Tables](#Tables)

[Inline_HTML](#Inline_HTML)

[Using_Emojis](#Using_Emojis)

[Ignoring_Markdown_Formatting](#Ignoring_Markdown_Formatting)

Headers
------
```
# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1
======

Alt-H2
------
```
# H1
## H2
### H3
#### H4
##### H5
###### H6

Alternatively, for H1 and H2, an underline-ish style:

Alt-H1
======

Alt-H2
------
[Index](#Index)

Emphasis
------
```
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
```
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

[Index](#Index)

Styling_Text
------
You can indicate emphasis with bold, italic, or strikethrough text.


| Style                  |    Syntax      |   Example                        |    Output                      |
|:----------------------:|:--------------:|:--------------------------------:|:------------------------------:|
| Bold                   | ** ** or __ __ | \**Bold Text\**                  |**Bold Text**                   |
| Italic                 |   * * or _ _   | \*Italic Text\*                  |*Italic Text*                   |  
| Strikethrough          |    ~~ ~~       | \~~Strikethrough\~~              |~~Strikethrough~~               |  
| Bold and Nested Italic | ** ** and _ _  | \**Is \_extemely\_ important\**  |**This is _extemely_ important**|
| All Bold and Italic    |   *** ***      | \***This is bold and italic\***  |***This is bold and italic***   |

[Index](#Index)

Linebreak
------
To create a `Linebreak` there are several methods that can be used. These are:
```
Hello  <--Double Space at the end of the line
World
```
Hello  
World

```
Hello<--No space = no linebreak even though they are on seperate lines in the code
World
```
Hello
World
```
Hello <br/>
World
```
Hello <br/>
World
```
Hello\ <-- the backslash must be the last character
World
```
Hello\
World
```
Hello
      <----leave a blank line between the two however this leaves a blank line within the markdown also
World
```
Hello

World

[Index](#Index)

Lists
------
```
1. First ordered list item
2. Another item
  * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
4. And another item.  
   
   Some text that should be aligned with the above item.

* Unordered list can use asterisks
- Or minuses
+ Or pluses
```
1. First ordered list item
2. Another item
  * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
4. And another item.  
   
   Some text that should be aligned with the above item.

* Unordered list can use asterisks
- Or minuses
+ Or pluses

[Index](#Index)

Nested_Lists
------
You can create a nested list by indenting one or more list items below another item.

To create a nested list using the web editor on GitHub or a text editor that uses a monospaced font, like Atom, you can align your list visually. Type space characters in front of your nested list item, until the list marker character (- or *) lies directly below the first character of the text in the item above it.

```
1. First list item
    - First nested list item
    - Second nested list item
```
1. First list item
    - First nested list item
    - Second nested list item

1. First list item
    - First nested list item
        - Second nested list item

[Index](#Index)

Task_List
------
To create a task list, preface list items with a regular space character followed by `[ ]`. To mark a task as complete, use `[x]`.

```
- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request
```

- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request

[Index](#Index)

Links
------
There is two way to create links:

```
[I'm an inline-style link](https://www.google.com)

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com
```

[I'm an inline-style link](https://www.google.com)

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

[Index](#Index)

Images
------
```
Here's our logo (hover to see the title text):

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"
```
Here's our logo (hover to see the title text):

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

[Index](#Index)

Blockquotes
------
```
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.

[Index](#Index)

Horizontal_Rule
------
```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores

[Index](#Index)

Code_and_Syntax_Highlighting
------
Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and Markdown Here -- support syntax highlighting. Markdown Here supports highlighting for dozens of languages (and not-really-languages, like diffs and HTTP headers); to see the complete list, and how to write the language names, see the [highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html)

```
Inline `code` has `back-ticks around` it.
```

Inline `code` has `back-ticks around` it.

Blocks of code are either fenced by lines with three back-ticks ```, or are indented with four spaces. I recommend only using the fenced code blocks -- they're easier and only they support syntax highlighting.

```
        ```javascript
        var s = "JavaScript syntax highlighting";
        alert(s);
        ```
 
        ```python
        s = "Python syntax highlighting"
        print s
        ```
 
        ```
        No language indicated, so no syntax highlighting. 
        But let's throw in a <b>tag</b>.
        ```
```

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```
Again, to see what languages are available for highlighting, and how to write those language names, see the [highlight.js demo page.](http://softwaremaniacs.org/media/soft/highlight/test.html)

[Index](#Index)

Tables
------
```
Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

[Index](#Index)

Using_Emojis
------

Using emoji
You can add emoji to your writing by typing `:EMOJICODE:`.

`@octocat :+1: This PR looks great - it's ready to merge! :shipit:`

@octocat :+1: This PR looks great - it's ready to merge! :shipit:

Typing `:` will bring up a list of suggested emoji. The list will filter as you type, so once you find the emoji you're looking for, press Tab or Enter to complete the highlighted result.

For a full list of available emoji and codes, check out [emoji-cheat-sheet.com.](http://emoji-cheat-sheet.com/)

[Index](#Index)

Inline_HTML
------
You can also use raw HTML in your Markdown, and it'll mostly work pretty well.
```
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

[Index](#Index)

Ignoring_Markdown_Formatting
------

You can tell GitHub to ignore (or escape) Markdown formatting by using `\` before the Markdown character.

```
Let's rename \*our-new-project\* to \*our-old-project\*
```

Let's rename \*our-new-project\* to \*our-old-project\*.

[Index](#Index)
