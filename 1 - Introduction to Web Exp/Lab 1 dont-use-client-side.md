## Problem Statement
---

**Problem:**

>Can you break into this super secure portal?
https://2019shell1.picoctf.com/problem/49886/ or http://2019shell1.picoctf.com:49886

**Hints:**

1. Never trust the client

## Write-Up
---

Locating this chunk of the code:

```js
if (checkpass.substring(0, split) == 'pico') {
  if (checkpass.substring(split*6, split*7) == 'e2f2') {
    if (checkpass.substring(split, split*2) == 'CTF{') {
     if (checkpass.substring(split*4, split*5) == 'ts_p') {
      if (checkpass.substring(split*3, split*4) == 'lien') {
        if (checkpass.substring(split*5, split*6) == 'lz_e'){
          if (checkpass.substring(split*2, split*3) =='no_c') {
            if (checkpass.substring(split*7, split*8) == '4') {
```

We can deduce the probable order of the flag through the number multiplied by `split`. For instance, the piece associated with `split` goes before `split*2` which goes before `split*3` etc... Note that the fragments of the flag is surrounded by single quotes i.e., `'some text'`.

To learn more about Javascript, I've included a link to a cheat sheet:
https://htmlcheatsheet.com/js/
