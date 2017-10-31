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

## Instructions

The school newspaper is doing an article for tomorrow's edition on the financial benefits of Ford's new hybrid cars. Unfortunately, the lead researcher lost the log of all the driving miles! Now, they have no data and you're their last hope.

The team has driven their Ford Fusion Hybrid enough to know the miles per gallon info - **41 in the city and 43 on the highway**.

<img src="https://upload.wikimedia.org/wikipedia/commons/0/04/Ford_Fusion_Hybrid_WAS_2017_1650.jpg" alt="Ford Fusion Hybrid" style="width: 200px; height: 200px"/>

They've asked you to build a `moneySaver` function. This function should take students' current info and calculate the amount of money spent on gas. Then it should compare that to the 2017 Ford Fusion Hybrid.

This will test your knowledge of using functions and arguments. Be conscious about what input each function takes and what output it returns.

Three case studies have been designed to demonstrate the efficiency of hybrid vehicles. Look over each student's information and design your function to address each situation.

Here's your info:

  + **Kayla** is a high school senior getting ready for college. Driving to college means 20 miles a day on the highway, and 3 miles a day in the city. Kayla's school is in session for only 150 days each year, and she takes the bus when school is out. Her Ford Escape gets **23 mpg** in the city and **31 mpg** on the highway.
  
  + **Paola** is a junior who loves cars. Her afternoon, ocean-side joyrides put her at an average of 50 miles a day in the city, and 15 on the highway. She also needs to drive 6 miles a day to get to and from school 180 days of the year. Her Ford Mustang gets **21 mpg** in the city and **30 mpg** on the highway.
  
  + **Mariah** is a senior who just got her license. She's taking a year off to roadtrip around the country and will be driving an average of 110 miles a day on the highway. Her Ford Explorer gets **19 mpg** in the city and **27 mpg** on the highway.

## Goal:
Calculate the yearly savings in gas each of these students can expect by driving the **Ford Fusion Hybrid**.

Use the tests as a guide!

## Resources

* [MDN - For Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)
* [MDN - While Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)
