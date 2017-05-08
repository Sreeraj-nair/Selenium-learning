# Selenium Grid Concepts

## What is Selenium Grid? 
Selenium Grid allows you to run your tests on different machines against different browsers in parallel. That is, running 
multiple tests at the same time against different machines running different browsers and OS. It supports distributed test execution. 

## When to use Selenium Grid? 
  - To run your tests against multiple browsers, multiple versions of browser, and browsers running on different operating systems.
  - To reduce the time it takes for the test suite to complete a test pass.

## How Selenium Grid works? 
A grid consists of a single hub, and one or more nodes. Both are started using the selenium-server.jar executable. 

## Starting Selenium-Grid
Generally you would start a hub first since nodes depend on a hub. This is not abolutely necessary however, since nodes can 
recognize when a hub has been started and vice-versa. For learning purposes though, it would easier to start the hub first, 
otherwise you’ll see error messages that may not want to start off with your first time using Selenium-Grid.

## Starting a Hub
    - java -jar selenium-server-standalone-2.44.0.jar -role hub

## Starting a Node
    - java -jar selenium-server-standalone-2.44.0.jar -role node  -hub http://localhost:4444/grid/register
