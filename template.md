# DART Programming Language

<img src="https://dart.dev/assets/shared/dart-logo-for-shares.png?2" width = 400>

# PARVIN EYVAZOV
## - History of the language

Dart is an object-oriented, class-based, garbage-collected language with C-style syntax. Dart can compile to either native code or JavaScript. It supports interfaces, mixins, abstract classes, reified generics and type interfence.

Approved as an Ecma standart(European Computer Manufactures Association), Dart is a general purpose programming language which was created by Google. Its major use is in the creation application for web, servers, mobiles and Internet of Things devices. Dart possesses a BSD(Berkeley Software Distribution) license and an open source software.

Dart has a syntax quite similar to that of C and can transcompile into JavaScript optionally. It is single inheritance, class based and object oriented language. Dart has support for mixins, interfaces, reified generics, optional typing and abstract classes. Dart code runs faster than the same code written in JavaScript. In addition, Dart code can be run directly in some Google Chromium browsers and standalone Software Development Kits to be used in command line interfaces. Dart codes can be compiled into JavaScript have made the language quite compatible with many modern day web browsers.

The GOTO conference took place during 10th-12th  October 2010 at Aarhus, Denmark. It was here that the Dart programming language was revealed for the first time. The Dart project had been initiated by Lars Bak, a Danish programmer famous for his work on virtual machines and contributions to the creation of Google Chrome browsers and Kasper Lund, a software engineer. 


## - Why was it invented

C#  +  Java  +  Python  +  JavaScript  =  Dart

It is compiled, type-safe language(like C# and Java)  and a scripting language (like Python and JavaScript) at the same time. Dart is similar to C# and Java syntax.

Actually, Dart was made to replace Javascript, and at some point, all front-end Framework. But Dart today is a very different language than what it was 8 years ago. It has sound static type system, AOT compilation and lot of syntactic sugar to make building user interface in code better experience. Many of these language changes are driven by Flutter requirements. 

Dart was originally designed with the web in mind. A collection of engineers within the Chrome/V8 org had a laundry list of issues they wanted to address with web development, from the performance of method dispatch in JavaScript to a cleaner, easier-to-use language with decent (but relatively compact) core libraries. A variant of Chromium informally referred to as Dartium embedded both V8 and the Dart VM and was used for rapid edit-refresh development. For production deployment, the code was compiled through dart2js, a tree-shaking compiler that emitted optimised, minified JavaScript. Dart on the web is pretty heavily-used within Google, particularly within Ads (for example, the AdWords frontend), but can also be seen in the Google Fiber frontend, and running on the Fiber set top boxes among others.


## - How to setup an environment to use it in different platforms
## Windows
For installing the Dart SDK we can use [Chocolatey](https://chocolatey.org/)

To install the Dart SDK:
```bash
C:\ > choco install dart-sdk
```

To upgrade the Dart SDK:

```bash
C:\ > choco upgrade dart-sdk
```

## Linux

For installing the Dart SDK we can use apt-get

Install apt-get

```bash
$ sudo apt-get update
$ sudo apt-get install apt-transport-https

$sudo sh -c 'wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'

$sudo sh -c 'wget -qO- https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'
```

Then install the Dart SDK:

```bash
$ sudo apt-get update 
$ sudo apt-get install dart
```

## Mac

First, we have to install [Homebrew](https://brew.sh/) and then run the following commands:

```bash
$ brew tap dart-lang/dart 
$ brew install dart
``` 

To upgrade when a new release of Dart is available:

```bash
$ brew upgrade dart
```






# ILKIN MAMMADZADA
## - When/why shall we use it
There are a lot of things that makes Dart better than other OOP languages.
### 1. Flexibility

You can run your Dart code in anywhere. Mobile app codes in Dart can
run for Android and iOS at the same time. Dart also gives you opportunity to switch
between type-less and other type coding. For unit tester, Dart provides built-in
support. You do not need any lib or framework.

### 2. Open Source

Open source languages are always choice of programmers. In tech world
all open-source softwares self-improves. If user see bug, he/she report or try to 
solve it immediately.

### 3. Easy to learn

Dart is statically typed.
Type inference refers to the automatic detection of the data type of an
expression in a programming language. The ability to infer types automatically makes
many programming tasks easier, leaving the programmer free to omit type annotations
while still permitting type checking.
Dart syntax is simple.
Anyone who knows a bit Java,C, C#, it will be very easy to learn Dart.
Syntaxes are ver similar.

### 4. Compiles 

Dart has AOT and JIT compiles. JIT compilation provides HOT Reloading.
This saves a lot of time of devs.

### 5. Single-page app

Dart can be extensively used to create single-page applications.
Single-page applications apply only to websites and web applications.
Single-page applications enable navigation between different screens of
the website without loading a different webpage in the browser.

## - Example codes

Dart - Mixin code example

```dart
import 'dart:math';

class Position {
  int x;
  int y;

  double distanceTo(Position other) {
    var dx = other.x - x;
    var dy = other.y - y;
    return sqrt(dx * dx + dy * dy);
  }
}

class Square {
  int width;
  int height;

  int get area => width * height;
}

// Classes can be mixed in using 'with'
class SquareView extends Square with Position {}

main() {
  var origin = new Position()
    ..x = 0
    ..y = 0;

  var square = new SquareView()
    ..x = 5
    ..y = 5
    ..width = 10
    ..height = 10;

  print(square.distanceTo(origin));
  print(square.area);
}
```

## - Things that are specific to this language?

### 1. Concepts

Everything in Dart is object. All objects inherit from Object class.
Dart parses all your code before running it.
	
### 2. Functions

Functions are also objects.

```dart bool isTrue(int ballNumber) => _balles[ballNumber] != null; ```
```dart => expr ``` syntax is stand for ```dart {return expr; } ```
	
### 3. Operators

"~/"  -> divide, returns an integer result.
(..)  -> make a sequence of operations
Dart has syntactic sugar
Constructors aren’t inherited by subclass. If subclass
don't provide a constructor, a default constructor will be provided.
To create factory contructor, you can use ```dart factory ``` keyword.
	
### 4. Asynchronous functions

Dart provides Future and Stream object to support asynchronous functions.
	
#### Futures

Future means return value will be returned at some time in the future.
To get the result of Future, you can use .then followed by block codes
	  
#### Streams

Stream support to receive a sequence of events.To get values from a Stream,
use can use ```dart async. ```
```dart
	await for (varOrType identifier in expression) {
  	  // Executes each time the stream emits a value.
	}
```
Execution proceeds:
1. Wait until the stream emits a value.
2. Execute the body of the for loop, with the variable set to that emitted value.
3. Repeat 1 and 2 until the stream is closed.

