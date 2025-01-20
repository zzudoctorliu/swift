# swift grammar
Swift 的语法框架设计简洁、易读且功能强大，广泛用于苹果平台的应用开发。下面是一些 Swift 编程语言的核心语法和概念框架，帮助你了解 Swift 语言的基本结构和功能。

1. 变量和常量
	•	变量 用 var 声明：

var message = "Hello, World!"


	•	常量 用 let 声明，值不可修改：

let pi = 3.14159



2. 数据类型

Swift 是强类型语言，支持多种基本数据类型：
	•	整数：

var age: Int = 30


	•	浮动小数：

var price: Double = 19.99


	•	布尔值：

var isActive: Bool = true


	•	字符串：

var greeting: String = "Hello"



3. 控制结构
	•	条件语句：

if age > 18 {
    print("Adult")
} else {
    print("Child")
}


	•	循环：
	•	for-in 循环：

for i in 1...5 {
    print(i)
}


	•	while 循环：

var count = 0
while count < 5 {
    print(count)
    count += 1
}



4. 函数

定义一个函数使用 func 关键字：

func greet(name: String) -> String {
    return "Hello, \(name)"
}
print(greet(name: "John"))

5. 类和结构体

Swift 支持面向对象编程，使用 class 定义类，struct 定义结构体。
	•	类：

class Person {
    var name: String
    var age: Int
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
    func greet() {
        print("Hello, my name is \(name)")
    }
}

let person = Person(name: "Alice", age: 25)
person.greet()


	•	结构体：

struct Point {
    var x: Double
    var y: Double
}

var point = Point(x: 3.0, y: 4.0)



6. Optionals

Optionals 用于表示值可能为空的情况，用 ? 或 ! 标记：
	•	可选类型：

var name: String? = "John"


	•	解包可选值：
	•	安全解包：

if let unwrappedName = name {
    print("Hello, \(unwrappedName)")
}


	•	强制解包：

let unwrappedName = name!



7. 闭包 (Closures)

闭包是可以捕获并存储其所在上下文的函数或代码块。Swift 中的闭包非常强大，支持简洁的语法：

let add: (Int, Int) -> Int = { a, b in
    return a + b
}
print(add(2, 3))  // Output: 5

8. 枚举 (Enums)

枚举用于定义相关的值集合。可以带有关联值：

enum Direction {
    case north, south, east, west
}

var direction = Direction.north

9. 协议 (Protocols)

协议定义了一组方法和属性，类、结构体、枚举可以采用协议：

protocol Greetable {
    func greet()
}

class Person: Greetable {
    func greet() {
        print("Hello!")
    }
}

10. 错误处理 (Error Handling)

Swift 提供了强大的错误处理机制：
	•	定义错误类型：

enum MyError: Error {
    case invalidInput
    case networkError
}


	•	抛出和捕获错误：

func throwError() throws {
    throw MyError.invalidInput
}

do {
    try throwError()
} catch {
    print("Caught error: \(error)")
}



11. 扩展 (Extensions)

扩展允许你为现有类型添加新的功能，而无需修改原始类型的源代码：

extension Int {
    func squared() -> Int {
        return self * self
    }
}
print(4.squared())  // Output: 16

12. 自动引用计数 (ARC)

Swift 使用自动引用计数 (ARC) 来管理内存，开发者不需要手动管理内存，但需要理解强引用、弱引用和无主引用之间的区别，避免内存泄漏。

13. SwiftUI

SwiftUI 是苹果推出的声明式 UI 框架，用于开发用户界面。通过声明式语法，开发者可以轻松地创建跨平台的界面：

import SwiftUI

struct ContentView: View {
    var body: some View {
        Text("Hello, World!")
            .font(.largeTitle)
            .padding()
    }
}

@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            ContentView()
        }
    }
}

14. 异步编程（Concurrency）

Swift 5.5 引入了 async/await 语法，简化异步编程：

func fetchData() async -> String {
    return "Data fetched"
}

Task {
    let result = await fetchData()
    print(result)
}

###Swift 的语法框架旨在简洁、现代和类型安全，结合了面向对象编程、函数式编程和协议导向编程的特点。Swift 的设计使得编写高效、清晰和可维护的代码变得更加容易，尤其是在苹果平台开发中。如果你已经了解了上述语法和概念，可以进一步深入学习 Swift 来开发丰富的应用程序。###
