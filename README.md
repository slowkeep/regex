# REGEX Pentest
### URL´s

```
grep -Eor '([a-zA-Z0-9-]+\.)+[a-zA-Z]{2,}' file.txt
```

```
grep -Pro '([\p{L}\p{N}-]+\.)+[\p{L}\p{N}-]{2,}' file.txt
```
```
grep -Pro '(([\p{L}\p{N}-]+\.)|(\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]))+[\p{L}\p{N}-]{2,}' *
```

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

### FW

```
grep -HnriE "django\|laravel\|symfony\|graphite\|grafana\|X-Drupal-Cache\|struts\|code ?igniter\|cake ?php\|grails\|elastic ?search\|kibana\|log ?stash\|tomcat\|jenkins\|hudson\|com.atlassian.jira\|Apache Subversion\|Chef Server\|RabbitMQ Management\|Mongo\|Travis CI - Enterprise\|BMC Remedy\|artifactory" * 
```

### IP´s

```
grep -HnroE "(([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])\\.){3}([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])" *
```

###  Dates of birth
```
\b((19|20)\d{2})[-/.]?(0[1-9]|1[0-2])[-/.]?(0[1-9]|[12][0-9]|3[01])\b
```
### Passport numbers

```
\b[A-Z]{2}\d{7}\b
```

### International Bank Account Numbers (IBANs): 

```
\b[A-Z]{2}\d{2}\s?(?=(\d{4}\s?){4})(\d{4}\s?){3}\d{1,4}\b
```

### Health Insurance Portability and Accountability Act (HIPAA) identifiers: 

```
(SSN|NPI|EIN|UPIN|HICN|MEDICAID|MEDICARE)
```
