---
layout: post
title:      "Deeper Dive into Understanding Fetch"
date:       2017-12-10 22:19:54 +0000
permalink:  deeper_dive_into_understanding_fetch
---


One of the main appeals of using a coding language like React is how quickly it "reacts" to the site requests to display the requested content. Traditional website design makes a call to the server each time a link is clicked or input is entered and then waits for the server to respond and load the data on the page, which can cause increased loading and wait times depended on bandwidth and traffic volume.

To avoid the loading times of each request going back and forth to the server, otherwise known as synchronous calls, we complete all possible requests with one initial asynchronous task that returns a  Promise object.

Promises are created by using a Fetch method. Fetch calls upons the API or server to return the data and has a "then" function which returns our Promise. "Then" is what allows us to chain multiple calls to it.  It also contains methods that handles two possible outcomes of our Promise: "success" and "error". If the result of one of these handler is another Promise, the next handler in the code will only occur after this request is finished.

Whether it is a success or an error, these two methods are only called once during this whole Fetch request and after it is completed.

If we look at this bit of code below, it might be easy to think at first glance that the order of letters logged in the console would be "[a, b, c, d]" based on their order written in code.

![](http://res.cloudinary.com/straydar/image/upload/v1512941872/callApiCode_fuysxz.png)

But running the code acutally produces "[a, d, b, c]".

![](http://res.cloudinary.com/straydar/image/upload/v1512941868/console_results_wisjua.png)

The first letter it is told to log in the console is 'a', which makes sense, as it is the first actually piece of code being executed in this method. The next line begins our fetch to call our API. That whole piece of code has to complete before the next lines of "then" methods, our success and error methods, can run. So before console can log 'b' and 'c' , the rest of the code outside of that needs to complete. Next up is 'd', and then since there is no more code in the task, it is considered complete. This is when the code in the "then" statements run.  Each console.log() statement after that executes in order, signifying that line of code has run properly and it has behaved as it was told.

In our success response, we could specify a value for the success or error handler to kick off another promise to start on a new chain of success and error responses, depending on how complex your calls need to be.




