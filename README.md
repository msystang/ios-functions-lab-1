# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1 DONE

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {

}
```
Answer:
```swfit
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax(calculateTaxOf cost:Double) -> Double {
let costWithTax = cost + cost*nyTax
return costWithTax
}

totalWithTax(calculateTaxOf: itemCost)

let totalCost = Int(totalWithTax(calculateTaxOf: itemCost))
print(totalCost)
```

Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"

## Question 2 DONE

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```
Answer:
```swift
let todaysTemperature = 72
var forecast: String = ""

func tellMeTheTemperature(forecastOfTemp temp:Int) -> String {
if temp <= 40 {
forecast = "It's cold out."
} else if temp >= 85 {
forecast = "It's really warm."
} else {
forecast = "Weather is moderate."
}
return forecast
}

let todaysForecast = tellMeTheTemperature(forecastOfTemp: todaysTemperature)
print(todaysForecast)
```

## Question 3 DONE

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`

Answer:
```swift
var smallestNumber = 0

func min2(a: Int, b: Int) -> Int {
if a < b {
smallestNumber = a
} else {
smallestNumber = b
}
return smallestNumber
}

print(min2(a: 1, b: 2))
```

## Question 4 DONE

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`

Answer:
```swift
func lastDigit(_ number: Int) -> Int {
let lastDigitOfNum = number % 10
return lastDigitOfNum
}

print(lastDigit(12345))
```

## Question 5 DONE

Write a function that takes in any two positive integers and return the sum.

Answer:
```swift
func takesSumOfTwoInts(sumOf a: Int, b: Int) -> Int {
return a + b
}

let sumOf5And9 = takesSumOfTwoInts(sumOf: 5, b: 9)
print(sumOf5And9)
```

## Question 6 DONE

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |

Answer:
```swift
var grade: String = ""

func giveMeLetterGrade(LetterGradeFor score:Int) -> String {
if score == 100 {
grade = "A+"
} else if score >= 90 && score <= 99 {
grade = "A"
} else if score >= 80 && score <= 89 {
grade = "B"
} else if score >= 70 && score <= 79 {
grade = "C"
} else if score >= 65 && score <= 69 {
grade = "D"
} else {
grade = "F"
}
return grade
}

print(giveMeLetterGrade(LetterGradeFor: 90))
```

## Question 7 DONE

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.

Operator parameter: (+, -, x, /)

Answer:
```swift
var answer = 0

func calculator(_ num1: Int, op: Character, num2: Int) -> Int {
if op == "+" {
answer = num1 + num2
} else if op == "-" {
answer = num1 - num2
} else if op == "x" {
answer = num1*num2
} else if op == "/" {
answer = num1/num2
} else {
answer = 0
}
return answer
}

calculator(3, op: "x", num2: 2)
```

## Question 8 DONE

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

//Write your code below

let myFinalCost = totalWithTip() //Fill in the arguments
```

Answer:
```swift
let mealCost = 45
let tipPercentage = 0.15

func totalWithTip(calculatesCostOf cost: Int, tip: Double) -> Double {
let costWithTip = Double(cost) + Double(cost)*tip
return costWithTip
}

let myFinalCost = totalWithTip(calculatesCostOf: mealCost, tip: tipPercentage)
print(myFinalCost)
```


Write a function that will print out **total cost after tip and tax.**

```swift
let taxPercentage = 0.09

//Write your code below

let myFinalCostWithTipAndTax = totalWithTipAndTax() //Fill in the arguments in function
```
Answer:
```swift
let mealCost = 45
let tipPercentage = 0.15
let taxPercentage = 0.09

func totalWithTipAndTax(calculatesCostOf cost: Int, tip: Double, tax: Double) -> Double {
let costWithTipAndTax = Double(cost) + Double(cost)*tip + Double(cost)*tax
return costWithTipAndTax
}

let myFinalCostWithTipAndTax = totalWithTipAndTax(calculatesCostOf: mealCost, tip: tipPercentage, tax: taxPercentage)
print(myFinalCostWithTipAndTax)
```

## Question 9 DONE

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`

Answer:
```swift
func repeatPrint(repeats message:String, count:Int) {
for _ in 1...count {
print(message, terminator: "")
}
}

repeatPrint(repeats: "+", count: 10)
```

## Question 10 DONE

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`

Answer:
```swift
func first(n:Int) -> Array<Int> {
var array = [Int]()
for i in 1...n {
array.append(i)
}
return array
}

print(first(n: 3))
```

## Question 11 DONE

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)

Answer:
```swift
func countFizzBuzz(x:Int) {
if x % 3 == 0 {
print("Fizz")
} else if x % 5 == 0 {
print("Buzz")
} else if x % 3 == 0 && x % 5 == 0 {
print("FizzBuzz")
} else {
for i in 1...x {
print(i, terminator: "")
}
}
}

countFizzBuzz(x: 6)
```

## Question 12 DONE

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`

Answer:
```swift
func reverse(numbers: Array<Int>) -> Array<Int> {
let revNums: [Int] = numbers.reversed()
return revNums
}

reverse(numbers: [1, 2, 3])
```



## Question 13***

Write a function that prints out the most frequently appearing Int in an array of Int.

Answer: (Not sure why the answer does not print)
```swift
func findMostFreq(mostFreqFor array: Array<Int>) {

var freqDict: [Int:Int] = [:]

for num in array {
if freqDict.keys.contains(num) {
freqDict.updateValue(freqDict[num]!+1, forKey: num)
} else {
freqDict[num] = 1
}
}

let highestFreq = freqDict.values.max()

for (key, value) in freqDict {
if freqDict[value] == highestFreq {
print(freqDict[key]!)
}
}
}
findMostFreq(mostFreqFor:[3,2,15,5,2,21,2,2,2])
```

