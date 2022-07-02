# Day 2
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
