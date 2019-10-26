## Meeting 1: Introduction to Web Exploitation
---

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Labs](#labs)
  * [Warmup 0: Insp3ct0r (50 pts)](#warmup-0-insp3ct0r-50-pts)
  * [Lab 1: dont-use-client-side (100 pts)](#lab-1--dont-use-client-side-100-pts)
  * [Lab 2: logon (100 pts)](#lab-2-logon-100-pts)
  * [Lab 3: Open-to-admins (200 pts)](#lab-3-open-to-admins-200-pts)
  * [Lab 4: Irish-Name-Repo 1 (300 pts)](#lab-4-irish-name-repo-1-300-pts)
  * [Lab 5: JaWT Scratchpad (400 pts, but imo should be 700)](#lab-5-jawt-scratchpad-400-pts-but-imo-should-be-700)

## Labs

These problems were taken from the ongoing PicoCTF2019 contest.

### Warmup 0: Insp3ct0r (50 pts)

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

### Lab 2: logon (100 pts)

**Problem:**

>The factory is hiding things from all of its users. Can you login as logon and find what they've been looking at? https://2019shell1.picoctf.com/problem/47307/ or http://2019shell1.picoctf.com:47307

**Hints:**

1. Hmm it doesn't seem to check anyone's password, except for {{name}}'s?

### Lab 3: Open-to-admins (200 pts)

**Problem:**

>This secure website allows users to access the flag only if they are admin and if the time is exactly 1400.
https://2019shell1.picoctf.com/problem/49858/ or http://2019shell1.picoctf.com:49858

**Hints:**

1. Can cookies help you to get the flag?

### Lab 4: Irish-Name-Repo 1 (300 pts)

**Problem:**

>There is a website running at https://2019shell1.picoctf.com/problem/47253/ or http://2019shell1.picoctf.com:47253. Do you think you can log us in? Try to see if you can login!

**Hints:**

1. There doesn't seem to be many ways to interact with this, I wonder if the users are kept in a database?
2. Try to think about how does the website verify your login?

### Lab 5: JaWT Scratchpad (400 pts, but imo should be 700)

**Problem:**

>Check the admin scratchpad! https://2019shell1.picoctf.com/problem/12283/ or http://2019shell1.picoctf.com:12283

**Hints:**

1. What is that cookie?
2. Have you heard of JWT?
