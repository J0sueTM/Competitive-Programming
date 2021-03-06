# Stack

A stack is a linear data structure - works in O(n) - in which the elements are stored in a formation called FILO (first in last out) or LIFO (last in first out).
In a more counter-intuitive idea, you can think about stacks like a "stack of plates". Operations are done in those two just presented modes. The first element will be handled last, while the last inserted element will be handled first. 

## Operations

- *Push* Adds an item. If the stack is already full, it's a stack overflow.
- *Pop* Removes the last pushed item from the stack. If the stack is empty, it's a stack underflow.
- *Top* Gets the top element from the stack.
- *isEmpty* Verifyies whether the stack is empty or not.

## Implementation

There are two general methods for implementing the stack: array and lined list

*Array*

```
class Stack:
    Stack(integer stackCapacity):
        this.stackArray = new array[stackCapacity + 1]
        this.stackCurrentTop = 0
        this.stackSize = stackCapacity
    end

    function isEmpty():
        return this.stackCurrentTop == 0
    end

    function isFull():
        return this.stackCurrentTop == this.stackSize - 1;
    end

    function push(integer newData);
        if isFull():
            return 2147483648 # stack overflow
        end

        ++this.stackCurrentTop
        this.stackArray[this.stackCurrentTop] = newData

        return this.stackArray[this.stackCurrentTop]
    end

    function pop():
        if isEmpty():
            return -2147483648 # stack underflow
        end

        integer poppedData = this.stackArray[this.stackCurrentTop]
        this.stackArray[this.stackCurrentTop] = 0
        --this.stackCurrentTop

        return poppedData
    end

    function top():
        if isEmpty():
            return -2147483648 # stack underflow
        end

        return this.stackArray[this.stackCurrentTop]
    end
end
```

*Linked List*

```
class Node:
    integer data
    Node next

    Node(_data):
        this.data = _data
        this.next = null
    end
end

function push(integer newData, Node rootNode):
    newNode = Node(newData)
    newNode.next = rootNode

    rootNode = newNode
end

function pop(Node rootNode):
    if not isEmpty(rootNode):
        tempNode = rootNode
        rootNode = rootNode.next
        delete(rootNode)        

        return rootNode.data 
    end

    return -2147483648 # stack underflow
end

function top(Node rootNode):
    if not isEmpty(rootNode):
        return rootNode.data
    end

    return -2147483648 # stack underflow
end

function isEmpty(Node rootNode):
    if rootNode.next is null:
        return true
    else:
        return false
    end
end
```
