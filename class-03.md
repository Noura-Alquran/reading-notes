# class-03 summary
## Lists:
* There are three different types of lists in HTML :
  1. ***Ordered lists*** are lists where each item in the list is numbered.
  2. ***Unordered lists*** are lists that begin with a bullet point (rather than characters that indicate order).
  3. ***Definition lists*** are made up of a set of terms along with the definitions for each of those terms.

* The ordered list is created with the < ol > element.Each item in the list is placed
between an opening < li > tag and a closing < /li > tag. (The li stands for list item.)

* The unordered list is created with the < ul > element.Each item in the list is placed
between an opening < li > tag and a closing < /li > tag. 

* The description list is created using < dl > element. The < dl > element is used in conjunction with the < dt > element which specify a term, and the < dd > element which specify the term's definition.

* You can put a second list inside an < li > element to create a sublist or ***nested list***.

## Boxes :
* All HTML elements can be considered as boxes. In CSS, the term "box model" is used when talking about design and layout.

* The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.
![image](https://miro.medium.com/max/565/1*6DrszcyPybYDGziiS9CWdg.png)

* To set your own dimensions for a box you can use the **height** and **width** properties. The most popular ways to specify the size of a box are to use pixels, percentages, or ems.
* the min-width/ min-height property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width /max-height property indicates the maximum width a box can stretch to when the browser window is wide.
* The **overflow** property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values:
     - **hidden**:This property simply hides any extra content that does not fit in the box.
     - **scroll**:This property adds a scrollbar to box so that users can scroll to see the missing content.
* The border-width property is used to control the width of a border. The value of this property can either be given in pixels or using one of the following values:
          - thin
          - medium
          - thick
* The border style properties specify the line style of a box's border.[Syntax] : (border-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset)
![image](https://www.w3.org/wiki/images/a/af/Cssed_borderstyles.png)
* The border color properties specify the color of a box's border.([Syntax] :border-color: < color >)
* The border property allows you to specify the width, style and color of a border in one property (and the values should be coded in that specific order).
* The padding property allows to specify how much space should appear between the content of an element and its border.
* The margin property controls the gap between boxes. Its value is commonly given in pixels, although you may also use percentage or ems.
* To center a box on the page (or center it inside the element that it sits in), you can set the left-margin and right-margin to auto.
* The display property of an object determines how it is rendered by the browser.[syntax] : display : 
    1. block
    2. inline
    3. none
    4. contents
    5. flow
    6. flow-root
    7. table (and all the table-* ones)
    8. flex
    9. grid
    10. list-item
    11. inline-block
    12. inline-table
    13. inline-flex
    14. inline-grid
    15. inline-list-item

* The visibility property allows you to hide boxes from users but It leaves a space where the element would have been. This property can take two  values:
    1. hidden :This hides the element.
    2. visible :This shows the element.
* The border-image property applies an image to the border of any box. It takes a background image and slices it into nine pieces.
* The box-shadow property allows you to add a drop shadow around a box.
* CSS3 introduces the ability to create rounded corners on any box, using a property called border-radius. The value indicates the size of the radius in pixels.

## Arrays in Javascript :
* The**array** is a special type of variable, which can store multiple values using special syntax. Every value is associated with numeric index starting with 0. 
  ![image2](https://www.tutorialsteacher.com/Content/images/js/js-array.png)
  * An array in JavaScript can be defined and initialized in two ways, **array literal** and **Array constructor** syntax.
  * Array literal syntax is simple. It takes a list of values separated by a comma and enclosed in square brackets.
      - Syntax: var < array-name > = [element0, element1, element2,... elementN];
  * JavaScript array can store multiple element of different data types. It is not required to store value of same data type in an array.
  * The Array constructor has following three forms.
    - Syntax: 

          * var arrayName = new Array();

          * var arrayName = new Array(Number length);

          * var arrayName = new Array(element1, element2, element3,... elementN);

  * Array includes length property and various methods to operate on array objects.

  ## Decisions and Loops:
  * A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.
  ![image](https://www.tutorialspoint.com/javascript/images/switch_case.jpg)
  * JavaScript can convert data types behind the scenes to complete an operation. This is known as **type coercion**
  * Due to type coercion, every value in JavaScript can be treated as if it were true or false; and this has some interesting side effects.
  * Falsy values are treated as if they are false. Falsy values can also be treated as the number 0 .
  * Truthy values are treated as if they are true.Truthy va lues can also be treated as the number 1.
  * Because the presence of an object or array can be considered truthy, it is often used to check for the existence of an element within a page.
  * Logical operators are processed left to right. They short-circuit (stop) as soon as they have a result - but they return the value that stopped the processing (not necessarily true or false).
  * Loops check a condition .if it returns true, a code block will run.Then the condition will be checked again and if it still returns true,the code block will run again .It repeats until the condition returns false.
- There are three types of loops:
  1. For ( to run the code specific number of times, the condition is counter).
  * The syntax of the for loop is:

for(initialExpression; condition; updateExpression) {
    // for loop body
}


   - The initialExpression initializes and/or declares variables and executes only once.
   - The condition is evaluated.
      + If the condition is false, the for loop is terminated.
      + if the condition is true, the block of code inside of the for loop is executed.
   - The updateExpression updates the value of initialExpression when the condition is true.
   - The condition is evaluated again.This process continues until the condition is false.
  ![for](https://cdn.programiz.com/sites/tutorial2program/files/javascript-for-loop.png)

  2. While (the code will continue to loop for as long as the condition is true)
  The syntax of the while loop is:
while (condition) {
    // body of loop
}


   - A while loop evaluates the condition inside the parenthesis ().
   - If the condition evaluates to true, the code inside the while loop is executed.
   - The condition is evaluated again.
   - This process continues until the condition is false.
   -  When the condition evaluates to false, the loop stops.
  ![while](https://cdn.programiz.com/sites/tutorial2program/files/javascript-while-loop.png)
  3. Do while (it will always run the statement inside the curly braces at least once even the condition evaluates to false .
  ![do while](https://cdn.programiz.com/sites/tutorial2program/files/javascript-do-while-loop.png)
  
