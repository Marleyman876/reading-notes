# Stacks and Queues

* A stack is a dta structure that consists of Nodes.

Some common terminologies for stacks are:

* Push - Nodes or items that are put into the stack are pushed

* Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.

* Top - This is the top of the stack.

* Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.

* IsEmpty - returns true when stack is empty otherwise returns false.

Stacks Are FILO's or First in Last out concept data structures, the first item added to the stack will be the last item taken from the stack.

## Queues

Like stack, queue is a linear data structure that stores items in First In First Out (FIFO) manner. With a queue the least recently added item is removed first. A good example of queue is any queue of consumers for a resource where the consumer that came first is served first.

Operations associated with queue are:

* Enqueue: Adds an item to the queue. If the queue is full, then it is said to be an Overflow condition – Time Complexity : O(1)

* Dequeue: Removes an item from the queue. The items are popped in the same order in which they are pushed. If the queue is empty, then it is said to be an Underflow condition – Time Complexity : O(1)

* Front: Get the front item from queue – Time Complexity : O(1)

* Rear: Get the last item from queue – Time Complexity : O(1)
