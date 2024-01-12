a domain name is a string of text that maps to an alphanumeric IP address, used to access a website from a client software. domain names are typically broken into 2/3 parts, each separated by a dot.

a uniform resource locator (URL) contains the domain of a site as well as other information, including the protocol and the path.

# anatomy of a URL
a URL is composed of different parts, some mandatory and other optional.
![anatomy of a URL](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL/mdn-url-all.png)

- **scheme**: the first part of the URL is the scheme, which indicates the protocol that a browser must use to request the resource
- **authority**: the authority includes both the domain and the port separated by a colon
	- port indicates the technical "gate" used to access the resources on the web server, usually omitted if the web server uses standard ports of the HTTP protocol (80 for HTTP and 443 for HTTPS)
- **path to resource**
- **parameters**: extra parameters are a list of key value pairs separated by the & symbol

# references
- https://www.cloudflare.com/en-gb/learning/dns/glossary/what-is-a-domain-name/
- https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL
