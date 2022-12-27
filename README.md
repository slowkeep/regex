# REGEX Pentest
### URL´s

Simple URL regex:
```
/https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)/
```
This regular expression will match most basic URLs that start with http:// or https://. It includes optional support for a www. subdomain.

URL with optional protocol and subdomain:
```
/(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)/
```
This regular expression is similar to the previous one, but it allows the protocol and www. subdomain to be optional.

URL with support for multiple subdomains:
```
/(https?:\/\/)?(([\w-]+\.)+[a-zA-Z]{2,})(:[0-9]{1,5})?(\/[\w-.\/?%&=]*)?/
```
This regular expression allows for multiple subdomains and also supports an optional port number.

URL with support for query parameters:
```
/(https?:\/\/)?(([\w-]+\.)+[a-zA-Z]{2,})(:[0-9]{1,5})?(\/[\w-.\/?%&=]+)?(\?[\w-.=&]+)?/
```
This regular expression is similar to the previous one, but it also supports optional query parameters.

Keep in mind that regular expressions can be complex and it is not always easy to capture all possible variations of a URL. You may need to modify these regular expressions to fit your specific needs.
