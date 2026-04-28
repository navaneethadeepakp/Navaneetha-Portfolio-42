Minishell Case Study

Overview
Replicated a functional Unix shell to understand the core mechanisms of Operating Systems, specifically how processes are created, managed, and executed.

Technical Architecture
* Process Management: Used fork() to create child processes and execve() to execute system commands.
* Communication: Implemented Inter-Process Communication (IPC) using pipe() and file descriptors for command chaining.
* Signal Handling: Configured sigaction to handle shell interruptions (like Ctrl+C and Ctrl+D) without exiting the parent process.
* Memory Management: Developed a custom list-based memory tracker to ensure no leaks occurred during long-running shell sessions.

Engineering Challenge
The biggest hurdle was synchronizing input/output redirection with multi-level pipes. I solved this by treating the command line as a tree structure, where each node represented a command, allowing the shell to recursively set up pipes before execution.
