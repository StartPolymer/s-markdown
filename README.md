
<!---

This README is automatically generated from the comments in these files:
s-markdown.html

Edit those files, and our readme bot will duplicate them over here!
Edit this file, and the bot will squash your changes :)

The bot does some handling of markdown. Please file a bug if it does the wrong
thing! https://github.com/PolymerLabs/tedium/issues

-->

##&lt;s-markdown&gt;

Ultra fast regex-based Markdown parser.

Inspired by [&lt;marked-element&gt;](https://github.com/PolymerElements/marked-element) and [Slimdown](https://gist.github.com/jbroadway/2836900).

`<s-markdown>` accepts Markdown source, and renders it to a child
element with the class `markdown-html`. This child element can be styled
as you would a normal DOM element. If you do not provide a child element
with the `markdown-html` class, the Markdown source will still be rendered,
but to a shadow DOM child that cannot be styled.

The Markdown source can be specified either via the `markdown` attribute:

```html
<s-markdown markdown="`Markdown` is _awesome_!" rules="code em">
  <div class="markdown-html"></div>
</s-markdown>
```

Or, you can provide it via a `<script type="text/markdown">` element child:

```html
<s-markdown rules="a blockquote code del em-strong h hr img ol q ul p">
  <div class="markdown-html"></div>
  <script type="text/markdown">
    ## This is an h2 tag
    ### This is an h3 tag

    ---

    `<div class="title">Title</div>`

    **bold text**

    ~~Scratch this.~~

    :"Quote text":

    > blockquote

    - item 1
    - item 2
    - item 3

    1. item 1
    2. item 2
    3. item 3

    [Polymer](https://www.polymer-project.org)

    ![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)
  </script>
</s-markdown>
```

Note that the `<script type="text/markdown">` approach is *static*. Changes to
the script content will *not* update the rendered markdown!

### Styling

If you are using a child with the `markdown-html` class, you can style it
as you would a regular DOM element:

```css
.markdown-html p {
  color: red;
}

.markdown-html td:first-child {
  padding-left: 24px;
}
```
