# JavaScript Loops

## Objectives
+ Explain the purpose of a loop
+ Build a while loop
+ Build a for loop
+ Explain the difference between each type of loop in JS

## Terminology to Look Out For
+ loop
+ condition
+ body
+ initialization
+ iteration

## About

Loops are used to execute the same block of code a specified number of times. 

This is a code-along, so follow along with the instructions in each section. There are tests to make sure you're coding your solutions correctly.

## The While Loop

The `while` loop is similar to an if statement, except that its body will keep executing until the condition evaluates to false. Here's how we write them:
  
#### Syntax

```javascript
while ([condition]) {
  [loopBody]
}
```

Every `while` loop has two statements:

- Condition
  + The expression that is evaluated each time the loop runs (every iteration). If the expression is `true`, the loopBody runs. If `false`, the loopBody does not run.
- LoopBody
  + The block of code that runs each time the condtion evaluates to `true`.


The while loop first checks to see if the condition is `true`. If it is, the code in the loopBody is run and the while loop starts over. If the condition is still true, the loop runs for another iteration. If the condition evaluates to `false`, then the loop stops.

A `while` loop is perfect for when you're not sure how many times the loop will run. 

#### Example

```javascript
var litersOfCoffeeNeeded = 1.000
var coffeeDrank = 0

while (coffeeDrank <= litersOfCoffeeNeeded) {
  coffeeDrank += 0.250
  console.log("Just drank 250 milliliters of coffee.")
}
```

The example shows a while loop that will run until the `coffeeDrank` variable is greater than or equal to `litersOfCoffeeNeeded`. Each time the loop runs, `0.25` is added to the `coffeeDrank` variable. Without this increment, the loop would run forever!

## The For Loop

The `for` loop is slightly more complex. The `while` loop has only a condition and loopBody, but the `for` loop has two additional statements to deal with.

When we need more control over how many times the loop should run, we use `for` loops.

In the `while` loop example, the `coffeeDrank` variable was first set to `0` outside the loop. The condition was then evaluated, and the `coffeeDrank` variable was incremented in the loop body.

The `for` loop combines all three of those steps like this:

#### Syntax

```javascript
for ( [initialization]; [condition]; [iteration] ) {
  [loopBody]
}
```
The additional initialization and iteration statements are as follows:

- Initialization
  + Usually an expression where the counter variable is created or assigned a value to start with. Ex. `var i = 0`.

- Iteration
  + The statement that runs at the end of each loop iteration. This is usually where the counter variable is incremened or decremented to cause an end to the loop.

#### Example

```javascript
console.log("Just got my new car and 100,000 mile warranty!")

for (var i = 1; i <= 365; i++) {
  console.log("I've had my car for " + i + "days!")
  console.log("I've now driven " + (i * 20) + " miles.")
}

// How many years of driving until the warranty expires?
```

The `for` loop is probably the most common loop and is usually the loop of choice for JavaScript programmers. 

## Itsa Me, Mario!

***This is a group lab, so make sure you are working in a group of 2-3 students***

Toward the beginning of World 1-1 in Nintendo’s Super Mario Brothers, Mario must hop over two "half-pyramids" of blocks as he heads toward a flag pole. Below is a screenshot.

![mario](http://prog1.mprog.nl/course/20%20Problem%20sets/10%201%20-%20Mario/pset13.png)

Your mission is to recreate these blocks using Javascript. 

### Part I: The Boring Pyramid
Create a program that will print the following pyramid:

```
   #  #
  ##  ##
 ###  ###
####  ####
```

(The height and the width of the half-pyramids pictured above are 4 with a gap of size 2 separating them.) 

### Part II: User Specified Height

Add a new feature to your program that asks a user how tall they would like to make the pyramid. This should be a non-negative integer no greater than 23 (this is the tallest that a pyramid can be in Mario land).

### Part III: Chained pyramids

Modify your code to prompt the user for the number of pyramids they want. Using this number, stack the pyramids on top of each other in a chain. This would be an example of a pyramid with height of 4 and chain length of 3:
```
   #  #
  ##  ##
 ###  ###
####  ####
   #  #
  ##  ##
 ###  ###
####  ####
   #  #
  ##  ##
 ###  ###
####  ####
```
### Part IV: Every-Other-Upside-Down Pyramid
Modify your code to make every other pyramid inverted. Example:
```
   #  #
  ##  ##
 ###  ###
####  ####
####  ####
 ###  ###
  ##  ##
   #  #
   #  #
  ##  ##
 ###  ###
####  ####
```



## Goal:
Calculate the yearly savings in gas each of these students can expect by driving the **Ford Fusion Hybrid**.

Use the tests as a guide!

## Resources

* [MDN - For Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)
* [MDN - While Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)
