# Concurrency 
Concurrency is very important aspect of application design and architecture , repo contains various patterns and apporach to handle concurrency in golang microservice

Below is a simple golang service example which receives request and for every request http package(golang standard package) creates new Goroutine and we have go scheduler whose responsibility is to manage Goroutine and allocate run time from operation system threads.  

![Untitled drawio](https://user-images.githubusercontent.com/98384750/150939789-14e6acab-398c-46e6-83b7-8f6e4b966383.png)


