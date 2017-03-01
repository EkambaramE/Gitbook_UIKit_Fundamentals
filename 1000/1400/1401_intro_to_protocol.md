# Introduction to Protocol

## Introduction
Welcome to Lesson 1 of The UIKIt Fundamentals Part 1 Intro to Protocol Oriented Programming. Before I talk about details, I'd like to share with you that learning Protocol was such a daunting task. Not only it was located at the end of the Swift documentation, but it just felt really foreign to me. It sounded scary. Of course, it feels natural to use it, so I understand if you are not comfortable with it. I just would like to tell you that you might have to watch this video multiple times to get by. You might have to read 10 more articles for you to fully get comfortable. I really expect you guys to be proactive when you are confused. I will do my part which is to explain in the most clear way possible. Well, let's get started from the bottom with me. Let's go!

## Lecture Notes

There are certainly benefits of using OOP, but the opposites as well.
When you subclass, you have to inherit properties and methods which you may not need. Your object becomes unnecessarily bloated.
When you make a lot of super classes, it becomes extremely hard to navigate between each class and fix bugs/edit.
Since objects are referencing to the same place in memory, if you make a copy and create a small change its property, it can f up the rest. (Mutability due to reference)

### Problem
Problem: I don't know Protocol

> Protocol is like a basketball coach. He/she tells players what to do, but he/she doesn't know how to dunk.

### Protocol
Create a protocol called, `Rookieable`. It contains two properties and one method. Do not worry about `get` and `set` for now.

```swift
protocol Rookieable {
  var numberOfEXP: String { get set }
  var name: String { get }

  func introduce()
}
```

Create a class that conforms to `Rookieable` just like how you would subclass. To prevent Swift from screaming, you must implement two properties and one method defined in the protocol.

```swift
class Bob: Rookieable {
  // Stored property has no effect on get or set
  var numberOfEXP: String = "13"
  var name: String = "Bob"

  func introduce() {
    print("Hi, I'm \(name) and I have \(numberOfEXP) years of experience")
  }

}
```

Create an object and call the `introduce` method.
```swift
Bob().introduce()
```

> { get } or { get set} only apply to computed property. If you are defining a stored property, you may choose either { get } or { get set }.


### Computed Property
Create a protocol called, `Breathable`. It contains two properties: `isBreathing` and `isLiving`.

```swift
protocol Breathable {
  var isBreating: Bool { get set }
  var isLiving: Bool { get }
}
```

Create a struct that conforms to `Breathable`. The struct contains properties: `isBreathing` and `isLiving`. Define them as computed properties rather than stored.

```swift
struct Human: Breathable {
  var isBreating: Bool {
    get { return true }
    set { } // If no set, error occurs. isBreathing is { get set }
  }

  var isLiving: Bool {
    get { return true }
    set { }
  }

}
```

> **Rule:** If you are using a computer property, if it is { get } you may make a property gettable or settable. If it is defined as { get set } within a protocol, you must make it gettable and settable.

### Resources
### Source Code
[1401_Protocol Basics](https://www.dropbox.com/sh/n5y58kvek9zp1ef/AACvWcKQbmtclxYLxc3Qy8zAa?dl=0)

## Conclusion
Are you wrapping your heads around? Again, make sure you remember a couple rules. If you use { get } or { get set }. You can both use it as a stored property and change the value as you wish. However, if you identify a property with { get set } please remember if you use computed property, you have to make it settable as well. For { get }, you can do whatever you want. In our next lesson, you are going to see some of practical aspects of Protocol. You've only seen the tip of an ice berg. Let's get started my friend. Super excited to make you smarter.

#### Stay Connected
If you'd like to be on my mailing list and receive personal updates on upcoming books and courses, feel free to send me an email at `bobleesj@gmail.com`
<p>
<a href="http://bobthedeveloper.io"><img src="https://img.shields.io/badge/Personal-Website-333333.svg"></a>
<a href="https://facebook.com/bobthedeveloper"><img src="https://img.shields.io/badge/Facebook-Like-3B5998.svg"></a> <a href="https://youtube.com/bobthedeveloper"><img src="https://img.shields.io/badge/YouTube-Subscribe-CE1312.svg"</a> <a href="https://twitter.com/bobleesj"><img src="https://img.shields.io/badge/Twitter-Follow-55ACEE.svg"></a> <a href="https://instagram.com/bobthedev
"><img src="https://img.shields.io/badge/Instagram-Follow-BB2F92.svg"></a> <a href="https://linkedin.com/in/bobleesj"><img src= "https://img.shields.io/badge/LinkedIn-Connect-0077B5.svg"></a>
<a href="https://medium.com/@bobleesj"><img src="https://img.shields.io/badge/Medium-Read-00AB6C.svg"/></a>
</p>
