# 3rd from the end

Write an algorithm to find the 3rd element from the end of a linked list. Note You may be tempted to add a length property to your linked list class. The length property is not a typical property of linked list, therefore don't make any modification to the linked list class that is provided to you.

````
function thirdFromTheEnd(linkedList) {
  let current = linkedList.head
  
  if(!current.next.next.next) {
    return null
  }
  
  let tfl = current
  
  while(current.next.next.next !== null) {
    tfl = current
    current = current.next
  }
  return tfl.value
}
````
