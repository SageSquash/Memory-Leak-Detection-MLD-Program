# Memory-Leak-Detection-MLD-Program

This program is designed to detect memory leaks in C programs using the Memory Leak Detection (MLD) technique. It identifies and prints leaked objects, helping developers identify and fix memory management issues.

Prerequisites
gcc compiler
Linux or Unix-like operating system
Build
To build the program, execute the following commands in the terminal:

```
gcc -g -c mld.c -o mld.o
gcc -g -c LinkedList/LinkedListApi.c -o LinkedList/LinkedListApi.o
gcc -g -c app.c -o app.o
gcc -g -o exe app.o LinkedList/LinkedListApi.o mld.o
```

Run
To execute the program, run the following command:
```
./exe
```

Leaked Objects
The program prints the leaked objects, providing valuable information for debugging and resolving memory leaks. Here is an example of the output:
Dumping Leaked Objects

```
-----------------------------------------------------------------------------------------------------|
0   ptr = 0x5a57db83fa40 | next = 0x5a57db83fa10 | units = 1    | struct_name = student_t  | is_root = FALSE |
-----------------------------------------------------------------------------------------------------|
student_t[0]->stud_name = jose
student_t[0]->rollno = 1
student_t[0]->age = 22
student_t[0]->aggregate = 85.50
student_t[0]->best_colleage = (nil)
```

The above example demonstrates the detection of a leaked object of type student_t. The object's attributes and memory addresses are provided, aiding in the identification and resolution of memory leaks.

