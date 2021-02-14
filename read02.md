# welcome to learn web dev

## first we talked about html

1. Headings:

```
<h1> <h2> <h3> <h4> <h5> <h6>

 HTML has six "levels" of headings:
 

<h1> 
is used for main headings

<h2>
is used for subheadings
If there are further sections under the subheadings then the <h3> element is used, and so on...

2. Paragraphs:


<p>
To create a paragraph, surround the words that make up the paragraph with an opening <p> tag and closing </p> tag.

```

![](img/p1.png)

3. Bold & italic:
```
<b>
By enclosing words in the tags <b> and </b> we can make characters appear bold.

<i>
By enclosing words in the tags <i> and </i> we can make characters appear italic.

```

4. superscribt&subscript:

```
<sup>
The <sup> element is used
to contain characters that should be superscript such
as the suffixes of dates or mathematical concepts like raising a number to a power such as 22.

<sub>
The <sub> element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as H20.

```

![](img/p2.png)

5. line Braek & Horizontal rules:

```
<br/>
As you have already seen, the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag <br />.

<hr />
To create a break between themes — such as a change of topic in a book or a new scene
in a play — you can add a horizontal rule between sections using the <hr /> tag.

```

# semantic markup:

There are some text elements that are not intended to affect the structure of your web pages, but they do add extra information to the pages — they are known as semantic markup.

```

In the rest of the chapter you will meet some more elements that will help you when you are adding text to web pages. For example, you are going to meet the <em> element that allows you to indicate where emphasis should be placed on selected words and the <blockquote> element which indicates that a block of text is a quotation.



Browsers often display the contents of these elements in
a different way. For example, the content of the <em> element is shown in italics,
and a <blockquote> is usually indented. But you should not use them to change the way that your text looks; their purpose is to describe the content of your web pages more accurately.


The reason for using these elements is that other programs, such as screen readers or search engines, can use this extra information. For example, the voice of a screen reader may add emphasis to the words inside the <em> element, or a search engine might register that your page features a quote if you use the <blockquote> element.

```

6. strong & emphasis:

```
<strong>
The use of the <strong> element indicates that its content has strong importance.

<em>

The <em> element indicates emphasis that subtly changes the meaning of a sentence.



7. quotaartiiocnles:


<blockquote>

The <blockquote> element is used for longer quotes that take up an entire paragraph. Note how the <p> element is still used inside the <blockquote> element.
Browsers tend to indent the contents of the <blockquote> element, however you should not use this element just to indent a piece of text — rather you should achieve this effect using CSS.

```


