# Protocol Extension

## Introduction
Welcome to Lesson 2 of The UIKIt Fundamentals Part 1 Intro to Protocol Oriented Programming. Today, you are going to learn a magic. It will dramatically reduce the number of lines by... so much. It's just incredible. I don't need to talk much. Let's dive in.

## Lecture Notes
### Problem
I don't even want to type anymore.

### Create Protocol
Create a protocol called `MathGenius` that contains one method.

```swift
protocol MathGenius {
  func calculateGPA()
}
```

### Create Protocol Extension
Create an extension to `MathGenius`. The extension contains a default method.

```swift
extension MathGenius {
  func calculateGPA() {
    print("I'm too cool for school")
  }
}
```

Create a struct that conforms to `MathGenius`. Since the extension provides a default method, you no longer have to specify the required method. If you do, it will override the default method.
```swift
struct Bob: MathGenius {
  // Override
}

Bob().calculateGPA() // "I'm too cool for school"

struct Bobby: MathGenius {}
Bobby().calculateGPA() // "I'm too cool for school"
Bobby.init() // Same as calling Bobby()
```

### Practical Protocol Extension
Create a protocol that contains a method that takes two `Double` parameters and return `String`.

```swift
protocol FindAreable {
  func calculateArea(side: Double, length: Double) -> String
}
```

Create an extension to `FindAreable` which will return a statement whose type is in `String`.

```swift
extension FindAreable {

  func calculateArea(side: Double, length: Double) -> String {
    let area = String(side * length)
     return "The area is \(area)"
  }
}
```

Every struct and class that conforms to `FindArea` contains the default `calculateArea` method from the extension.

```swift
struct Square: FindAreable {}

Square.init().calculateArea(side: 4, length: 100)

let bigSquare = Square.init()
bigSquare.calculateArea(side: 100, length: 20)

struct Hexagon: FindAreable {}
Hexagon().calculateArea(side: 6, length: 20)
```

### Usage Case
UIAnimation.

### Resources
If you are interested in how you may apply Protocol to UIKit, you may read [Protocol Oriented View with Bob (Blog)](https://medium.com/ios-geek-community/protocol-oriented-programming-view-in-swift-3-8bcb3305c427#.u3rr936vm). But, I plan to cover in Part 2. So, you may get head started.

### Source Code
[1402_Protocol Extension](https://www.dropbox.com/sh/qw9qw6z5ygyayz3/AAAkhxvYyAv1JFbyNd8UEGj_a?dl=0)



## Conclusion
Wow... All I can say is, wow. Protocol Oriented Programming is only limited by your imagination. It's really up to you how you can start using it. If you've ever done coding before or you are going to, take a moment, and really imagine and visualize how Protocol Oriented Programming can be applied. In this course, I'm not here to feed you. It's your job to pick up these skills that I present, and you apply, not me. Keep developing your skills, and you will be even surprised by the next level. Let's go.

#### Stay Connected
If you'd like to be on my mailing list and receive personal updates on upcoming books and courses, feel free to send me an email at `bobleesj@gmail.com`
<p>
<a href="http://bobthedeveloper.io"><img src="https://img.shields.io/badge/Personal-Website-333333.svg"></a>
<a href="https://facebook.com/bobthedeveloper"><img src="https://img.shields.io/badge/Facebook-Like-3B5998.svg"></a> <a href="https://youtube.com/bobthedeveloper"><img src="https://img.shields.io/badge/YouTube-Subscribe-CE1312.svg"</a> <a href="https://twitter.com/bobleesj"><img src="https://img.shields.io/badge/Twitter-Follow-55ACEE.svg"></a> <a href="https://instagram.com/bobthedev
"><img src="https://img.shields.io/badge/Instagram-Follow-BB2F92.svg"></a> <a href="https://linkedin.com/in/bobleesj"><img src= "https://img.shields.io/badge/LinkedIn-Connect-0077B5.svg"></a>
<a href="https://medium.com/@bobleesj"><img src="https://img.shields.io/badge/Medium-Read-00AB6C.svg"/></a>
</p>
