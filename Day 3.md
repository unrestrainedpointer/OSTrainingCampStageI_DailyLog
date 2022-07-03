# Day 3
### Study Rust
#### Collection types: Arrays and Vectors
##### Arrays
1. `let my_array=["One, Two"];`
2. We can use `my_array.thdaoethothed();` to get our arrays' type.

#### Vectors
1. ```
      fn main(){
          let name1="Windy";
          let name2="Gomesy";
          let name3="MB";
          
          let mut my_vec=Vec::new();
          
          my_vec.push(name1);
      }
   ```
   If we remove `my_vec.push(name1);`, it will return an error because the complier does not know the type of elements in the vector.
2. `let my_vec: Vec<String> = Vec::new();`
   `let my_vec=vec![7,8,9,10];`
   We can create a vector like this.
3. `let vec_of_ten=vec![1,2,3,4,5,6,7,8,9,10];`
   `let three_to_five=&vec_of_ten[2..5];`
   We can use references to split the vector.
5. We can use `my_vec.capacity()` to get the capacity of a vector.
6. 
