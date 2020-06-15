# Middle of a list

- Write an algorithm to find the middle element of a linked list. 
  - Note You may be tempted to add a length property to your linked list class. The length property is not a typical property of linked list, therefore don't make any modification to the linked list class that is provided to you. 
  - Also, finding the size of the linked list using the size() function and dividing it by half will not find the correct middle of the linked list. So, don't use either of these approaches.
  
  ````
  function middle(linkedList) {
  let first = linkedList.head
  let second = linkedList.head
  
  while ((second !== null) && (second.next !== null)) {
    second = second.next.next
    first = first.next
  }
  return first.value
  }
  
  function main() {
	const SLL = new LinkedList;

	SLL.insertLast(1);
	SLL.insertLast(2);
	SLL.insertLast(3);
	SLL.insertLast(4);
	SLL.insertLast(5);
	SLL.insertLast(6);
	SLL.insertLast(7);
	SLL.insertLast(8);
	SLL.insertLast(9);

	console.log(middle(SLL), "middle");
  }
  ````

