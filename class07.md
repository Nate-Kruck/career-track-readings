# Class 07 Readings (Sept. 21tst)

## HTTP Basics

- HTTP stands for Hypertext Transfer Protocol.

- HTTP allows for communication between a variety of hosts and clients, and supports a mixture of network configurations.

- Communication between a host and a client occurs, via a request/response pair.

- At the heart of web communications is the request message, which are sent via Uniform Resource Locators (URLs).
  - get, post, put, delete

### Status Codes

- 1xx: Informational Messages
  All HTTP/1.1 clients are required to accept the Transfer-Encoding header.

- 2xx: Successful
  This tells the client that the request was successfully processed. The most common code is 200 OK.

- 3xx: Redirection
  404 indicates that the resource is invalid and does not exist on the server.

- 4xx: Client Error
  These codes are used when the server thinks that the client is at fault, either by requesting an invalid resource or making a bad request. The most popular code in this class is 404 Not Found

- 5xx: Server Error
  This class of codes are used to indicate a server failure while processing the request. The most commonly used error code is 500 Internal Server Error.

## How DNS works

- Computers and other devices communicate using IP addresses to identify each other on the internet. But humans can't remember IP addresses, so they use words.

- The domain name system (DNS) brings the two together and gets you to your destination.

- The resolver server is usually your ISP (Internet Service Provider). All resolvers must know one thing: where to locate the root server.

- The root server knows where to locate the .COM TLD server. TLD stands for Top-Level Domain.

- Root servers sit at the top of the DNS hierarchy. They are scattered around the globe and operated by 12 independent organisations.
  - They are named [letter].root-servers.net where [letter] ranges from A to M.
  - Each organisation provides multiple physical servers distributed around the globe.
