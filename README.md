# DataStructureImplementations

### Linked List:-

## In C++
### Using Structures

```c++
#include <bits/stdc++.h>
using namespace std;
struct Node
{
    int data;
    struct Node *next;
};
struct Node *head = NULL; // a pointer that points to struct type node

void insert(int val)
{
    struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));
    newNode->data = val;
    newNode->next = NULL;
    if (head == NULL)
    {
        head = newNode;
    }
    else
    {
        struct Node *temp = head;
        while (temp->next != NULL)
        {
            temp = temp->next;
        }
        temp->next = newNode;
    }
}
void display()
{
    struct Node *ptr = head;
    while (ptr != NULL)
    {
        cout << ptr->data << " ";
        ptr = ptr->next;
    }
}
int main()
{
    insert(1);
    insert(2);
    insert(3);
    insert(4);
    insert(5);
    display();
    return 0;
}

```

## Using Classes in C++
- required a node class to create nodes
- require a linked list class to perform operations like insertion,deletion,searching,traversing

```c++
#include<iostream>
using namespace std;
class Node{
    public:
      int data;
      Node* next;
      
      Node(){
          data = 0;
          next = NULL;
      }
      Node(int val){
          this->data = val;
          this->next = NULL;
      }
};
class linkedList{
    Node* head;
public:
       linkedList(){
           head = NULL;
       }
       void insertNode(int);
       void display();
};
void linkedList::insertNode(int data){
    Node* newNode = new Node(data);
    if(head==NULL){
        head = newNode;
        return;
    }
    else{
        Node* temp = head;
        while(temp->next!=NULL){
            temp = temp->next;
        }
        temp->next = newNode;
    }
    
};

void linkedList::display(){
    Node* ptr = head;
    if (head == NULL) {
		cout << "List empty" << endl;
		return;
	}
    while(ptr!=NULL){
        cout << ptr->data;
        ptr = ptr->next;
    }
}

int main(){
    linkedList obj;
    obj.insertNode(1);
    obj.insertNode(2);
    obj.insertNode(3);
    obj.display();
    return 0;
}

```

## In Python 
- using classes similar to c++

```python
class Node:
    def __init__(self,data=None):
        self.data = data
        self.nextNode = None
class LinkedList:
    def __init__(self):
        self.head = None
        
        
    def insertNode(self,data):
        newNode = Node(data)
        
        if self.head is None:
            self.head = newNode
            return
           
        else:
            temp = self.head
            while temp.nextNode:
                temp = temp.nextNode
            temp.nextNode = newNode
    def display(self):
        ptr = self.head
        while ptr is not None:
            print(ptr.data)
            ptr = ptr.nextNode
            
obj = LinkedList()


obj.insertNode(1);
obj.insertNode(2);
obj.insertNode(3);
obj.insertNode(4);
obj.insertNode(5);
obj.display();

```

## In Java
- using classes same as c++
```java
class Node{
    public int data;
    public Node next;
    public Node(){
        data = 0;
        next = null;
    }
    public Node(int data){
        this.data = data;
        this.next = null;
    }
}
public class linkedList{
    Node head;
    public linkedList(){
        head = null;
    }
    public void insertNode(int data){
        Node newNode = new Node(data);
        if(head==null){
            head = newNode;
        }
        else{
            Node temp = head;
            while(temp.next!=null){
                temp = temp.next;
            }
            temp.next = newNode;
        }
    }
    public void display(){
        Node ptr = head;
        while(ptr!=null){
            System.out.println(ptr.data);
            ptr = ptr.next;
        }

    }
    public static void main(String[] args){
        linkedList obj = new linkedList();
        obj.insertNode(1);
        obj.insertNode(2);
        obj.insertNode(3);
        obj.insertNode(4);
        obj.display();
       
    }
}
```

## Graphs in C++

```c++
#include<iostream>
#include<vector>
using namespace std;
int main(){
    int n = 5;
    int m = 6;
    int u,v;
    vector<int> graph[n+1];
    for(int i=0;i<m;i++){
        cin>>u>>v;
        graph[u].push_back(v);
    }
    for(int i=1;i<=n;i++){
        for(auto x:graph[i]){
            cout<<x<<" ";
        }
    }
    return 0;
}
```



