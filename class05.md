# Class 05 Readings (Sept. 14th)

## Webscraping

- HTTP clients are tools capable of sending a request to a server and then receive a response from it. Almost every tool that will be discussed uses an HTTP client under the hood, to query the server of the website that you will attempt to scrape.

### Superagent

- Much like Axios, Superagent is another robust HTTP client that has support for promises and the async/await syntax sugar. It has a fairly straightforward API like Axios, but Superagent has more dependencies and is less popular.

### Getting Started with Webscraping

- The simplest way to get started with web scraping without any dependencies is to use a bunch of regular expressions on the HTML string that you receive by querying a webpage using an HTTP client, but there is a big tradeoff. Regular Expressions aren't as flexible and quite a lot of people both professionals and amateurs struggle with writing the correct regular expression.

## MDN querySelector

- The Document method querySelector() returns the first Element within the document that matches the specified selector, or group of selectors. If no matches are found, null is returned.

- A DOMString containing one or more selectors to match. This string must be a valid CSS selector string; if it isn't, a SYNTAX_ERR exception is thrown. See Locating DOM elements using selectors for more about selectors and how to manage them.

- An HTMLElement object representing the first element in the document that matches the specified set of CSS selectors, or null is returned if there are no matches.

## MDN querySelectorAll

- The Document method querySelectorAll() returns a static (not live) NodeList representing a list of the document's elements that match the specified group of selectors.