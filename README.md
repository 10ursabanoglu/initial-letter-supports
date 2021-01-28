# initial-letter-supports

**Description**

Initial letter CSS property allows us to set the style of the initial letters. Unfortunately, only the safari browser supports this feature. In other browsers, the area belonging to this feature is broken and provides a bad view. This code snippet is a protective code block that prevents this bad view in non-working browsers.

### Not Supports

```css
p::first-letter {
  color: #fc5000;
  margin-right: 0.5rem;
  font-weight: bold;

  -webkit-initial-letter: 4;
  initial-letter: 4;
}
```

#### Firefox



## Firefox