# Requirements

## 1. Implement a stack

Functions:

  * **`stack_create()`** - This function should allocate, initialize, and return a pointer to a new stack structure.

  * **`stack_free()`** - This function should free the memory held within a stack structure created by `stack_create()`.  Note that this function only needs to free the memory held by the stack itself.  It does not need to free the individual elements stored in the stack.  This is the responsibility of the calling function.

  * **`stack_isempty()`** - This function should return 1 if the stack is empty and 0 otherwise.

  * **`stack_push()`** - This function should insert a new element on top of the stack.  **This operation must have O(1) average runtime complexity.**

  * **`stack_top()`** - This function should return the value stored at the top of the stack without removing it.  **This operation must have O(1) average runtime complexity.**

  * **`stack_pop()`** - This function should pop a value from the stack and return the popped value.  **This operation must have O(1) average runtime complexity.**

Importantly, the stack you build **MUST** use a linked list as its underlying data storage.  You are provided with a linked list implementation in `list.h` and `list.c` that you may use for this purpose.  Feel free to modify this linked list implementation as needed to implement your stack, *with the constraint that you may only interact with the linked list implementation via its interface functions.*  In particular, you may not directly access or modify the fields of the linked list structure (`struct list`).  In other words, you may not change the fact that `list.h` only contains a forward declaration of `struct list`, and you may not redefine the list structure in `stack.h` or `stack.c`.

Also, note that, as with the data structures you implemented in assignment 1, values in the stack will be stored as void pointers.

## 2. Implement a queue

Functions:

  * **`queue_create()`** - This function should allocate, initialize, and return a pointer to a new queue structure.

  * **`queue_free()`** - This function should free the memory held within a queue structure created by `queue_create()`.  Note that this function only needs to free the memory held by the queue itself.  It does not need to free the individual elements stored in the queue.  This is the responsibility of the calling function.

  * **`queue_isempty()`** - This function should return 1 if the queue is empty and 0 otherwise.

  * **`queue_enqueue()`** - This function should insert a new element at the back of the queue.  **This operation must have O(1) average runtime complexity.**

  * **`queue_front()`** - This function should return the value stored at the front of the queue without removing it.  **This operation must have O(1) average runtime complexity.**

  * **`queue_dequeue()`** - This function should dequeue a value from the queue and return the dequeued value.  **This operation must have O(1) average runtime complexity.**

Importantly, the queue you build **MUST** use a dynamic array as its underlying data storage.  You are provided with a dynamic array implementation in `dynarray.h` and `dynarray.c` that you may use for this purpose.  Feel free to modify this dynamic array implementation as needed to implement your queue, *with the constraint that you may only interact with the dynamic array implementation via its interface functions.*  In particular, you may not directly access or modify the fields of the dynamic array structure (`struct dynarray`).  In other words, you may not change the fact that `dynarray.h` only contains a forward declaration of `struct dynarray`, and you may not redefine the dynamic array structure in `queue.h` or `queue.c`.

Also, note that, as with the data structures you implemented in assignment 1, values in the queue will be stored as void pointers.

## Testing

```
make
./test_stack
./test_queue
```
Example output of these two testing programs using correct implementations of the stack and queue is provided in the `example_output/` directory.

In order to verify that your memory freeing functions work correctly, it will be helpful to run the testing applications through `valgrind`.

