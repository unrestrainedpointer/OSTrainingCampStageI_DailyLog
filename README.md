# OSTrainingCampStageI_DailyLog
This is the daliy log of OS training camp for stage 1
|  Sunday   | Monday  | Tuesday | Wednesday | Thursday | Friday | Saturday |
|  :----:  |  :----:   |   :----:   |  :----:  |   :----:   |  :----:   |   :----:  | 
|   |  |   |  |   | 1<br>[Day 1](#day-1) | 2<br>[Day 2](#day-2)  | 
| 3<br>[Day 3](#day-3)  | 4<br>[Day 4](#day-4) | 5<br>[Day 5](#day-5)  | 6<br>[Day 6](#day-6) | 7<br>[Day 7](#day-7)  | 8<br>[Day 8](#day-8) | 9<br>[Day 9](#day-9)  | 
| 10<br>[Day 10](#day-10)  | 11<br>[Day 11](#day-11) | 12<br>[Day 12](#day-12)  | 13<br>[Day 13](#day-13) | 14<br>[Day 14](#day-14)  | 15<br>[Day 15](#day-15) | 16<br>[Day 16](#day-16)  | 
| 17<br>[Day 17](#day-17)  | 18<br>[Day 18](#day-18) | 19<br>[Day 19](#day-19)  | 20<br>[Day 20](#day-20) | 21<br>[Day 21](#day-21)  | 22<br>[Day 22](#day-22) | 23<br>[Day 23](#day-23)  | 
| 24<br>[Day 24](#day-24)  | 25<br>[Day 25](#day-25) | 26<br>[Day 26](#day-26)  | 27<br>[Day 27](#day-27) | 28<br>[Day 28](#day-28)  | 29<br>[Day 29](#day-29) | 30<br>[Day 30](#day-30)  | 
| 31<br>[Day 31](#day-31)  |  |   |  |   |  |   | 

## Day 1
### Study Rust
Using websites:
1. https://www.youtube.com/watch?v=yYlPHRl2geQ&list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk&index=5
2. https://kumakichi.github.io/easy_rust_chs/Chapter_9.html

Today, I have learned about comments, some primitive types, type inference and floats and so on. Because I am the beginner of rust, I have to study from scratch. There is nothing else worth logging because of the simplification of today's content.

## Day 2
### Study Rust
Using websites:
1. https://www.youtube.com/watch?v=yYlPHRl2geQ&list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk&index=5
2. https://kumakichi.github.io/easy_rust_chs/Chapter_9.html

- Declaring variables and code blocks:
    - Code blocks are like functions:
    - ```
          let my_number={
            let second_number=9;
            second_number
          };
          println!("{}", my_number);
      ```
      It prints 9.
     - ```
          let my_number={
            let second_number=9;
            second_number+9;
          };
          println!("My number is:{:?}", my_number);
        ```
      It prints nothing because we are ending this block with a semicolon. Thus, a value for returning must not end with a semicolon.
- Debug print:
    - Considering about the example above, what does the {:?} mean?
    - If we remove the ':?' in '{}', we will get an error that '()' does not implement 'std::fmt::Display'
- Mutability = ability to change.
    - Consider about the code below:
    - ```
      let my_number = 8;
      println!("My number is: {}", my_number);
      my_nunmber = 10;
      println!("My number is: {}", my_number);
      ```
      The second print will  get an error that cannot assign twice to immutable variable 'my_number'.
     - It is immutable default in rust and you can use `let mut my_number = 8` to make my_number mutable.
