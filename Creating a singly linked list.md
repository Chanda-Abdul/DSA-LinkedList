# Creating a singly linked list

- Write a function main. 

````
function main() {
  const SLL = new LinkedList()
  
  SLL.insertLast('Apollo')
  SLL.insertLast('Boomer')
  SLL.insertLast('Helo')
  SLL.insertLast('Husker')
  SLL.insertLast('Starbuck')
  SLL.insertLast('Tauhida')
  SLL.remove('Husker')
  
  SLL.insertBefore("Athena", "Boomer") 
  
  SLL.insertAfter("Hotdog", "Helo") 
  
  SLL.insertAt("Kat", 3)
  
  SLL.remove('Tauhida')
  
  console.log(SLL, "SLL")
}
````
- Within the function, using the linked list class above, create a linked list with the name SLL and add the following items to your linked list: 
  - Apollo, Boomer, Helo, Husker, Starbuck. 
  - Add Tauhida to the list. 
  - Remove Husker from the list. 
  ```
  SLL.insertLast('Apollo')
  SLL.insertLast('Boomer')
  SLL.insertLast('Helo')
  SLL.insertLast('Husker')
  SLL.insertLast('Starbuck')
  SLL.insertLast('Tauhida')
  SLL.remove('Husker')
  ```
  
- Implement a function called `insertBefore()` in the class that inserts a new node before a given node containing a key. 

````
  insertBefore(newItem, beforeItem) {
    if (!this.head) {
      console.log('list was empty')
      this.insertFirst(newItem)
      return
    }
    let currNode = this.head
    let prevNode = this.head
    
    while (currNode !== null && currNode.value !== beforeItem) {
      prevNode = currNode
      currNode = currNode.next
    }
    
    if (currNode === null) {
      this.insertLast(newItem)
      return
    }
    const tempNode = new _Node(newItem, currNode)
    
    prevNode.next = tempNode
  }
  ````
  
- Implement a function called `insertAfter()` in the class that inserts a new node after a node containing the key. 
````
insertAfter(newItem, afterItem) {
    if (this.head === null) {
      this.insertFirst(newItem)
      return
    }
    let currNode = this.find(afterItem)
    
    if(currNode === null) {
      this.insertLast(newItem)
      return
    }
    const tempNode = new _Node(newItem, currNode.next)
    
    currNode.next = tempNode
  }
  
  ````

- Implement a function called `insertAt()` that inserts an item at a specific position in the linked list.
````
insertAt(item, position) {
    if (this.head === null) {
      this.insertFirst(item)
      return
    }
    
    let currNode = this.head
    let currPosition = 1
    
    while (currPosition < position - 1) {
      currNode = currNode.next
      currPosition++
    }
  ````
- Add Athena before Boomer using your insertBefore() function. 
```
 SLL.insertBefore("Athena", "Boomer") 
```
- Add Hotdog after Helo using the insertAfter() method. 
```
SLL.insertAfter("Hotdog", "Helo")
```
- Using the insertAt() method insert Kat in the 3rd position of the list. 
```
SLL.insertAt("Kat", 3)
```
- Remove Tauhida from the list.
```
SLL.remove('Tauhida')
```
