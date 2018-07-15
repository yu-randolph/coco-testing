# COCO API Testing

Quick and easy steps on how to test our API

## Getting Started
You need to have 2 types of servers:
1. Apache Tomcat
2. Apache2

Any LAMP stack will do (MAMP,WAMP,XAMP) for my case I use MAMP for a quick and easy way to get this up and running.
For the Tomcat, the simplest way to get this up and running is to just run it in IntelliJ

## Server Configurations

Open up your IDE, in my case for the video it was IntelliJ. You must allow Cross origin for your 2 servers to connect.
Let us say you are running our Testing code in Port 8888, then you need to add the line "@CrossOrigin(origins = "http://localhost:<PORT>")" right above the following:
1. getConcepts
2. getConcordances
3. getPattern
4. getPatternFilterByID
5. getSuggestions
```
...
@CrossOrigin(origins = "http://localhost:8888")
@RequestMapping(value = "/getConcepts", method = RequestMethod.POST)
...
...
@CrossOrigin(origins = "http://localhost:8888")
@RequestMapping(value = "/getConcordances", method = RequestMethod.POST)
...
...
@CrossOrigin(origins = "http://localhost:8888")
@RequestMapping(value = "/getPattern", method = RequestMethod.POST)
...
...
@CrossOrigin(origins = "http://localhost:8888")
@RequestMapping(value = "/getPatternFilterByID", method = RequestMethod.POST)
...
...
@CrossOrigin(origins = "http://localhost:8888")
@RequestMapping(value = "/getSuggestions", method = RequestMethod.POST)
...
```
For your client, simply put it in the htdocs folder and go to your URL.

## How to use:
Go to the client URL and press the 3 buttons in order from left to right. Wait for the popup to show before moving on.
