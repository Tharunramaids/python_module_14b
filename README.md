# Priority Queue Implementation in Python

## Aim
To implement a priority queue using a class in Python where elements are dequeued in order of highest priority (largest value first).

## Procedure
1. Define a class `PriorityQueue` with an internal list `queue`.
2. Implement the following methods:
   - `insert(data)`: Adds an element to the queue.
   - `delete()`: Finds and removes the element with the highest priority (maximum value).
   - `isEmpty()`: Checks if the queue is empty.
3. Accept `n` elements from the user and insert them into the priority queue.
4. Display the queue contents.
5. Delete and display elements one by one until the queue is empty.

## Program

```python
class PriorityQueue(object):
    def __init__(self):
        self.queue = []

    def __str__(self):
        return ' '.join([str(i) for i in self.queue])

    def isEmpty(self):
        return len(self.queue) == 0

    def insert(self, data):
        self.queue.append(data)

    def delete(self):
        if self.isEmpty():
            return "Queue is empty"
        
        max_value = max(self.queue)  
        self.queue.remove(max_value)
        return max_value  

# Create PriorityQueue object
myQueue = PriorityQueue()

# Input number of elements
n = int(input())

# Insert elements into the queue
for i in range(n):
    ele = int(input())
    myQueue.insert(ele)

# Print current queue
print(myQueue)

# Delete elements in order of priority
while not myQueue.isEmpty():
    print(myQueue.delete())
```

## output
![Screenshot 2025-04-20 213334](https://github.com/user-attachments/assets/268df4fa-2622-4f23-9bf1-641335f62318)

## Result
The program successfully implements a priority queue, inserting and deleting elements based on priority (maximum value first).
