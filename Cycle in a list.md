# Cycle in a list

Write an algorithm to find whether a linked list has a cycle (i.e., whether a node in the list has its next value pointing to an earlier node in the list). For this exercise, create a linked list with the name CycleList. Be sure to insert nodes in the list so that it has a cycle. Then test your program with a cycleList function.

````
function cycle(linkedList) {
  let first = linkedList.head
  let second = linkedList.head
  
  while((second !== null) && (second.next !== null)) {
    second = second.next.next
    first = first.next
    if (second.value === first.value) {
      return true
    }
  }
  return false
  
}

function main() {
	const CycleList = new LinkedList;
	
	CycleList.insertLast(1);
	CycleList.insertLast(2);
	CycleList.insertLast(3);
	CycleList.insertLast(4);
	CycleList.insertLast(5);
	CycleList.insertLast(6);
	CycleList.insertLast(7);
	CycleList.insertLast(8);
	CycleList.insertLast(9);
  
	CycleList.find(6)
	CycleList.find(1)

	console.log(cycle(CycleList), "cycle");
}
````
