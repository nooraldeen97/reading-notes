
## Stacks & Queues<br>
## What is a Stack<br>

**A stack is a data structure that consists of Nodes. Each Node references only the next Node in the stack, and<br> follow these concepts: FILO, and LIFO.**<br>

Common terminology for a stack:<br>
1- Push<br>

2- Pop<br>

3- Top<br>

4- Peek<br>

5- IsEmpty<br>


**Stack Visualization**<br>
The topmost item is denoted as the top. When you push something to the stack, it becomes the new top. When you<br> pop something from the stack, you pop the current top and set the next top as top.next.<br>

<hr>

![my-image](https://4cawmi2va33i3w6dek1d7y1m-wpengine.netdna-ssl.com/wp-content/uploads/2018/07/Computer-science-fundamentals_6.1.png)

<hr>


Push O(1)<br>
Pushing a Node onto a stack will always be an O(1) operation.<br>

The pseudocode to push a value onto a stack:<br>

< // INPUT <-- value to add, wrapped in Node internally<br>

// OUTPUT <-- none<br>

node = new Node(value)<br>

node.next <-- Top<br>

top <-- Node<br>

**Pop O(1)**<br>
The pseudocode to pop a value onto a stack:<br>

< // INPUT <-- No input<br>

// OUTPUT <-- value of top Node in stack<br>

// EXCEPTION if stack is empty<br>

Node temp <-- top<br>

top <-- top.next<br>

temp.next <-- null<br>

return temp.value<br>

**Peek O(1)**<br>
The pseudocode to peek a value onto a stack:<br>

< // INPUT <-- none<br>

// OUTPUT <-- value of top Node in stack<br>

// EXCEPTION if stack is empty<br>

return top.value<br>

**IsEmpty O(1)**<br>
The pseudocode to peek a value onto a stack:<br>

< // INPUT <-- none<br>

// OUTPUT <-- boolean<br>

return top = NULL<br>

## What is a Queue

**Common terminology for a queue is:**<br>

1- Enqueue O(1)<br>

< // INPUT <-- value to add to queue (will be wrapped in Node internally)<br>

// OUTPUT <-- none<br>

node = new Node(value)<br>

rear.next <-- node<br>

rear <-- node<br>

2- Dequeue O(1)<br>

< // INPUT <-- none // OUTPUT <-- value of the removed Node<br>

// EXCEPTION if queue is empty<br>

Node temp <-- front<br>

front <-- front.next<br>

temp.next <-- null<br>

return temp.value<br>

3- Front<br>

4- Rear<br>

5- Peek<br>

< // INPUT <-- none<br>

// OUTPUT <-- value of the front Node in Queue<br>

// EXCEPTION if Queue is empty<br>

return front.value<br>

6- IsEmpty<br>

< // INPUT <-- none<br>

// OUTPUT <-- boolean<br>

return front = NULL<br>

Queues follow FIFO, and LILO.<br>