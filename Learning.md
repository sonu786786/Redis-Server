# Doubt

1) "include<atomic>" is used for what purpose? <br><br>
Ans) #include <atomic> lets you use std::atomic<T> to make variables safe when multiple threads read/write them at the same time—no locks needed.​<br>
Simple Purpose:<br>
In multithreaded code (like the Redis server handling many clients), normal bool running = true; can get corrupted if one thread reads while another writes. std::atomic<bool> running(true); fixes this by making changes "atomic" (one step, unbreakable).
