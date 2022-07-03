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
4. We can use `my_vec.capacity()` to get the capacity of a vector.

#### Exercises
##### Variables:
1. variables1.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047143-6db11071-9564-4846-b4c9-f7a43d1c41c3.png)
2. variables2.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047351-83e3cf34-46d1-436a-ba8a-e506891edadc.png)
3. variables3.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047301-17d5203c-e208-45eb-9229-436f1419dae5.png)
4. variables4.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047393-3aa2051c-7acf-4d14-820e-54fc2c0f4441.png)
5. variables5.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047440-eaa8bfef-516a-4a31-9266-b17d3125cd77.png)
6. variables6.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047485-5ba984e0-3ed6-4bef-82e4-d9fa189bb2d6.png)

##### Functions
1. functions1.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047776-1ec55f45-3419-4188-896d-4a783975be06.png)
2. functions2.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047860-340a3d1c-4711-405b-9c7d-e8626648584d.png)
3. functions3.rs
   ![image](https://user-images.githubusercontent.com/102142490/177047923-be0bc6c7-db6d-4779-ad8b-d8278245d3ad.png)
4. functions4.rs
   ![image](https://user-images.githubusercontent.com/102142490/177048082-604ce27b-8a3f-4724-b685-3bad5deb422c.png)
5. functions5.rs
   ![image](https://user-images.githubusercontent.com/102142490/177048129-316c2e4f-b97a-4c2d-babc-c18a88e29dc4.png).

##### If
1. if1.rs
   ![image](https://user-images.githubusercontent.com/102142490/177048239-7f3e9569-003b-4909-9b60-8ffe5cce9657.png)
2. if2.rs
   ![image](https://user-images.githubusercontent.com/102142490/177048346-0a0b72c9-f57b-4193-ba98-011210d31a12.png)


