Download Link: https://assignmentchef.com/product/solved-cinf362-week-9-js-part-ii
<br>
<h1></h1>

<strong>Agenda</strong>

<ul>

 <li>Introduction to JavaScript

  <ul>

   <li>More JS Concepts

    <ul>

     <li>Variable Scope</li>

     <li>Arrays</li>

     <li>Objects</li>

    </ul></li>

   <li>Class Example</li>

   <li>JS Challenges 2</li>

  </ul></li>

 <li>Next Week</li>

</ul>




<h2>More JS Concepts</h2>

<strong>Variable Scope</strong>

In JavaScript, there are two major types of scopes for variables, local and global. Global variables are ones declared outside of functions while local variables are declared inside of functions. The difference is that global variables can be accessed anywhere in the document. Local variables can only be manipulated inside of their function. In the example below, x is a global variable and y is local to “myFunction()”…this means we can use the x value in and outside of the function. However, we can only refer to y inside of the function it was created in.




var x = 5; // Globally declared x variable

var myFunction = function() {

var y = 4; // Locally declared y variable

console.log(x); // X can be accessed inside this function

}

myFunction(); // Produces output

console.log(y); // Will cause an error because y is only defined inside of myFunction

<strong> </strong>

There is also <strong>block scope</strong> which is when a variable is declared inside of a block of code. If that same variable name exists as a global variable, changing its value inside of a block will change the value of the global variable. In the example below, we declare x to be 5 and log it to the console. After that, we check to see if x is greater than 0, if it is, we redeclare it to be 4.




var x = 5;

console.log(x); // Will log 5

if (x &gt; 0) {

var x = 4; // Redeclare our variable

}

console.log(x); // Will log 4 since the value has been changed




Sometimes this is what we want, however, there are cases where we want to use the same variable name inside of a block of code without changing the value of the global variable. We can do that by using the <strong>let </strong>keyboard. Instead of using var x = 4, we can use let x = 4.

var x = 5;

console.log(x); // Will log 5

if (x &gt; 0) {

let x = 4; // Declare our variable using <strong>let</strong> instead of <strong>var</strong>

}

console.log(x); // Will log 5 this time since using let doesn’t affect our global variable.




In the example above, I used let instead of var to declare a variable. As such, the global variable isn’t affected even though I used the same variable name. For the most part, we will deal with function/global variables and won’t need let but it’s a good thing to understand.




<strong>Arrays</strong>

These are essentially lists of any kinds of data (which can include other arrays). These data pieces are separated by commas and placed inside of square brackets. Every item inside of an array has an index number which is used to refer to that item. For example, we might have an array of house pets:




var housePets = [];




The one above is empty and has nothing in it.




var housePets = [‘cat’, ‘dog’, ‘bird’, ‘chinchilla’]




The above array has <strong>four</strong> items, but the index number only goes up to <strong>three.</strong> This is because the first item in any array has an index number of 0. The values are listed below:




housePets[0]; // Refers to cat

housePets[1]; // dog

housePets[2]; // bird

housePets[3]; // chinchilla




You can change values at any point by referring to the item and then assigning it a new value:




housePet[3] = “fish”;




The array would now be housePets[‘cat’, ‘dog’, ‘bird’, ‘fish’]




Like strings, arrays have their own set of methods/functions which can be used on them.




Using housePets.length; would produce 4 for our case.




We can also use things like pop() or push() to remove or add items to our array.




housePets.pop(); // Removes last item in our array – becomes cat, dog, bird

housePets.push(‘cow’); // Adds cow to the end of our array – becomes cat, dog, bird, cow




<strong> </strong>

<strong>Objects</strong>

These are things in JS that have their own properties and methods which can be called upon using something called <strong>dot syntax</strong>.




For example, if you have a car, that car has multiple characteristics and things it can perform. We can create an object for a car with the following code:




var myCar = {

name: “Herbie”;

owner: “none”;

age: 57;

honk: function() {alert(“HONK HONK!”);}

};




All you need to do is say var variableName = {} and place all methods/properties inside of the curly brackets. Name, owner, and age are all properties while honk is a method. We separate these with a colon but refer to them as key/value pairs. To get these values and use them, we use <strong>dot syntax</strong> which utilizes a period and the property/method name.




console.log(myCar.name); // Refers to the name key but logs the value “Herbie” to the console

myCar.honk(); // Would cause an alert to appear with “HONK HONK!”

myCar.age; // Refers to the age key and the value of 57




Objects in JS are powerful because almost everything is an object of some sort. Arrays, strings, and other types all have their own properties or methods (length, concat, push, pop, splice, etc.).




<u>Additional Reading</u>

<ul>

 <li><a href="https://www.w3schools.com/js/js_let.asp">https://www.w3schools.com/js/js_let.asp</a> (Let vs var)</li>

 <li><a href="https://css-tricks.com/javascript-scope-closures/">https://css-tricks.com/javascript-scope-closures/</a> (Only up to “function hoisting”, this goes very in-depth)</li>

 <li><a href="https://www.htmldog.com/guides/javascript/beginner/arrays/">https://www.htmldog.com/guides/javascript/beginner/arrays/</a> (Arrays)</li>

 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array</a> (Array Methods – ignore let for now)</li>

 <li><a href="https://www.htmldog.com/guides/javascript/beginner/objects/">https://www.htmldog.com/guides/javascript/beginner/objects/</a> (Objects)</li>

 <li><a href="https://www.geeksforgeeks.org/objects-in-javascript/">https://www.geeksforgeeks.org/objects-in-javascript/</a> (More Objects)</li>

</ul>

<strong><u> </u></strong>

<strong><u>Class Examples:</u></strong>

<a href="https://iinf362.000webhostapp.com/examples/">https://iinf362.000webhostapp.com/examples/</a> (All examples for the course)

<a href="http://iinf362.000webhostapp.com/examples/javascript-part-2/">http://iinf362.000webhostapp.com/examples/javascript-part-2/</a> (This week’s example)

Right-click this page in order to view the page source. I’ve left comments throughout the JavaScript to help you understand what is going on. These examples will help you with the challenges for this week’s assignment.




<strong><u>If you haven’t done so already, please read the “Creating and Viewing our Web Pages.docx” file on Blackboard. You will not be able to submit anything for the assignment without completing that portion first. </u></strong>




<strong>JS Challenges 2</strong>

Download the “JS-Challenges-2.zip” folder from Blackboard under the Lecture Notes for this week or in the Assignments folder. Inside of this zip folder, you’ll find an HTML file, a js folder, and a script.js file. Using these files, your task is to add JS to complete the challenges as they are described in the HTML file. In total, there are 4 main challenges. Feel free to reference the class example code as it has items that will directly help you with this assignment. Also, the very last slide of the JavaScript PowerPoint slides on Blackboard has a video which depicts how the output/results should be for this assignment. Feel free to watch it for assistance. If the download is too big (roughly 70MB), please let me know.

<u> </u>

To receive credit for these challenges, submit a link to your JS Challenges 2 page by <u>Wednesday, April 1<sup>st</sup> at midnight</u>. The assignment with be called JS Challenges 2 in the assignments folder. It will also be accessible through the Lecture Notes for this week.