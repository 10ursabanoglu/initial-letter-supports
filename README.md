# initial-letter-supports

**Description**

Initial letter CSS property allows us to set the style of the initial letters. Unfortunately, only the safari browser supports this feature. In other browsers, the area belonging to this feature is broken and provides a bad view. This code snippet is a protective code block that prevents this bad view in non-working browsers.

```css
p::first-letter {
  color: #fc5000;
  margin-right: 0.5rem;
  font-weight: bold;

  -webkit-initial-letter: 4;
  initial-letter: 4;
}
```

What we want to do here is to define the style for the first letter of the paragraph.

## Safari
![Safari](browsers/Safari.png?raw=true)

Works perfectly smoothly.

Now let's try it in firefox.

![Firefox-no-supports](browsers/firefox-no-supports.png?raw=true)


Here we need to write the following support query to prevent bug appearance in browsers such as firefox and chrome.

```css
@supports (initial-letter: 4) or (-webkit-initial-letter: 4) {
  p::first-letter {
    color: #fc5000;
    margin-right: 0.5rem;

    -webkit-initial-letter: 4;
    initial-letter: 4;
  }
}
```

![Firefox-supports](browsers/firefox-supports.png?raw=true)

Yes it works.





In the meantime, if you want to reach the current browser support, you can reach it from the link below.

https://caniuse.com/?search=initial-letter


Also, if you want to examine the initial-letter feature in more detail, you can find it in the link below.

https://developer.mozilla.org/en-US/docs/Web/CSS/initial-letter
