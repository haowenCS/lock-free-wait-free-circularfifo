### The experiment result

1. Circular_FIFO with lock shared:

```text
/Users/mac/Documents/工作/C++/lock-free-wait-free-circularfifo/cmake-build-debug/unit_test_lock_shared --gtest_filter=* --gtest_color=no
Testing started at 11:50 下午 ...
hello from thread 
std::thread::hardware_concurrency() = 16


Prepare to wait a bit, pushing 1000000 through a locked dynamic fifo 

	#1000000 items took #158 milliseconds to shuffle

Producer: 	#1000000 items took #125.234 milliseconds to shuffle, average: 0.125234, hit limit?: 0


Consumer: 	#1000000 items took #157.781 milliseconds to shuffle, average: 0.157781, hit limit?: 0


FINISHED WITH THE TESTING
Process finished with exit code 0
```

2. Circular_FIFO with lockfree aquire release relaxed:

```text
/Users/mac/Documents/工作/C++/lock-free-wait-free-circularfifo/cmake-build-debug/unit_test_lockfree_aquire_release --gtest_filter=* --gtest_color=no
Testing started at 11:52 下午 ...


hello from thread 
std::thread::hardware_concurrency() = 16


Prepare to wait a bit, pushing 1000000 through a circular fifo of size: 1048576

	#1000000 items took #58 milliseconds to shuffle

Producer: 	#1000000 items took #22.003 milliseconds to shuffle, average: 0.022003, hit limit?: 0


Consumer: 	#1000000 items took #57.82 milliseconds to shuffle, average: 0.05782, hit limit?: 1


FINISHED WITH THE TESTING
Process finished with exit code 0
```