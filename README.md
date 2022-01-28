# Concurrency 
Concurrency is very important aspect of application design and architecture, This repository contains various patterns and apporach to handle concurrency in golang microservice


# What is Concurrency 
Consider a microservice(which support Rest), If system does not support concurrency then each incoming request will be executed one at a time meaning a user will have to wait for sometime before all the request before his request has been served , We all know this is not the case , So whats actually happening , Each incoming request is running simulataneously with other that is called concurrency executing sub task simaltaneously.

But Wait Whats is Parallism then 
# Parellelism
Parellelism is saying every sub-task of an application is running simaltaneously and for each sub-task a seperate CPU/Core is allocated so it does not have wait for CPU time

Below is a simple golang service example which receives request and for every request http package(golang standard package) creates new Goroutine and we have go scheduler whose responsibility is to manage Goroutine and allocate run time from operation system threads.  

![Untitled drawio](https://user-images.githubusercontent.com/98384750/150939789-14e6acab-398c-46e6-83b7-8f6e4b966383.png)


We are saying that each request is a goroutine then what is this goroutine

# Goroutine 
Goroutine also called green thread or user space threads , We cannot call it as light weight thread as its not actually a thead , It actually is a small function or methods which is executed by Os thread , We can also see it as abstraction over thread.

Goroutines are very light weight as they dont have to maintain context or run queue , Its just a small peice of code which is looking to be executed. Go scheduler picks up Goroutines and assigns it to OS thread to get executed.

# Go Scheduler 
Go Scheduler is a program provider by go runtime which manages all goroutine , What does manages means 
1. 

![Untitled drawio (2)](https://user-images.githubusercontent.com/98384750/151479809-449ecce5-313e-4179-abeb-a179747124c6.png)
