# Week 8 - Producer Consumer Using POSIX Semaphores

## Aim

To implement the Producer-Consumer problem using a bounded circular buffer with one producer and one consumer using pthreads and POSIX semaphores.

## Description

This program uses a circular buffer of fixed size to store items produced by the producer thread.

Three POSIX unnamed semaphores are used:

- `empty` - keeps track of the number of empty spaces in the buffer.
- `full` - keeps track of the number of items available in the buffer.
- `mutex` - ensures that only one thread accesses the shared buffer at a time.

The producer adds items to the buffer, while the consumer removes items from the buffer.

## Files

- `producer_consumer.c` - C program implementing the Producer-Consumer problem.

## Compilation

Compile the program using:

```bash
gcc producer_consumer.c -o producer_consumer -pthread 

