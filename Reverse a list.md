# Reverse a list

- Write an algorithm to reverse a linked list. 
  - The time complexity of your algorithm should be linear (O(n)). 

For this exercise, notice we are not asking you just to print the linked list in reverse or use another linked list to store the value in reverse order. 
- Your program should reverse the direction of a given singly linked list. In other words, all pointers should point backward.

````
function reverseLL(linkedList) {
  if (this.isEmpty) {
      return 'list is empty'
    }
  
  let current = linkedList.head
  let previous = null
  let next = null
  
  while (current !== null) {
    next = current.next
    current.next = previous
    previous = current
    current = next
  }
  linkedList.head = previous
}

````
* BONUS: Solve this problem using both recursive and iterative algorithms.
