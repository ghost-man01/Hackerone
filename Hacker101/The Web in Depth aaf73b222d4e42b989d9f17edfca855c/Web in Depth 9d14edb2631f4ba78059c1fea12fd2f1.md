# **The Web in depth**

The website is sending the request to the server. # —————————————————— 
**Request Headers

**Host** – Indicates the desired host handling the request

**Accept** – Indicates which MIME types(s) accepted by the client.Often used to specify JSON or XML output for the web-services.

**Cookie** – Passes cookie data to the sever.

**Referer** – Which page actually led to that request.

**Authorization** – Used for ‘Basic auth’ pages. Takes the form “Basic<basic64’d username:password>”

## Cookies

Cookies are key-value pairs and exist in client . They are present for an fixed Period of time. Sent from the Server and added by the JAVASCRIPT.They are sent to each domain that they are scoped. Each cookie has domain pattern that has matches sometimes it’s very specific and sometimes it’s root domain. If you can set cookies where they are not supposed to that is also be a breach of security.

## Cookie Security

The cookies are only work on HTTPS pages. It’ll never be set up in pure plain HTTP request

Httpsonly – Doesn’t do the Opposite of security. It make sure that it only sent the cookies up on the web request. It wouldn’t allow you to read the cookies from javascript.

from Java-script normally use (document.cookies) and all the list of cookie that are applied

Secure: The cookie will only accessible to the https pages.

Httponly: The cookie cannot be read by the Javascript.

These are present in Set-cookie header place.

## HTML-Parsing

Html is just not parsed by only BROWSER but it’s also parsed by Web-application firewalls and look at many things like cross-site scripting. Whenever there is discrepancy in how these two items parse things, probably there’s a vuln that you can exploit.

## Legacy Parsing

Due to decades of bad HTML browsers are quite excellent at cleaning up after authors, and these conditions are often exploitable:

tag on its own the script tag will automatically close at end of the page. If you can add HTML in a page. If there is cross-site scripting in the url and you can’t get a SLASH because there is a parse of path separator. A tag missing it’s closing angle bracket will automatically closed by the angle bracket of the next tag on the page.

## Content Snipping

Content snipping is the sending data to browser without giving all information of what are you sending.

## Mime Sniffing

Mime type sniffing means what type of file are you sending it.

Use by many browser. The browser just not look at the Content type headers but also look at what’s on the page. If there are enough marker that make look like HTML, The browser treat like HTML.

```
In IE 6/7 era bugs where image and text file that has proper **MIME** type set down and contain enough HTML What actuall executes as HTML.
```

These are old now but these are installed in company and enterprises have a big issue about this.

Always set **Mime type** no matters what even if you’re sending an octet stream.

## Encoding Sniffing

Checking what type of sort text encoding you are sending it.

Put the example of UTF-7 (7 bit unicode with the Base64’d blocks denoted by +..- ) text into xss payloads.

## Same Origin Policy
[[DOM]]
How browser restrict a number of security-critical features :

1. What domains you contact via XmlhttpRequest
2. Access to the DOM across separate frames/windows.

When anytime its circumvented in some way bad things going to happen for everyone.

## Origin Matching
- It's much more strict than cookies 
- Protocol must match you will never cross https/http boundaries 
- Port number must 
- Domain name must be in exact match.

## SOP loosening
It's possible for developers to loosen the grip of **document.domain** and that will allow you to which subdomain in essence you are able to communicate with and there are rules
