# LeetCode 225 - Implement Stack using Queues

## Problem

Implement a last-in-first-out (LIFO) stack using only queue operations.

The stack should support the following operations:

* `push(x)` - Pushes element `x` onto the stack.
* `pop()` - Removes and returns the top element.
* `top()` - Returns the top element without removing it.
* `empty()` - Returns `true` if the stack is empty.

## Example

```text
Input:
["MyStack", "push", "push", "top", "pop", "empty"]
[[], [1], [2], [], [], []]

Output:
[null, null, null, 2, 2, false]
```

## Approach

A queue normally follows FIFO order, while a stack follows LIFO order.

We use one queue and rearrange its elements after every `push`.

When a new element is added, all previous elements are moved behind it. This makes the newest element stay at the front of the queue.

Therefore:

* `push()` adds the element and rearranges the queue.
* `pop()` removes the front element.
* `top()` returns the front element.
* `empty()` checks whether the queue is empty.

## Algorithm

1. Create an empty queue.
2. For `push(x)`, add `x` to the queue.
3. Move all previous elements from the front to the back.
4. The newest element is now at the front.
5. For `pop()`, remove the front element.
6. For `top()`, return the front element.
7. For `empty()`, check whether the queue contains any elements.

## Complexity

* `push()` - `O(n)`
* `pop()` - `O(1)`
* `top()` - `O(1)`
* `empty()` - `O(1)`
* Space Complexity - `O(n)`

## Language

Python

## LeetCode

Problem: 225 - Implement Stack using Queues

## Author

**T.Nandhini**
