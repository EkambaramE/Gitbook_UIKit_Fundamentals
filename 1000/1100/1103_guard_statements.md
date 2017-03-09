# Guard Statement
## Introduction
Welcome back. We are at Lesson 3 of Part 1 of the Swift fundamentals with Bob. First of all, let me share a story of mine. When I learned Swift as my first programming language,  I understood  an `else-if` statement. It wasn't a big deal. For example, if something is `true`, you run a block. However, a `guard` statement confused the heck out of me. Maybe some of you guys feel the same way as I did. Don't worry. I'm here for you today. You will understand that a `guard statement` is just another for you to write an `else-if` statement. A `guard statement` provides a feeling of zenness. In other words, it adds clarity, emptiness, and lots of cloud and space. Let's get in.

## Lecture Notes

### Problem
Is there any better way to write an `else-if` statement? How do you safely unwrap many optionals?

### Typical else-if
Without having known guard statements, you used a long `else-if` statement to handle an error message block.

```swift
func checkDrinkingAge() {

  let canDrink = true

  if canDrink {
    print("You may enter")
    // More
    // More Code
    // More Code

  } else {
    // More Code
    // More Code
    // More Code
    print("Let me take you to the jail")
  }
}
```

### Issues with else-if
1.  Nested brackets
2.  Have to read every line to spot error

### Guard Statement
It provides an early exit and fewer brackets. A `guard` block only runs if the condition is `false`. If not, the function ignores it. If the condition is `false`, it will call `return` which causes the function to stop.

```swift
func checkDrinkProgram() {
  let iCanDrink = true

  guard iCanDrink else {
    // if iCanDrink == false, run this block
    print("You can't drink")
    return
  }

  print("You may drink")
  // You may move on
  // Come on.
  // You may leave
  // You don't need to read this.
  // Only one bracket on the bottom: feeling zen.
}
```


### Unwrap Optionals with else-if
A `guard` statement is not only useful for replacing an `else-if` statement. It could also unwrap optionals by minimizing the number of brackets. To compare, let's first begin how to unwrap multiple optional types using an `else-if`.

```swift
var publicName: String? = "Bob"
var publicPhoto: String? = "URL"
var publicAge: Int? = 21

// If I find "nil" in any of these variables, don't do anything

func unwrap() {
  if let name = publicName, let photo = publicPhoto, let age = publicAge {
         print("Your name is \(name). I see your face right here, \(photo), you are \(age)")
  } else {
    print("Something is missing")
    // Animation Logic
    // Networking
  }

```
### Unwrap Optionals with Guard
Let's learn how a `guard` statement is used as a way to safely/implicitly unwrap optionals.

```swift
func safetlyUnwrapUsingGuard() {

  guard let name = publicName, let photo = publicPhoto, let age = publicAge else {
    //  If  one or more optionals contain nil
    print("Something is missing")
    return
  }

  // All optionals contain non-nil
  print("Your name is \(name). I see your, \(photo). You are \(age).")
  // Animation Logic
  // Networking
  // More Code, but still zen
}
```

### Source Code
[1103_Guard Statement](https://www.dropbox.com/sh/locish5028pi9vh/AAD2ZnHDhOHdy8ArFspUO219a?dl=0)

### Resources
[The Complete Swift 3 Tutorial with Bob: Guard Statement (YouTube)](https://www.youtube.com/watch?v=oeUYGNLqqqg)

## Conclusion
By now, I hope you understand the power of using a `guard` statement. It provides an early exit and you don't have to read all the way to the bottom spot error messages. You use a `guard` statement not just to please yourself, but also for the sake of your teammate's falling hair and prevent it from turning into grey when he/she reads your code. Okay, great. In our next lesson, you are going to learn another `!` and `?` for `type casting` which allows you to convert types. 🤔 Let's find out.

#### Stay Connected
I focus on building a long-term relationship with you. Feel free to follow on my social media for personal updates and engagement. You may see what my daily activity is like on Instagram.  

<p>
<a href="http://bobthedeveloper.io"><img src="https://img.shields.io/badge/Personal-Website-333333.svg"></a>
<a href="https://facebook.com/bobthedeveloper"><img src="https://img.shields.io/badge/Facebook-Like-3B5998.svg"></a> <a href="https://youtube.com/bobthedeveloper"><img src="https://img.shields.io/badge/YouTube-Subscribe-CE1312.svg"</a> <a href="https://twitter.com/bobleesj"><img src="https://img.shields.io/badge/Twitter-Follow-55ACEE.svg"></a> <a href="https://instagram.com/bobthedev
"><img src="https://img.shields.io/badge/Instagram-Follow-BB2F92.svg"></a> <a href="https://linkedin.com/in/bobleesj"><img src= "https://img.shields.io/badge/LinkedIn-Connect-0077B5.svg"></a>
<a href="https://medium.com/@bobleesj"><img src="https://img.shields.io/badge/Medium-Read-00AB6C.svg"/></a>
</p>
