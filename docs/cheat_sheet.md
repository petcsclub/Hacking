title: Cheat Sheet

# Cheat Sheet

## What is this for?
This is a rough guideline to help you identify the vulnerabilities in a web application. When attacking a website, consider the questions being asked and follow the steps to an easy pwn! This guide will be updated before each meeting.

## What was that acronym?
Sometimes we're too lazy to type out the full word, so I've compiled a nice list of acronyms for you to look up. Sometimes we use fancy jargon that no one understands.  
**[Click here for an amazing list](#jargon-decoder).**

## Yes, but what exactly is this thing? *Think R.E.E.!*

3 easy steps to weight loss! Just kidding. These are what I believe to be the 3 steps in approaching and performing a successful exploit on a website.

### 1. Reconnaissance
You don't know anything about the website yet. You are trying to identify the attack surface and possible vulnerabilities. You still need to identify the objective (i.e., RCE, Authentication, Leaking Code etc...).  

**If this is you, [click here](#1-recon).**

### 2. Engagement
You have found a possible vulnerability and are trying to exploit it now. You still need to verify if this vulnerability can lead to what you want. It is possible that you find a vulnerability/bug that is completely useless to you.

**If this is you, click here.**

### 3. Exploitation/Exfiltration
You found and verified the vulnerability and need to complete the full exploit. This is where you can (if you want) write a script to complete the exploit.

**If this is you, click here.**

## Jargon Decoder

Thank you Wikipedia.

| Short Form | Full Name                 | Description                                                                                                                                                                                                                                                                          |
|------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| --         | Attack surface            | The attack surface of a software environment is the sum of the different points (the "attack vectors") where an unauthorized user (the "attacker") can try to enter data to or extract data from an environment.                                                                     |
| --         | Attack vector             | A vector in computing is the method that this code uses to propagate itself or infect a computer.                                                                                                                                                                                    |
| LFI        | Local File Inclusion      |                                                                                                                                                                                                                                                                                      |
| RFI        | Remote File Inclusion     |                                                                                                                                                                                                                                                                                      |
| SQL        | Structured Query Language | It is a programming language designed for querying and managing databases. Some examples include MySQL, Oracle SQL and SQLite.                                                                                                                                                       |
| SQLi       | SQL Injection             | A code injection technique in which malicious SQL statements are inserted into an entry field for execution (e.g. to dump the database contents to the attacker). SQL injection is mostly known as an attack vector for websites but can be used to attack any type of SQL database. |

## Ok, Enough! Let's begin.

### 1. Recon

You have to ask yourself *where*, *what* and *how* in that order.  

- *Where* is the vulnerability?
- *What* is the vulnerability?
- *How* is the vulnerability exploitable?

!!! success "I can use DevTools"
    Before continuing, can you use [DevTools](inspect.md) properly?

#### i. "Where": The Attack Surface

!!! tip
    OWASP has released a bunch of great resources. For example, I took [this list](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Attack_Surface_Analysis_Cheat_Sheet.md) from them.  
    You might be interested in [this](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Web_Service_Security_Cheat_Sheet.md) too.

Obviously if there's no way to interact with an application (i.e., a black box) then there's nothing to exploit. We have to identify possible places where a vulnerability could be hiding. Some specific points of entry are listed below. Be sure to keep track of:  

1. User interface (UI) forms and fields
2. HTTP headers and cookies
3. APIs
4. Files/Other local storage
5. Databases
7. Email or other kinds of messages

You may want to group the elements above into different types, such as:  

1. Login/authentication entry points
2. Admin interfaces
3. Inquiries and search functions
4. Data entry (CRUD) forms
5. Transactional interfaces/APIs
6. Operational command and monitoring interfaces/APIs
7. Interfaces with other applications/systems

!!! quote "From OWASP's "Attack Surface Analysis Cheat Sheet""
    For web apps you can use a tool like the [OWASP ZAP](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project) or [Arachni](http://arachni-scanner.com/) or [Skipfish](http://code.google.com/p/skipfish/) or [w3af](http://w3af.sourceforge.net/) or one of the many commercial dynamic testing and vulnerability scanning tools or services to crawl your app and map the parts of the application that are accessible over the web.

Once you've made your list of common entry points, determine how the website interacts with it. Here are some examples and some possible questions you can ask yourself:  

- A login is a possible attack surface. **How** does the website log you in? **How** are your credentials sent to the website? Is it through an HTTP POST request? **What** is being sent? Are there any **hidden values** being sent?

    !!! tip
        You can investigate further through capturing Network Requests using DevTools!

    !!! tip "Pro Tip"
        Sometimes websites will more data than you give it. These are usually in the form of `<hidden>` fields.

- Cookies can be a possible attack surface. **What** are the cookies being sent? **What** information are the cookies encoding/representing? Are the cookies encrypted? **How** are the cookies encrypted? **Why** are the cookies being sent?

    !!! tip
        Be sure to check common encodings such as Base64, JWT or even AES!

    !!! tip "Pro Tip"
        Sometimes, cookies can be misleading! Be sure to ignore cookies starting with `GA_` as those are Google Analytics cookies.

- Data entry forms are a possible attack surface. **Where and how** is the data being sent? Can you see the data after? How is the data being displayed after being entered into the system?
- HTTP Requests are a possible attack surface. Are there any **query parameters** being sent? Are there any in the URL? Look out for things such as `id=1` `lang=en` `file=index` etc...

#### ii. "What": Common Vulnerabilities


### 2. Engage

### 3. Exploit
