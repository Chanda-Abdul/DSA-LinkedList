# Supplemental functions for a linked list

Implement the following functions that operate on your linked list class. Note that these should be free functions instead of methods of the linked list class, so implement them outside the linked list class. Test each function using the list created in exercise 1.

- display: displays the linked list size: returns the size of the linked list
```
function display(linkedList) {
  //displays the linked list size: returns the size of the linked list
  function size(linkedList) {
    let counter = 0
    let current = linkedList.head
    while (current !== null) {
      current = current.next
      counter ++
    }
    return counter
  }
}
```

- isEmpty: finds if the list is empty or not (without using the size() function) 
```
function isEmpty(linkedList) {
  //finds if the list is empty or not (without using the size() function)
  return (linkedList.head === null)
}
```

- findPrevious: finds the node before the item you are looking for 
```
function findPrevious(linkedList, key) {
   //finds the node before the item you are looking for
  if(isEmpty(linkedList)) {
    return 'list is empty'
  }
  if(linkedList.head.value === key) {
    return 'no previous item'
  } else {
    let current = linkedList.head
    let previous = linkedList.head
    while (current !== null && current.value !== key) {
      previous = current
      current = current.next
    }
    if (current === null) {
      return 'Item not found'
    }
    return previous
  }
}
```

- findLast: returns the last node in the linked list
```
function findLast(linkedList) {
 //returns the last node in the linked list
  if (isEmpty(linkedList)) {
    return 'List is empty'
  }
  let current = linkedList.head
  while (current.next !== null) {
    current = current.next
  }
  return current
}
```
