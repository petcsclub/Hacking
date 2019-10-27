## Problem Statement


### Insp3ct0r (50 pts)

**Problem:**

>Kishor Balan tipped us off that the following code may need inspection:
https://2019shell1.picoctf.com/problem/28717/ or http://2019shell1.picoctf.com:28717

**Hints:**
1. How do you inspect web code on a browser?
2. There's 3 parts

## Write-Up


Using "View Page Source," we can locate all three parts of the flag.

The first part of the flag is located at the bottom of the page.
The second part is located in the `mycss.css` stylesheet file (click the blue hyperlink) and the third part is located at the bottom of the `myjs.js` javascript file.

```html
<link rel="stylesheet" type="text/css" href="mycss.css">
<script type="application/javascript" src="myjs.js"></script>
```
