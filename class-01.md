# class-01 summary
## Introduction to HTML and CSS:

* ***web browser*** is a software application for accessing information on the World Wide Web. Popular examples : Firefox, Internet Explorer, Safari, Chrome, and Opera. In order to view a web page, users might type a web address into their browser, follow a link from another site, or use a bookmark.

* When you ask your browser for a web page, the request is sent across the Internet to a special computer known as a  ***web server*** which hosts the website.

* People are accessing websites on an increasing range of ***devices*** including desktop computers, laptops, tablets, and mobile phones.

* ***Screen readers*** are programs that read out the contents of a computer screen to a user. They are commonly used by people with visual impairments.
### How  websites are  created? 
All websites use HTML and CSS, but content management systems, blogging software, and e-commerce platforms often add a few more technologies into the mix.
### How the web works? 

  1. When you connect to the web, you do so via an ***Internet Service Provider (ISP)***. You type a domain name or web address into your browser to visit a site
  2. Your computer contacts a network of servers called ***Domain Name System (DNS)*** servers. These act like phone books; they tell your computer the IP address associated with the requested domain name. An IP address is a number of up to 12 digits separated by periods / full stops. Every device connected to the web has a unique IP address; it is like the phone number for that computer.

  3. The unique number that the DNS server returns to your computer allows your browser to contact the web server that hosts the website you requested. A web server is a computer that is constantly connected to the web, and is set up especially to send web pages to users.
  4. The web server then sends the page you requested back to your web browser.


## STRUCTURE: 
* HTML refer to ***HyperText Markup Language***.
* HTML elements are usually made up of two  tags: an opening tag and a closing tag. (The closing tag has an extra forward slash in it.) Each HTML element tells the browser something about the information that sits between its opening and closing tags( Tags act like containers) HTML uses elements to describe the structure of Pages. 
* Attributes tell more  about  elements by providing additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a  **name** and a  **value**, separated by an equals sign. 
* < body > : Everything inside this element is shown inside the main browser window.
* < head > Before the  < body >  element you will often see a  this element which contains information about  the page and  you will usually find a  < title > element inside it .
* < title > The contents of it is shown in the top of the browser, above where you usually type in the URL of the page you want to visit, or on the tab for that page .

## EXTRA MARKUP: 
* Since the web was first created, there have been several different versions of HTML.
  - HTML 4: released 1997 .
  - XHTML 1.0 :released 2000.
  - HTML 5 :released 2000.
* DOCTYPE : Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using.

* To add a comment to the code that will not be visible in the user's browser, you can add the text between these characters: 
< !-- comment goes here -- >
* Every HTML element can carry the  id  attribute. It is used to uniquely identify that element from other elements on the page. 
* The  id  attribute is known as a global attribute  because it can be used on any element.
* Every HTML element can also carry a  class  attribute. It used to identify more than one uniquely element within a document and on any element can share the same value. 
* Some elements will always appear to start on a new line in the browser window. These are known as  block level  elements. Examples of block elements are < h1 >,  < p >,  < ul >, and  < li >.
* Some elements will always appear to continue on the same line as their neighbouring elements. These are known as inline  elements. Examples of inline elements are < a >,  < b >,  < em >, and  < img >.
* The  < div >  element allows you to group a set of elements together in one block-level box.
* The  < span >  element acts like an inline equivalent of the  < div > element. It is used to either: 
1. Contain a section of text where there is no other suitable element to differentiate it from its surrounding text 
2. Contain a number of inline elements
* < iframe > An iframe is like a little window that has been cut into your page — and in that window you can see another page. The term iframe is an abbreviation of inline frame.

* The  < meta >  element lives inside the  < head >  element and contains information about that web page.
* The  < meta >  element is an empty element so it does not have a closing tag. It uses attributes to carry the information.
* Escape characters are used to include special characters in your pages such as <, >, and ©.

## HTML5 laytout : 
* HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them. 
* The  < header >  and  < footer > elements can be used for: ● ● The main header or footer that appears at the top or bottom of every page on the site. A header or footer for an individual  < article >  or < section > within the page.
* The  < nav >  element is used to contain the major navigational blocks on the site such as the primary site navigation.
* The  < article >  element acts as a container for any section of a page that could stand alone and potentially be syndicated.
* The  < aside >  element has two purposes, depending on whether it is inside an  < article > element or not. When the  < aside >  element is used inside an  < article > element, it should contain information that is related to the article but not essential to its overall meaning. When the  < aside >  element is used outside of an  < article > element, it acts as a container for content that is related to the entire page.
* The  < section >  element groups related content together, and typically each section would have its own heading.
* The purpose of the  < hgroup > element is to group together a set of one or more  < h1 >  through < h6 >  elements so that they are treated as one single heading. 
* < figure > - to add figure(Images, Videos, Graphs, Diagrams, Code samples, Text that supports the main body of an article) inside the < article > .
* < figure > element should also contain a < figcaption > element which provides a text decription for the content of the < figure > element.
* The new elements provide clearer code (compared with using multiple  < div >  elements). 
* Older browsers that do not understand HTML5 elements need to be told which elements are block-level elements. 

* To make HTML5 elements work in Internet Explorer 8 (and older versions of IE), extra JavaScript is needed, which is available free from Google.

## Process & design : 

* Every website should be designed for the target audience. It is very important to understand who your target audience is.why they would come to your site, what information they want to find and when they are likely to return.
* ***Site maps*** allow you to plan the structure of a site.
* To decide what information should go on each page, you can use a technique called ***card sorting***.
* ***Wireframes*** allow you to organize the information that will need to go on each page.
* Design is about communication. Visual hierarchy helps visitors understand what you are trying to tell them.
* You can differentiate between pieces of information using size, color, and style.
* You can use grouping and similarity to help simplify the information you present.


## Introuction to JavaScript : 
* JavaScript used to make websites more interactive( by accessing and modifying the content, Programing rules or instructions the browser can follow ,responding to what the user does) interesting, and user-friendly.
>jQuery makes writing JavaScript a lot easier.


* A script is a series of instructions that a computer can follow to achieve a goal step-by-step.

* Each time the script runs, it might only use a subset of all the instructions.

* Computers approach tasks in a different way than humans, so your instructions must let the computer solve the task programmatically.

* To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it.
     1. DEFINE THE GOAL
     2. DESIGN THE SCRIPT (using flow chart to help )
     3. CODE EACH STEP

* **How do computers fit in with the world around them** ? 
* Computers create models of  the world using data .
* in computer programming,each physical thing in the world can be represented as object . And , each object can have its own properties( name and value ) ,events(to trigger methods) and methods(can retrieve the properties).
* Web browsers use HTML markup to create a model of the web page.Each element creates its own ***node*** .
* ***The interpreter(scripting engine)*** takes the instructions in javascript and translates them so the browser can use them to achieve the tasks.

* ***separation of concerns***:


![image](data:image/png;base64,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)
* JavaScript file is text file with extension (.js) .
* It's best to keep JavaScript code in its own JavaScript file .
* The HTML< script > element {in the end of < body > after the < footer > } used to tell browser to lead the Javascript file .
