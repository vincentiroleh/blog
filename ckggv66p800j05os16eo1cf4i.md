## The Basics of Consuming REST APIs

Learn the basics of using REST APIs by building a GitHub Finder.

**REST APIs** are becoming very popular and are a must-know for every type of developer. In this article, I'll go over the basics of what they are and how to use them.

The word **consuming** used among developers when referring to APIs simply means the act of consuming or using a REST API means to eat it all up (to eat it, swallow it and digest it). Sounds yummy 😋? 

It seems that every application out there is hungry for an API. Let's look at Uber for example. Uber by itself won't have the functionality you'd expect. In order to search nearby drivers and locations, it needs to use an API for a map. It uses Google map API, with that it can locate the nearest driver and allows you to book a taxi. APIs allow developers to integrate one tool into another to give it more functionality. 

## But what are an API and REST?

**API** stands for "Application Programming Interface". It is a way to get one software application to talk to another software application.

**REST** stands for "Representational State Transfer". It is how the API looks like, it is a set of rules that developers follow when they create their API. One example of these rules states that you should be able to get a piece of data (called a resource) when you make a call or link to a specific URL.

Each URL is called a **request**, while the data sent back to you is called a **response**.

## So why are APIs so important?

There are several different software applications used by most companies, including banking, security services, project management system, etc. To have the software all work together is increasingly important, which is also making work processes flow more easily. Companies also create their own tools using other APIs to enhance their own software, making their customers happier and giving them the tools they need.

## Let's Consume An API

I will be showing you how to make a basic request to the  [GitHub API](https://developer.github.com/v3/), and display the user's information on a web page.


> 
Working with APIs requires you to study the documentation of that API, to understand how it works.

**Code Sample**

%[https://codepen.io/iroleh/pen/XWKKEeE]

In the code sample above we consumed the GitHub API that allows us to get the user's information. 

By making a request to the GitHub API `https://api.github.com/users/{user}` which returns a response with the data of the user, we were able to use this data to manipulate our HTML.

**Important Concept**

- **fetch()**: A simple interface for fetching resources. Fetch makes it easier to make web requests and handle responses. [Read more](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) 
- **querySelector()**:  returns the first element within the document that matches the specified selector, or group of selectors. [Read more](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)
- **preventDefault()**:  stops the default action of an element from happening. [Read more](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault)
- **trim()** : The trim() method removes whitespace from both ends of a string. [Read more](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/String/trim)

<hr>

[Github Repo](https://github.com/vincentiroleh/github-finder)

I hope this article was helpful. If so, share this article and follow me on [Twitter](https://twitter.com/IrolehVincent)