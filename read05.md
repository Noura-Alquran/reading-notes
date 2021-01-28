# Reading 05 Summary
## Comparison operators:
 + Evaluating conditions:
   - You can evaluate a situation by comparing one value in the script to what you expect it might be .
   - The result will be a Boolean :

         1. True 
         2.  False 

+ ( == ) is equal to , it’s compare two values to see if they the same. 

+ ( != ) is not equal to, it’s compare two values to see if they not  the same .

+ (===) strict equal to , it’s compare two values to check that both the datatype and the value are the same .

+ (!==) strict not equal to, it’s compare two values to check that both the datatype and the value are not the same .

+ (>) greater than ,it checks if the number on the left is greater than the number on the right.

+ (<) less than , it checks if the number on the left is less than the number on the right . 

+ ( >=) greater than or equal to, it checks if the number on the left is greater than or equal to the number on the right.

+ (<=) less than or equal to, it checks if the number on the left is less than or equal to the number on the right .

## Logical operators:
 - Comparison operators usually return single values of true or false.While, logical operators allow you to compare the results of more than one comparison operator.
- (&&) logical and, it tests more than one condition.

- ( | | ) logical or , it tests at least one condition.

- ( ! ) logical not , it takes a single boolean value and inverts it .


 ![imageee](https://slideplayer.com/slide/15945194/88/images/25/Logical+Operators+%28cont.%29.jpg)

 >  short circuit evaluation: 
 Logical expressions are evaluated left to right .
If the first condition can provide enough information to get the answer, then there is no need to evaluate the second condition.

## Loops :
Loops check a condition .if it returns true, a code block will run.
Then the condition will be checked again and if it still returns true,the code block will run again .
It repeats until the condition returns false.
- There are three types of loops:
  1. For ( to run the code specific number of times, the condition is counter)
  ![for](https://cdn-media-1.freecodecamp.org/images/1*XJvkwoG4BLFnx6tpfzPZQQ.jpeg)

  2. While (the code will continue to loop for as long as the condition is true)
  ![while](https://media.geeksforgeeks.org/wp-content/uploads/20191118164726/While-Loop-GeeksforGeeks.jpg)
  3. Do while (it will always run the statement inside the curly braces at least once even the condition evaluates to false .
