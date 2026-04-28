Get_Next_Line Case Study

Overview
A project centered on efficient file I/O. The goal was to write a function that returns a line read from a file descriptor, handling any buffer size without loading the entire file into memory at once.

Technical Architecture
* System Calls: Used the read() system call to fetch chunks of data from a file descriptor.
* State Management: Utilized static variables to persist the "leftover" data in the buffer between function calls.
* Memory Safety: Implemented precise dynamic memory allocation (malloc/free) to ensure no data was lost and no memory leaks occurred, regardless of the line length.

Engineering Challenge
The biggest hurdle was managing the buffer persistence. Since the function must be called multiple times to read a full file, I had to ensure that the "remainder" of the buffer (the characters after the \n) was preserved correctly across calls. I solved this by using a linked list to store buffer states, allowing for thread-safe-like logic even in a single-threaded environment.
