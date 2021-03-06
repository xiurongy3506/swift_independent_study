# Entry 2: Dive into the Learning

In this blog, I will cover mostly the notes I took from watching Swift Tutorial on youtube and the basic syntax. Feel free to scroll down to the bottom and check out CocoaPods, App Tinkering, and Takeaways. 

## Variables
As mentioned in my Blog Entry1, a variable holds data. By giving variables a specific type, i.e `var str:String`, it is telling the computer that the variable, str, only stores string data. 

**Note**: An error will occur if `var str:String = 4` as well as `var str:int = “hello playground”`

| Syntax      | Examples  |
| ----------- | ----------- | 
|`var variable name: type = expression` | `var c:Float = 2.3`<br> `var d:Double = 13.9` <br>`var e:Bool = true`|

## If, Else if, Else statement
Like most of the computer languages I've learned, the If, Else if, and Else statements are conditionals going in order. If conditional1 is true, it will execute the code that is under conditional1. If condition1 is not true, it will go down the loop and execute the code with the true condition.

```swift
if condition1 {
	Somecode
}
else if condition 2 {
	Code
}
else {
	Code
}
```

**Notes:**  _Equal Sign_ `==` _And_ `&&` _Or_ `||`  _Not_ `!=`

## Switch Statement
Switch Statements are similar to If Else Statements, except, they are easier to read than writing a bunch of if else statement (reminds me case statement in Ruby).

**Syntax**
```swift
switch value to consider{
	case value1: 
		some code
	case value2:
		some code
	default: 
		somecode
}
```

**Example**
```swift
var someCharacter:Character = "a"

switch someCharacter {
    case "a":
        print("is an A")
    case "b", "c":
        print("is a B or C")
    default:
        print("some fallback")
}
```
This will print “is an A”

## loops
Loops are instructions that are repeated until a certain condition is met. 

### For Loop
**Syntax** 
```swift
for counter in Lower…upper{
	some code
}
```

**Example**
```swift
var sum = 0
for index in 1...5 {
//print hello 5 times
//    print("hello")
//print from 1 to 5
//    print(index)
    sum += index
}
print(sum)
```

### While Loop 
**Syntax**
```swift
while condition {
    some code
}
```

**Example**  
```swift
var num = 6
while num < 4 {
    print("This runs when the above stement is true")
}
```

In this case, the condition is not true, so the while loop will not run. If the statement is true, it will run and run and create an **infinite loop** since nothing is there to break the loop. 

You can add **break** below print to make the code only run once.  

### Repeat While Loop 
**Syntax**
```swift
repeat {
    some code
}while condition
```

**Example**
```swift
var num = 6
repeat {
    print("This will always run once")
}while num < 5
```

Above will print <code>This will always run once</code>

#### :star: Order Matters
The order of the code can be seen through **the difference between Repeat While Loop and While Loop**. 

Repeat prints once and then check for the while condition. However, while loop will not repeat at all if the condition is not met.

## Functions
A function is a block of code that you can call multiple times.  

**Syntax**  
```swift
func name() {
    some code
}
```

:star: **Return Values**
```swift
func name() -> DataType {
    some code
    return someValue
}
```

:star: **parameter**
```swift
func name (argumentLabel parameterName:DataType) {
    some code
}
```

:star: **Multiple Parameters**
```swift
func name (arg1 param1:DataType, arg2 param2:DataType) {
    some code
}
```

**Example**
```swift
func addTwoNumbers(arg1 para1:Int, arg2 para2:Int) -> Int{
    return para + para2
}
let sum = addTwoNumbers(arg: 2, arg2: 3)
print(sum)
```

Above will print <code>5</code> because the function is adding the two parameters the user assign in <code>arg</code>.   

This code can look a bit overwhelming because you have to assign four different names that you will use, two parameters (to use within the function) and two arguments (to use outside of the function). Imagine if you were to add more parameters...

#### Ways you can make the above code simpler  
:star: **Make arg and para name the same**
```swift
func addTwoNumbers(para1:Int, para2:Int) -> Int{
    return para + para2
}

let sum = addTwoNumbers(para1: 2, para2: 3)
print(sum)
``` 

:star: **Easier to read**  
```swift
func addTwoNumbers(using para:Int, and para2:Int) -> Int{
    return para + para2
}

let sum = addTwoNumbers(using: 2, and: 3)
print(sum)
```

:star: **Don't want to use labels at all?**  
```swift
func addTwoNumbers(_ para:Int, _ para2:Int) -> Int{
    return para + para2
}

let sum = addTwoNumbers(2,3)
print(sum)
```

## CocoaPods
#### Where did this new concept, CocoaPods, came from? 
I told my co-worker, John, at my intern that I will be studying Swift for my independent_study. John, as an IOS Developer, asked me about what I am learning, and I told him about my experience of swift so far (learning the basics syntax and etc). I told John about my goal, to build a productivity app, and John kindly recommended me to look into CocoaPods as it contains many already developed code that can be useful to implement in my app. 

#### So I did some googling...  
CocoaPod is a dependency manager for Swift and Objective-C. 

In other words, CocoaPods allows you to import external libraries into your projects. A **pod** is referencing to a software library. Once it is installed on your computer, you can use it in your projects.

John showed me how to install, and here is the process
1. Open up the terminal  
2. cd into the cocoapods folder  
3. <code>pod init</code>  
4. <code>sudo gem install cocoapods</code>


Once installed, John used Alamofire, has to do with networking and API, as an example to help me set up.   
1. Add Alamofire to podfile (detail can be seen in the installation guide [here](https://cocoapods.org/pods/Alamofire) )
2. On the terminal, <code>pod install</code>   
    <img src="https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/cocoapod_install.png" width= "100%"/>
3. Once installed, the folder Alamofire will be created  
4. Import Alamofire on view controller  
 
Introduced to CocoaPods for the first time, I did some research and had a gist of what CocoaPods is. However, to implement it in swift, I still need to dive in deeper and watch more tutorials on how to use CocoaPods. Hopefully, I will do that next week and update what I learn on my next entry!

## App Tinkering
Thanks to John, he also gave me quick an overview on how apps work in swift and how to program them. 

#### What I learned
1. To code for a specific item in the storyboard, you would click and drag that item to where you want to place the code in ViewController.swift
2. A little box will pop up (shown below), and you can fill in the corresponding action.  
    <p align="center">
    <img src="https://raw.githubusercontent.com/xiurongy3506    /swift_independent_study/master/img/box.png" width=     "40%"/>
    </p>
3. Then, in the function, I can apply swift code. 

<p align="center">
    <b>A demo of what I did: Button Clicked</b><br>
    <img src="https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/button_click.gif" width= "60%"/>
</p>

_Above is a continuation of the previous app I created in Entry 1._

## Takeaways
1. **Follow the path of serendipity.** I currently work at a startup digital marketing app company, and I shared about my experience in coding and what I am currently working on with my co-workers. This leads me to help and advice from my co-worker, John, and expanded my understanding of the app platform. Overall, this gave me a balance to play around with Xcode and to continue learning the syntax on Swift Tutorial.

2. **Know how to pace your learning.**  I made sure that I watch at least one unit per day and practice using it either through code along with the youtube video or trying something on the playground (see previous entry if you do not know what a playground is). This way, I will make sure I know the basics and will dive a little into the app each time.






