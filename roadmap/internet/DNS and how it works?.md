the DNS is the phone book of internet. DNS translates domain names to IP addresses so browsers can load internet resources.

# how does DNS work?
the process of DNS resolution involves converting a hostname into an IP address. an IP address is given to each device on the internet, and that address is required to find the appropriate device.

for the web browser, the DNS lookup occurs "behind the scenes" and requires no interaction from the user's computer apart from the initial request. there are 4 DNS servers involved in loading a webpage:
- DNS recursor
- root nameserver
- top level domain (TLD) nameserver
- authoritative nameserver

# recursive DNS resolver
it is the computer that responds to recursive request from a client and takes the time to track down the DNS record. it does this by making a series of requests until it reaches the authoritative nameserver for the requested record.

![DNS record request sequence](https://cf-assets.www.cloudflare.com/slt3lc6tev37/3NOmAzkfPG8FTA8zLc7Li8/8efda230b212c0de2d3bbcb408507b1e/dns_record_request_sequence_recursive_resolver.png)

# authoritative DNS server
it is a server that actually holds, and is responsible for DNS resource records. it is the server at the bottom of the DNS lookup chain that will respond with the queried resource record, allowing the web browser making the request to reach the IP addresses needed to access a website or other web resources.

# steps in a DNS lookup
1) write an URL into a web browser and the query is received by a DNS recursive resolver
2) the resolver then queries a DNS root nameserver
3) the root nameserver then responds to the resolver with the address of a TLD DNS server, which stores the information for its domains
4) the resolver then makes a request to the domain TLD
5) the TLD server then responds with the IP address of the domain's nameserver
6) the recursive resolver sends a query to the domain's nameserver
7) the IP address for URL is then returned to the resolver from the nameserver
8) the DNS resolver then responds to the web browser with the IP address of the domain requested initially

![DNS lookup](https://cf-assets.www.cloudflare.com/slt3lc6tev37/1NzaAqpEFGjqTZPAS02oNv/bf7b3f305d9c35bde5c5b93a519ba6d5/what_is_a_dns_server_dns_lookup.png)

# types of DNS queries
- recursive: client requires that a DNS server will respond to the client with either the requested record or an error message if the resolver can't find the record
- iterative: client will allow a DNS server to return the best answer it can