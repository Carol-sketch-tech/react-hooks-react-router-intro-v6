## Client server routing.

- weh have learned about building compoennts changing state , passing props and even interacting with APIs.
all therse are required inorder to master creation of single pade applications, however we have to learn how we can separate our components onto different pages each wiht their own unique URl
- learinig how to seperate out our component onnto different pages each with their unique URL.
- 
Fo the manority of applications that arent single -page Application routingdescribes the following process:
 1. A user clicks on a link
 2. that link has its won distinct URl 
 3. th ebrowser makes a GET request to the server for the componnet fot he oage.

 Note that with client-side routing, the process will look different fo rone very important reason, the goal of client-side routing is to handle all the trouting logic wiht javascript, without making any additional GET requests for some new HTML document.

 For example our client-side app is going to have thrse routes
 1. /movies
 2. /about
 3. /login

 - the reacts server's only job is to render the HTML document.
 with client server routing the server ins not responsibel for handling thr routing,fetching and diplaying if the data in the browser.
 these are done by the client-side code intead.
  - with client-side routing you might get all the data necessary to render all three pages on the first page load , then when a suer clicks around your site, the client-side router swaps the movies page component with the about page component and renders faster than it would if you were requesting each sepearate page from a server.
  benefits of using a client-side router is the speed since we are only making on reques.

  ## single page applications.(SPAs)
  - these aoos do not require mulitple pages ot be loaded from the server, just the original GET request with our initla HTML,CSS nad Js files
  - few things to take into consderation;
   1. we want to make sure we have a URL that display what the user is doing at that moment. so if they are viewing a bio page it might look like react-hooks-react-router-intro-v6.com/bio instead of react-hooks-react-router-intro-v6.com.
   2.we want the user to be able to use the browsers back and forward buttons as well as the browser history with ease.
   3. we want a user to be able to input a URL into the adress bar and navigate tot he view they need to see.

   ## limits of client-side routing.
   - loading of the css and javascript.-since the css and js files are being loaded it can take a while to load our first page. this can be important as the first page might take a while to lead considering if one has a huge application.
   - Anlytics -
   - single page appliations are harder to design than traditional multi-page applications.

   ## React Routing 
   key features of react routing 
   1. conditional rendering of a component based on the URL e.g if the UrL is /movies the the <Movies> component is rendered.
   ## Location API
   - you can access the location in the URL bar from any website by typing this in the console in the browser's dev tools.
   window.location:
   - this will return the location object will all kinds of useful information including the pathname.

   ## History of APIs
   when we load a new page in the browser that information is saved in browser histoy
   Go to javascript console in the browser and type the following 
   window.history;

   the return should be the following code:
   {length:32, state:null, scrollRestoration:"auto"};
   length is how many location you have visited in this new window session.
   if you type window.history.back, it will take you back tothe last location you visited.
   you can also do window.history.forward()


with javascripts history APi we also have the ability to sue the windoe.history.pushState()
method to programatically navigate to a new page.
- teh window.history.pushState() take in three paramters:
1. state- this is plain javascript object that is associated wiht the new history wntry we are goign to create witht he pushStatefunction.
2. title- this is the current ignored by most browsers and it makes it safe to just pass ans emptystring here
3. URL - this is the URL for the new history entry, the browser will  not attmept to load this URL after it calls pushStatenpm i