# class-04 summary

## Links in HTML :
* **Links** are the defining feature of the web because they allow you to move from one web page to another.
*Links are created using the***< a > element***. Users can click on anything between the opening < a > tag and the closing < /a > tag. You specify which page you want to link to using the ***href attribute***.

  1. **Linking to Other Sites** :the value of the href attribute will be the full web address for the site, which is known as an ***absolute URL***.
  2. **Linking to Other Pages on the Same Site**: the href attribute will be a ***relative URL***.
![image](https://openlab.citytech.cuny.edu/clarkeadv2450/files/2012/08/xid-3696810_1.jpeg)
* On larger websites it's a good idea to organize your code by placing the pages for each different section of the site into a new folder. Folders on a website are sometimes referred to as ***directories***.
* The top-level folder is known as the **root folder**.
* The main homepage of a site written in HTML .

  3.**Email Links** : the value of the href attribute starts with mailto: and is followed by the email address.
  4. **Opening Links in a New Window** : by using the target attribute on the opening < a > tag. The value of this attribute should be _blank.
  5. **Linking to a Specific Part of the Same Page**: 
     - Before you can link to a specific part of a page, you need to identify the points in the page that the link will go to. You do this using the id attribute (which can be used on every HTML element).
     -To link to an element that uses an id attribute you use the < a > element again, but the value of the href attribute starts with the # symbol, followed by the value of the id attribute of the element you want to link to.
  6. **Linking to a Specific Part of Another Page** :the href attribute will contain the address for the page (either an absolute URL or a relative URL), followed by the # symbol, followed by the value of the id attribute that is used on the element you are linking to.

 ## Layout CSS :
 * If one block-level element sits inside another block-level element then the outer box is known as the **containing** or **parent element**.
 * A box may be nested inside several other block-level elements. The containing element is always the direct parent of that element.
 * <div> elements are often used as containing elements to group together sections of a page.
 * CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the **position property** in CSS. You can also float elements using the **float property**.
   1. Normal flow :Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one.
   2. Relative Positioning( position:relative ): This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed.
   3. Absolute positioning ( position:absolute , ex :Fixed Positioning): This positions the element in relation to its containing element.
 * **box offset properties** to tell the browser how far from the top or bottom and left or right it should be placed.
 * **z-index property**(stacking context) allows you to control which box appears on top.Its value is a number, and the higher the number the closer that element is to the front.
 * You do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be:
     position: static;
 * Fixed positioning ( position:fixed ) is a type of absolute positioning that requires the position property to have a value of fixed. It positions the element in relation to the browser window.
 * The **float property** allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible. Anything else that sits inside the containing element will flow around the element that is floated.
 * A lot of layouts place boxes next to each other. The float property is commonly used to achieve this.
 * Floated items require a defined width.
 * The clear property specifies what elements can float beside the cleared element and on which side.It can take the following values: left ,right, both or none.
 * Using the float property can cause a startling problem for CSS newbies: If floated elements have non-floated parent elements, the parent will collapse. 
     * Solution 1 : Float the parent.
     * Solution 2 : Give the parent an explicit height. 
     * Solution 3 : Append a "spacer" element inside the parent element.
     * Solution 4 : Set parent to overflow: auto.
 * Many web pages use multiple columns in their design. This is achieved by using a <div> element to represent each column. The following three CSS properties are used to position the columns next to each other: 
     * width : This sets the width of the columns.
     * float : This positions the columns next to each other.
     * margin : This creates a gap between the columns.
 * Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.
 * ***Resolution*** refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.
 * Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens).
 * Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.
 * Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.
 * Composition in any visual art (such as design, painting, or photography) is the placement or arrangement of visual elements — how they are organized on a page. Many designers use a grid structure to help them position items on a page, and the same is true for web designers.
 * Grids set consistent proportions and spaces between items which helps to create a professional looking design.
    1. Creates a continuity between different pages which may use different designs
    2.  Helps users predict where to find information on various pages.
    3. Makes it easier to add new content to the site in a consistent way.
    4.  Helps people collaborate on the design of a site in a consistent way.
 * CSS Frameworks provide rules for common tasks.


 ## “Functions, Methods, and Objects” in JavaScript
 * Programmers use functions, methods, and objects to organize their code.
 * **WHAT IS A FUNCTION?**
  - Functions let you group a series of statements together to perform a specific task. It's a reusable code which can be called anywhere in your program. This eliminates the need of writing the same code again and again. It helps programmers in writing modular codes. Functions allow a programmer to divide a big program into a number of small and manageable functions.
 ![image](https://www.miltonmarketing.com/wp-content/uploads/2018/04/mmjavascriptfunctions234234234functions-min.png)
 * A defined function doesn’t execute automatically. A function definition only specifies what to do when we execute the function. The actual execution is possible with the help of function invocation or function call.The syntax for function invocation is like this:

     + functionName(arguments);
 * The terms ***parameters*** and ***arguments*** are often interchangeably used as if it were one and the same thing but there is a very subtle difference.
     + Parameters are variables listed as a part of the function definition.
     + Arguments are values passed to the function when it is invoked.
* Some functions return information to the code that called them. Functions can return more than one value using an array.
![imagee](https://res.cloudinary.com/practicaldev/image/fetch/s--AYsS4JEv--/c_imagga_scale,f_auto,fl_progressive,h_500,q_auto,w_1000/https://cl.ly/cfe13d79d4a3/download/Image%25202018-11-29%2520at%25201.17.04%2520PM.png)
* An **anonymous function** is a function without a name. An anonymous function is often not accessible after its initial creation.
* **Immediately invoked function execution**: If you want to create a function and execute it immediately after declaration, you can use the anonymous function like this:
(function() {
    console.log('IIFE');
})();
*  The location where you declare a variable will affect where it can be used within your code. If you declare it within a function, it can only be used within that function. This is known as the **variable's scope**. 
* When a variable is created inside a function it can only be used in that function.It is called a ***local variable*** or ***function-level variable***.This means that:
      +  If the function runs twice, the variable can have different values each time.
      +  Two different functions can use variables with the same name without any kind of naming conflict.
 
* If you create a variable outside of a function, then it can be used anywhere within the script. It is called a ***global variable*** and has global scope.
* Global variables use more memory. The browser has to remember them for as long as the web page using them is loaded. Local variables are only remembered during the period of time that a function is being executed.


## 6 Reasons for Pair Programming:
* Pair programming is the practice of two developers sharing a single workstation to interactively tackle a coding task together.
* ***How does pair programming work?***
 -  Pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer while the Navigator guide the Driver but does not provide any direct input to the computer.
* ***Why pair program?***
 1.  Greater efficiency : pair programing takes slightly longer, but produces higher-quality code that doesn’t require later effort in troubleshooting and debugging.
 2. Engaged collaboration. 
 3. Learning from fellow students:the developers in a pairing have different skill sets. If one programmer is more experienced in a certain skill, they can teach a student who is less familiar with that area. 
 4. Pair programming is great for improving social skills. 
 5.  Job interview readiness : Pair programming strengthens all skills for most roles in companies such as  the ability to work with and learn from others and stellar communication skills .
 6. Work environment readiness .


