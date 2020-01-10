### Third party library
* [Trio](https://github.com/python-trio/trio) – a friendly Python library for async concurrency and I/O
  
# multithread in python 
Concurrent situation: printing/downloading/requests 


[When do we use multithreading in python? ](https://medium.com/towards-artificial-intelligence/the-why-when-and-how-of-using-python-multi-threading-and-multi-processing-afd1b8a8ecca)
> Using multiple threads can significantly speed up many tasks that are IO-bound. Here, the vast portion of the time taken to read the URLs is due to the network delay. 

> Python will happily let you spawn as many threads as you like, but the GIL ensures that only one of those threads will ever be executing at any given time.

> For an IO-bound task, that is perfectly fine. One thread fires off a request to a URL and while it is waiting for a response, that thread can be swapped out for another thread that fires another request to another URL. Since a thread doesn’t have to do anything until it receives a response, it doesn’t really matter that only one thread is executing at a given time.