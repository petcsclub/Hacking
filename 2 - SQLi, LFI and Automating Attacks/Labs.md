## Meeting 2: SQLi, LFI and Automating Attacks

## Table of Contents
- [Resources](#resources)
- [Labs](#labs)
  * [Warmup 0: Client-side-again (200 pts)](#warmup-0-client-side-again-200-pts-)
  * ~~[Warmup 1: Irish-Name-Repo 1 (300 pts)](#warmup-1-irish-name-repo-1-300-pts-)~~
  * [Lab 1: Irish-Name-Repo 2 (350 pts)](#lab-1-irish-name-repo-2-350-pts-)
  * ~~[Lab 2: Irish-Name-Repo 3 (400 pts)](#lab-2-irish-name-repo-3-400-pts-)~~
  * [Demo 1: cereal hacker 2 (500 pts)](#demo-1-cereal-hacker-2-500-pts-)
  * [Lab 3: http://lfi.warchall.net/](#lab-3-http-lfiwarchallnet-)
  * [Lab 4: http://rfi.warchall.net/](#lab-4-http-rfiwarchallnet-)


## Resources
1. [Insomnia REST Client](https://insomnia.rest)
2. [Send HTTP Requests Online](https://reqbin.com/)
3. [Online PHP Sandbox](http://sandbox.onlinephpfunctions.com/)
4. [PHP Documentation for include()](https://www.php.net/manual/en/function.include.php)
5. [PHP Documentation for wrappers](https://www.php.net/manual/en/wrappers.php)
6. [CVV #1: Local File Inclusion](https://medium.com/bugbountywriteup/cvv-1-local-file-inclusion-ebc48e0e479a)

## Labs

Some of these problems were taken from the ongoing PicoCTF2019 contest.

### Warmup 0: Client-side-again (200 pts)

**Problem:**

>Can you break into this super secure portal?
https://2019shell1.picoctf.com/problem/32255/ or http://2019shell1.picoctf.com:32255

**Hints:**

1. What is obfuscation?

---

### Warmup 1: Irish-Name-Repo 1 (300 pts)

**Problem:**

>There is a website running at https://2019shell1.picoctf.com/problem/47253/ or http://2019shell1.picoctf.com:47253. Do you think you can log us in? Try to see if you can login!

**Hints:**

1. There doesn't seem to be many ways to interact with this, I wonder if the users are kept in a database?
2. Try to think about how does the website verify your login?

---

### Lab 1: Irish-Name-Repo 2 (350 pts)

**Problem:**

>There is a website running at https://2019shell1.picoctf.com/problem/40968/. Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://2019shell1.picoctf.com:40968

**Hints:**

1. The password is being filtered.

---

### Lab 2: Irish-Name-Repo 3 (400 pts)

**Problem:**

>There is a secure website running at https://2019shell1.picoctf.com/problem/21874/ (link) or http://2019shell1.picoctf.com:21874. Try to see if you can login as admin!

**Hints:**

1. Seems like the password is encrypted.

---

### Demo 1: cereal hacker 2 (500 pts)

**Problem:**

Get the admin's password. https://2019shell1.picoctf.com/problem/62195/ or http://2019shell1.picoctf.com:62195

### Lab 3: http://lfi.warchall.net/

**Problem**

This is not a PicoCTF problem. Can you leak the source code of solution.php?

**Hints:**

1. Try `php://filter/convert.base64-encode/...`

---

### Lab 4: http://rfi.warchall.net/

**Problem**

This is not a PicoCTF problem. Can you get a shell?

**Hints:**

1. Can you gain RCE?
2. Can you find a one-line PHP backdoor? (Use Google!)
