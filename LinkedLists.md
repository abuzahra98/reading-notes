# Class 05

## references 

https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html

https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d

https://www.geeksforgeeks.org/linked-list-set-1-introduction/


## Linked Lists

There are two types of linked lists, singly linked, and doubly linked. 

Singly means that each node has one reference in them
doubly means there are two references in each node. 

When traversing a linked list, you cant use for or foreach loops, we depend on the "Next" value of each node. 

Make sure that each node has a value, and points to the next node in the sequence. 






A linked list is a series of nodes tied together like links in a chain, with each node referencing the next in line.

- Singly is the number of references a node has, and a singly-linked list has only one reference which points to the next node
- Doubly linked lists , as you might have guessed have double the references, one with the next node and one with the prior node as well
- Nodes, oft mentioned thus far, are the individual links in the chain and contain their data
- Next is a property of each node that refers to the next node in the link
- Head is a reference to the first node in a linked list
- Current is a reference to the node currently being looked at

Similar to arrays in concept, Linked Lists cannot be traversed through for/forEach loops, and must use a While loop while depending on the Next property defined above.

Sample Code

```Java
public static boolean includes(int value)

Current = Head // makes sure the loop starts at the beginning of the LL

while (Current != null) { //only runs if the current node has a value
  if (Current.value == value){ // checking if the value of current is the value we want. if it is, the loop ends and the method returns true
    return true
  }
  else (Current = Current.Next){ // if it is not the value we are looking for, the value of current is changed to look at the next link
  }
}
    return false // if the value never returns true then the value is not in the LL, therefore the method is false
```

Big O of time for the sample method is O(n), with n representing the nodes within the LL.
Big O of space would be O(1) because nothing is being created in the method, and the space taken up by the LL does not change.

[<== Back to Readme](README.md)