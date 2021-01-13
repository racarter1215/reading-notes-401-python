A few things I learned regarding Stacks and Queues:

Stacks:

There are five main commands when mainuplating a stack:
Push: "Pushes" nodes within a stack
Pop: Removing nodes from stack.
Top: Top node of a stack
Peek: Viewing the top node of a stack
IsEmpty: True when no nodes in stack, false otherwise.

First in Last Out (FILO): The first item added in stack will be the last one popped off.
Last in First Out (LIFO): The last item added in stack will be the first one popped off.

Push algorithm:
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node

Pop algorithm:
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value
   
Peek algorithm:
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   return top.value

IsEmpty algorithm:
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL

Queues:

There are five main commands when mainuplating a queue:
Enqueue: Added nodes/items in a queue
Dequeue: Nodes/items removed from queue
Front: a queue's first/front node
Rear: a queue's rear/last node
Peek: View the front node's value
IsEmpty: True when no nodes in stack, false otherwise.

First in Last Out (FILO): The first item added in queue will be the last one dequeued.
Last in First Out (LIFO): The last item added in queue will be the first one dequeued.

Enqueue algorithm:
ALGORITHM enqueue(value)
// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
   node = new Node(value)
   rear.next <-- node
   rear <-- node

Dequeue algorithm:
ALGORITHM dequeue()
// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty

   Node temp <-- front
   front <-- front.next
   temp.next <-- null

   return temp.value

Peek algorithm:
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of the front Node in Queue
// EXCEPTION if Queue is empty

   return front.value

IsEmpty algorithm:
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return front = NULL



