Philosophers Case Study

Overview
A study on concurrent programming and synchronization using the classic "Dining Philosophers" problem. The goal was to ensure thread safety and prevent resource starvation.

Technical Architecture
* Concurrency: Implemented multi-threading using pthread_create and pthread_join.
* Synchronization: Used mutexes to control access to shared resources (the "forks").
* Optimization: Developed a monitoring thread to track the state of every philosopher     in real-time to detect if anyone has died (the "starvation" scenario).

Engineering Challenge
Preventing **deadlocks** was the primary challenge. I implemented a strict locking protocol—if a philosopher takes the left fork, they must verify the right fork is available before attempting to pick it up, otherwise, they yield the resource. This eliminated circular waiting conditions.
