# REGEX Pentest
### URL´s

Here's an example of how you could use this pattern in grep to find all domains and subdomains in a file:
```
grep -Eor '([a-zA-Z0-9-]+\.)+[a-zA-Z]{2,}' file.txt
```

Here's an example of how you could use this pattern in grep to find all internationalized domains and subdomains.

```
grep -Pro '([\p{L}\p{N}-]+\.)+[\p{L}\p{N}-]{2,}' file.txt
```
Here is another complex regular expression pattern that you can use to find all domains and subdomains in a string:
```
grep -Pro '(([\p{L}\p{N}-]+\.)|(\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]))+[\p{L}\p{N}-]{2,}' *
```

Here's an example of how you could use this pattern in grep to find all domains and subdomains.

```
grep -Po '(([\p{L}\p{N}-]+\.)|(\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]))+((xn--[\p{L}\p{N}-]+)|([\p{L}\p{N}-]{2,}))' *
```

### Email's

Here's an example of how you could use this pattern in grep to find all emails.

```
grep -rEo "[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,6}" *
```

### AWSKeys

```
grep -HanrE "([^A-Z0-9]|^)(AKIA|A3T|AGPA|AIDA|AROA|AIPA|ANPA|ANVA|ASIA)[A-Z0-9]{12,}" *
```

### BASE64

```
grep -HanroE "([^A-Za-z0-9+/]|^)(eyJ|YTo|Tzo|PD[89]|aHR0cHM6L|aHR0cDo|rO0)[%a-zA-Z0-9+/]+={0,2}" *
```

### CORS

```
grep -HnriE "Access-Control-Allow" *
```

### DEBUG

```
grep -HnraiE "(Application-Trace|Routing Error|DEBUG\"? ?[=:] ?True|Caused by:|stack trace:|Microsoft .NET Framework|Traceback|[0-9]:in |#line [0-9]|SQLSTATE)" *
```

### firebase

```
grep -Hnri "firebaseio.com" * 
```