## Question 14 DONE

Write a function that sums all the even indices of an array of Ints.

Answer:
```swift
func findSumofEvenIndices(array: Array<Int>) -> Int {
var sum = 0
for (index, int) in array.enumerated() {
if index % 2 == 0 {
sum += int
}
}
return sum
}

print(findSumofEvenIndices(array: [2,4,2,15,6,2]))
```

## Question 15***

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`


## Question 16***

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

## Question 17 DONE

Write a function that determines if a value is inside of array.

Answer:
```swift
func tellsIfInArray(array: Array<Int>, num: Int) -> Bool {
let output = array.contains(num)
return output
}

tellsIfInArray(array: [1,2,3,4,5], num: 3)
```

## Question 18 DONE

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`

Answer:
```swift
let dieRoll = Int(arc4random_uniform(6) + 1)

func tellsEvenOrOdd(n: Int) -> Bool {
if n % 2 == 0 {
return true
} else {
return false
}
}
print(tellsEvenOrOdd(n: dieRoll))
```

## Question 19 DONE

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.

Answer pt. 1 & 2:
```swift
//Write a function that takes `[Int]` as input. It should return the largest Int in the array.

func givesLargestInt(array: Array<Int>) -> Int {
let sortedArray = array.sorted()
let largestInt = sortedArray[array.count-1]
return largestInt
}

let largestInt = givesLargestInt(array: [1,3,5,7,2,23,35,2])
print(largestInt)

//Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

print("The largest Int in my array is \(largestInt).")

```

Answer pt. 3:
```swift
let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]

func givesLargestInt(array: Array<Int>) -> Int {
let sortedArray = array.sorted()
let largestInt = sortedArray[array.count-1]
return largestInt
}

let largestInt = givesLargestInt(array: myArray)


func tellsEvenOrOdd(n: Int) -> String {
if n % 2 == 0 {
return "Even"
} else {
return "False"
}
}

let evenOrOdd = tellsEvenOrOdd(n: largestInt)

print("The largest Int in 'myArray' is \(largestInt) and it is \(evenOrOdd).")
```

## Question 20 DONE

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`

Answer:
```swift
let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."

func givesNumberOfCharacters(string:String) -> Int {
return string.count
}

givesNumberOfCharacters(string: myString)

//or

let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."

func givesNumberOfCharacters(string:String) -> Int {
var counter = 0
for _ in string {
counter += 1
}
return counter
}

givesNumberOfCharacters(string: myString)
```

## Question 21 DONE

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"
```

Sample output: `3`

Answer:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"

func givesNumberOfMatchingChars(string:String, char:Character) -> Int {
var counter = 0
for letter in string {
if letter == char {
counter += 1
}
}
return counter
}

print(givesNumberOfMatchingChars(string: testString, char:targetCharacter))
```

## Question 22***

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]
```

Output: `13`




## Question 23***

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.


## Question 24***

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`

Output: `93`

## Question 25***

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`


## Question 26 DONE

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`

Answer:
```swift
func filterOdd(arr: Array<Int>) -> Array<Int> {
var evenArray = [Int]()
for num in arr {
if num % 2 == 0 {
evenArray.append(num)
}
}
return evenArray
}

print(filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8]))
```

## Question 27 DONE

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`


Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.

Example:
Input:  `multiplyIt(arr: [1, 2, 3, 4], n: 4)`

Output:  `[4, 8, 12, 16]`

Answer:
```swift
//Part 1
func doubleIt(arr: Array<Int>) -> Array<Int> {
var doubleArray = [Int]()
for num in arr {
doubleArray.append(num*2)
}
return doubleArray
}
doubleIt(arr: [1, 2, 3, 4])


//Part 2
func multiplyIt(arr: Array<Int>, n: Int) -> Array<Int> {
var multArray = [Int]()
for num in arr {
multArray.append(num*n)
}
return multArray
}

multiplyIt(arr: [1, 2, 3, 4], n: 4)
```

## Question 28 DONE

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`

Answer:
```swift
func unwrap(arr: Array<Int?>) -> Array<Int> {
var unwrappedArray = [Int]()
for int in arr {
if int != nil {
if let intUnwrapped = int {
unwrappedArray.append((intUnwrapped))
}
}
}
return unwrappedArray
}

unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])
```

## Question 29***

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`


## Question 30****

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`


## Question 31***

Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`


## Question 32 DONE

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)

Answer:
```swift
func checksIfPalindrome(string: String) -> Bool {
var stringRev = ""
for char in string {
stringRev = String(char) + stringRev
}
return stringRev == string
}
checksIfPalindrome(string: "mom")
```

## Question 33

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)


## Question 34

Write your own `min()` and `max()` functions for an Array of Ints


## Question 35 DONE

Given two arrays of Ints, write a function that tells you all the values they have in common.

Answer:
```swift
func findCommonValues(arr1: Array<Int>, arr2: Array<Int>) -> Set<Int> {
let arr1Set = Set(arr1)
let arr2Set = Set(arr2)
let commonValues: Set<Int> = arr1Set.intersection(arr2Set)
return commonValues
}
findCommonValues(arr1: [1,2,3,4,5], arr2: [3,4,5,6,7,8])
```

## Question 36

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.


## Question 37

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`
