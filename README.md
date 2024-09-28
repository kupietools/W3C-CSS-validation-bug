# W3C-CSS-validation-bug
A small example of the W3C CSS validator reporting invalid CSS code as valid.

The W3C CSS validator at [https://jigsaw.w3.org/css-validator/](https://jigsaw.w3.org/css-validator/) reports following CSS as validating correctly:

```
b {text-decoration: underline solid black;}
/* .disabled-attribute{display: block;} */   %
!
)
/* .another > .disabled > .attribute {box-shadow: 10px 10px 20px RGBA(255,255,255,0);border: 1px solid hsla(0,0%,100%,.2) !important;} */

span.greentext {color: green;} 
```

Instead of reporting the error when it encounters the invalid characters, it simply stops validating and reports that the CSS is valid.

I've put together a working example of this at [https://github.com/kupietools/W3C-CSS-validation-bug](https://github.com/kupietools/W3C-CSS-validation-bug).
