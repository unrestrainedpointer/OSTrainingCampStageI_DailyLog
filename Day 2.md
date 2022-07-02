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
      my_number = 10;
      println!("Now my number is: {}", my_number);
      ```
      The second print will  get an error that cannot assign twice to immutable variable 'my_number'.
     - It is immutable default in rust and you can use `let mut my_number = 8` to make my_number mutable.
     - However, you can still not write `my_number = "Hello world";`. Otherwise, you will attain an error showing mismatched types.
     - To debug this error, you can write `let my_number = "Now I am a string";`. And this is called shadowing and will be illustrated in the next point. Here we just need know that when you use let again, it has nothing to do with mutability and you are creating something totally and the only thing that makes it looks like it's mutable is that the name is same but it is not the same variable at all.
- Shadowing: It is similar with the mutability, but they are different. For the last example, the second 'let' does not kill the first 'my_number'.
     - Consider about the code below:
     - ```
       let my_number = 8;
       println!("{}", my_number);
       {
            let my_number=9.2;//Here we are shadowing the first my_number
            println!("{}", my_number);
       }//But the second my_number only lives up to here. When we print it out, it is going to print the first my_number.
       println!("{}", my_number);
       ```
     - Here we can learn that the second my_number does not kill the first one. When it dead, we will get the first one.
     - Consider about the code below:
     - ```
       fn times_two(number: i32)->i32{//here '->' means that we need to return a variable whose type is 'i32'.
            number*2 //Do not forget that there is no semicolon here.
        }
        
        fn main(){
            let final_number={
                let y=18;
                let x=9;
                let x=times_two(x);
                let x=x+y;//Shadow with new x: 28
                x
            };
            println!("The number is now: {}", final_number)
        }
        ```
        We do not need too many variable names with shadowing.
- The stack, the heep, and pointers: the pointer in rust is called a reference.
     - If you want to define a reference, you can give a name and just put an ampersand in front of it like this: `let my_reference = &my_variable` and you can have a reference of a reference and as many as you want.
     - & and * are opposite symbols which means respectively references and the value that my referencec is pointing , so using * , you will go back to values.
     - The synmbol * works like this: `my_variale == *my_reference`.
     - Besides, && is opposite to **.
- More advanced printing: Something more about printing.
     - You need type double slash '\' to print slash, and another way is list this: `println!(r#"He said, "You can find the file at c:\files\my_documents\file.txt" Then I found the file."#)`. Usind 'r' and two pound signs to show the raw string is started and finished.
     - How to print #? You can use ## instead of #, then # between the two ## will be considered as a part of the string. And so on, if you want to print ###, you can start and end the string with ####.
     - Another letter we can put in front of strings is 'b' expect 'r', which can convert a string into bytes.
     - ```
            let number=555;
            println!("Binary: {:b}, hexadecimal: {:x}, octal: {:o}", number, number, number);
       ```
- Strings: Rust has two types of strings: String and &str
     - &str is a simple string, and it is a reference stored in the stack because rust knows the size of a reference, and the value it is pointing exit in the heap so that we can change it's size dynamically.
     - String is more like a struct of string.
     - There are ways to create a String:
          - `String::from("This is the string text");`
          - `"This is the string text".to_string();// It accepsts &str and make it a String.`
          - `let together=format!("I am {} and I come from {} but I live in{}", my_name, my_country, my_home);`
          - `let my_string: String = "Try to make this a String".into();`, if you remove the declare of type String, the compiler will report an error because it does not know which type you want to conver to from &str.
- const and static: const is used for some fixed values, and variables declared in static has their settled position in memories. They are all alive through the whole program.
