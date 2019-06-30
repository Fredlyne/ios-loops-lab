# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

***
let somRange = 1...150

for i in somRange {
print(i)
}


## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

let somRange = 1..<159

for i in somRange {
print(i)
}

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

let somRange = 15..<80

for i in somRange where i % 2 == 0 {
print(i)
}
***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

let somRange = 19..<51

for i in somRange where i % 2 == 1 {
print(i)
}
***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**


let somRange = 1..<100

for i in somRange where i % 10 == 5 {
print(i)
}



***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

let setRange = 1...40

for i in setRange where i % 10 == 7 {
print (i)
}

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

let setRange = 20...150

for i in setRange where i % 3 == 0 {
print (i)
}
***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

let setRange = 20...150

for i in setRange where i % 2 == 0 && i % 3 == 0 {
print (i)
}


***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

let setRange = 20...150

for i in setRange where i % 10 == 4 {
print (i)
}
***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

let setRange = 20...150

for i in setRange {
if i == 31 || i == 35 || i >= 40 && i <= 60 {
print (i)
}
}

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// It will run an infinite amount of times because 5 is greater than 3 and the outputs will all be greater than 5   
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i > 3 && i < 9) {
    i += 1
    print(i)
} 

OR

while (i < 9) {
i += 1
print(i)
}

```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// edited to below
var i = 5

while (i > 3) {
i += 1
print(i)
if i >= 1005 {
break
}
}


```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}

var i = 5

while (i > 3) {
i += 1
if i >= 1005  {
break
}
if i % 2 == 0 {
print(i)
}
}

```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10

No their outputs will not be different (in this case). The only differences between the two codes is the placement of the condition and that the repeat function will run the code even if the condition isnt met but only the first time. Loop one sets the condition before the iteration while loop two runs the iteration with the condition at the end. 
```

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

```
The continue function will "continue" to run the loop and only skip over (so to speak) the iteration of whatever condition set in place. It continues on to the next iteration in the code (within parameters if there are any).

EX.
var i = 7

for i in 0...11 {
if i == 9 {
continue
}
print(i)
}


The break function will end the loop  IMMEDIATELY once the condition has been met in that exact iteration, it stops and moves on to the next code. 

EX.
var i = 7

for i in 0...11 {
if i == 9 {
break
}
print(i)
}

```
***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}

1
2
3
8
9
10
```

[]1
[]2
[]3
[]8
[]9
[]10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
1
2
3
```

[]1
[]2
[]3


***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}

x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

the iteration will run but once y encounters 2 the iteration will stop and continue in the next number of x 

```

***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.
```

for i in 0...10 {
for j in 0...10 {
print ("\(i),\(j)", separator: "", terminator:"  ")
}
print(" ")
}
```
***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.
```
for i in 0...10 {
for j in 0...10 {
if (i - j >= 5) || (j - i >= 5){
print ("\(i),\(j)", separator: "", terminator:"  ")
}
};print("")
}
```
***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25

var N = 5
var squaredNumber = 1

while squaredNumber <= N {
print(squaredNumber*squaredNumber)
squaredNumber = squaredNumber + 1
}

```

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**

var N = 2

for i in 1...N {
for i in 1...N {
print("*", terminator: "")
}
print("")
}
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***

```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

var N = 3

for i in 1...N {
for j in 1...N {
print("*", terminator: "")
}
print("")
}

***
