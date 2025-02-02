---
title: How the web works
date: 2025-02-02
---
==How the internet works==
- A *network* is made up of at least two devices that connect and communicate via a wired or wireless connection. One network switch can connect to another switch to link two networks.
- With a the *client-server model*, the Internet connects the entire world. Data travels through large undersea cables connecting the world's networks.

==What is a web server and how does it work?==
- A *server* is a computer that runs applications and services ranging from websites to instant messaging. It's called a server because it provides a service to another computer and its user also known as the client. 
	- It Is typically stored in something called a *data center* with hundreds or thousands of other servers, all running different services connected to the internet.
	- There are data centers located all around the world. Many websites use these to allow you to access your content quickly from the data center nearest to you. 
	- The data center servers are built based on the service purpose. For example, if the server is only to be used for storing images, it might have a lot of hard drive space. Whereas a server computing complex calculations might need a fast processor and a lot of memory. This is usually referred to as a *server hardware*, the physical components of a server. 
	- The code that runs on the hardware is commonly known as *software*. Software is soft or easy to change. You just replace the code running on the server.
- A type of service software known as a *web server*. 
	- Web servers consist of hardware and software.
	- Have many functions which includes website storage and administration, data storage, security and managing email. 
	- Another primary function is to handle something known as a *web request*. When you open a browser on your device and type the name of the website, it's the job of the web server to send you back to that website's content. This process is known as the *request response cycle*.
	- Web servers are also designed to respond to thousands of requests from clients per second. 

==What are websites and webpages?==
- A *web page* is a document that displays images, texts, videos and other content in the web browser, a *website* is a collection of webpages that link together.
- What are webpages made up of and just how does that webpage get from the web server to what you see on your screen or device?
	- HTML structures the content you see, CSS controls the colors and style and JavaScript is responsible for the user interaction.
	- *HTML* stands for hypertext markup language, it works by using something called markup tags. These tags describe the content that is displayed in the browser window, this content can be things like headings, paragraphs, images and even multimedia elements such as audio and video, the way html describes the content is known as **markup**.
	- *CSS* is short for cascading style sheets and adds visual enhancements like colors and layout to the web page, this is commonly known as styling. It works by enhancing the HTML elements and telling them how to display.
	- *JavaScript*, which is a programming language built into the browser. JavaScript provides web developers with tools for interactivity, data processing, control and action.
- But how exactly does this code get translated to display the content that you see on your screen?
	- When a copy of that webpage is sent from the web server to your browser, each line of code is processed in sequential order from first to last. 
	- As each line is interpreted, the browser creates the building blocks, which is the visual representation you see on the screen. 
	- This creation process is known as *page rendering*, the response from the web server must be a complete web page in order to fulfill the request, to show the page in the browser.

==What is a web browser and how does it work?==
- A *web browser*, or browser for short, is a software application that you use to browse the World Wide Web.
	- It works by sending a request to a web server and then receives a response containing the content that is to be displayed on the screen of your device.
- The URL contains the protocol or the HTTP, the domain name, usually the name of the website, and the file path, or the path to the page that is displayed. When you make a request using this URL, the browser and server communicate using a protocol known as the **Hypertext Transfer Protocol** or *HTTP*. 
> - First, you open a web browser, which is a software application. Next, you type the domain name. Then when you press Enter, the web browser sends a request across a network and connects to another computer on the Internet called a web server, which takes requests for data. The web server responds by sending a webpage back to the browser. Once the browser receives all the response information, the webpage is made visible. The web page is a coded document that is rendered by the browser and then presented visually to you, the end-user. Now that the webpage is loaded in the browser, you interact with that page.
- 