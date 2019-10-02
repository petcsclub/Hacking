## Meeting 1: Introduction to Web Exploitation
---

These problems were taken from the ongoing PicoCTF2019 contest.

### Warm up: Insp3ct0r (50 pts)

**Problem:**

>Kishor Balan tipped us off that the following code may need inspection:
https://2019shell1.picoctf.com/problem/28717/ or http://2019shell1.picoctf.com:28717

**Hints:**
1. How do you inspect web code on a browser?
2. There's 3 parts

### Lab 1: dont-use-client-side (100 pts)

**Problem:**

>Can you break into this super secure portal?
https://2019shell1.picoctf.com/problem/49886/ or http://2019shell1.picoctf.com:49886

**Hints:**

1. Never trust the client

### Lab 2: Client-side-again (200 pts)

**Problem:**

>Can you break into this super secure portal?
https://2019shell1.picoctf.com/problem/32255/ or http://2019shell1.picoctf.com:32255

**Hints:**

1. What is obfuscation?

### Lab 3: logon (100 pts)

**Problem:**

>The factory is hiding things from all of its users. Can you login as logon and find what they've been looking at? https://2019shell1.picoctf.com/problem/47307/ or http://2019shell1.picoctf.com:47307

**Hints:**

1. Hmm it doesn't seem to check anyone's password, except for {{name}}'s?

### Lab 4: Open-to-admins (200 pts)

**Problem:**

>This secure website allows users to access the flag only if they are admin and if the time is exactly 1400.
https://2019shell1.picoctf.com/problem/49858/ or http://2019shell1.picoctf.com:49858

**Hints:**

1. Can cookies help you to get the flag?

### Lab 5: Irish-Name-Repo 1 (300 pts)

**Problem:**

>There is a website running at https://2019shell1.picoctf.com/problem/47253/ or http://2019shell1.picoctf.com:47253. Do you think you can log us in? Try to see if you can login!

**Hints:**

1. There doesn't seem to be many ways to interact with this, I wonder if the users are kept in a database?
2. Try to think about how does the website verify your login?

### Lab 6: Irish-Name-Repo 2 (350 pts)

**Problem:**

>There is a website running at https://2019shell1.picoctf.com/problem/40968/. Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://2019shell1.picoctf.com:40968

**Hints:**

1. The password is being filtered.


### Lab 7: Irish-Name-Repo 3 (400 pts)

**Problem:**

>There is a secure website running at https://2019shell1.picoctf.com/problem/21874/ (link) or http://2019shell1.picoctf.com:21874. Try to see if you can login as admin!

**Hints:**

1. Seems like the password is encrypted.

### Lab 8: JaWT Scratchpad (400 pts, but imo should be 700)

**Problem:**

>Check the admin scratchpad! https://2019shell1.picoctf.com/problem/12283/ or http://2019shell1.picoctf.com:12283

**Hints:**

1. What is that cookie?
2. Have you heard of JWT?
