# References in C++ and Java are *TOTALLY* different

Based on the below code:
```
Student s1 = Student("Astro");
Student & s2 = s1;
Student s3 = s2;
```
We first create an object s1 with string "Astro". Second line means s2 is exactly thr same student as s1, which means if we modify s2, s1 will also be modified. 
The third line means we create *another* object which the name of the students of s2 and s3 are the same. However, s2 and s3 are not the same objects. They just have the 
same name of the student. 
<img width="500" alt="Screen Shot 2022-09-26 at 1 44 21 PM" src="https://user-images.githubusercontent.com/97696773/192376430-e91baced-039b-4dfc-b234-4ca1ed261e94.png">

# Pointers in C++ is *similar* to Java

`*` = pointer

`&` = memory address

based ib the below code:
```
Student s = Student("Astro");
Student* ptr = &s;
Student** ptrPtr = &ptr;
```
We first create the object called s with name Astro. Then second line indicates that we declare an pointer that point to the memory address of the Student s. 
Third, since in c++ a pointer can point to another pointer, we create another pointer *ptrPtr that point to the previous one *ptr. 

<img width="868" alt="Screen Shot 2022-09-26 at 1 59 19 PM" src="https://user-images.githubusercontent.com/97696773/192379437-81e1309f-95f0-4d36-aa4a-28ae92d3fe22.png">

`Dereferencing` is getting the pointed value. 
We have 2 ways to do this in c++.
1. `Dereference` (*ptr).name ,name here is just a instance variables in class Student
2.  `Arrow Dereference` ptr -> name, name here is same as above

# Memory Manangement

Based on the below code: 
```
Student s1 = Student("Astro");
Student* s2 = new Student("Gary");
```
In Student s1, we create an object and when it was returned, it would automatically be deallocated by C++. However, in s2(pointer with type Student), since we use `new` which means 
it's a `Dynamic Memory Allocation` to point to the address of Student("Gary"). When it was returned, it would not automatically dellocated by C++ which can cause
`Memory Leak`. To address this issue, we have manually `delete` it to deallocate the memory of s2. 

<img width="971" alt="Screen Shot 2022-09-26 at 2 19 04 PM" src="https://user-images.githubusercontent.com/97696773/192382556-2ba1001d-62a3-4187-bd55-e836f9316868.png">


# Vector


# Stack v.s Heap

## Heap:
1. dynamic memory allocation
2. new, malloc
3. delete free
4. dynamically allocate objects if we need them to exist 

## Stack:
1. Local variables created within functions






    
