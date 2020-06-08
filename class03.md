## HTML Lists, CSS Boxes, JS Control Flow

### Lists
HTML provides us with three different types:
1- Ordered lists are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number.
2- Unordered lists are lists that begin with a bullet point (rather than characters that indicate order).
3- Definition lists are made up of a set of terms along with the definitions for each of those terms.
*Lists can be nested inside one another.*


### Boxes

* Controlling size of boxes
- `width, height`

- `hidden`

This property simply hides any extra content that does not fit in the box.

- `scroll`
This property adds a scrollbar to the box so that users can scroll to see the missing content.

* Box model for borders, margin and padding

#### Border

Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.

#### Margin

Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.

#### Padding

Padding is the space between the border of a box and any content contained within it.
Adding padding can increase the readability of its contents.

Centering Content

body {
text-align: center;}
 It is possible to hide elements using the display and visibility properties.

 ## JS

 ### If statement 

 if ... else statements allow you to run one set of code if a condition is true, and another if it is false.

 #### switch statement
 
 It starts with a variable called the switch value. Each case indicates a possible
value for this variable and the code that should run if the variable matches that value.

You have a default option that is run if none of the cases match.
If a match is found, that code is run; then the break statement stops the rest of the switch statement running (providing better performance than multiple i f statements).

DATA TYPE PURPOSE
string >>> Text
number >>> Number
Boolean >>> true or false
nul  >>> Empty value
undefined >>> Variable has been declared but not yet assigned a value

### LOOPS

- FOR 
The loop starts with the for keyword, then contains the condition inside the parentheses.As long as the counter is less than the total number of items in the array, the contents of the curly braces will continue to run. Each time the loop runs, the round number is increased by 1.

- while
A more typical use of awhi le loop would be when you do not know how many times you want the code to run. It should continue to run as long as a condition is met