# Design Linked List

**Platform:** LeetCode  
**Link:** https://leetcode.com/problems/design-linked-list/

## Problem
Design a singly linked list supporting get by index, add at head, add at tail, add before an index, and delete at an index.

## Approach
Represent the list with nodes and maintain a head reference plus size. Traverse to the required position for indexed operations and relink nodes for insertion/deletion.

## Java Solution
```java
class MyLinkedList {
    class Node {
        int val; Node next;
        Node(int val) { this.val = val; }
    }
    Node head;
    int size;
    public MyLinkedList() { head = null; size = 0; }
    public int get(int index) {
        if (index < 0 || index >= size) return -1;
        Node current = head;
        for (int i = 0; i < index; i++) current = current.next;
        return current.val;
    }
    public void addAtHead(int val) { Node node = new Node(val); node.next = head; head = node; size++; }
    public void addAtTail(int val) {
        Node node = new Node(val);
        if (head == null) head = node;
        else { Node current = head; while (current.next != null) current = current.next; current.next = node; }
        size++;
    }
    public void addAtIndex(int index, int val) {
        if (index < 0 || index > size) return;
        if (index == 0) { addAtHead(val); return; }
        Node prev = head;
        for (int i = 0; i < index - 1; i++) prev = prev.next;
        Node node = new Node(val); node.next = prev.next; prev.next = node; size++;
    }
    public void deleteAtIndex(int index) {
        if (index < 0 || index >= size) return;
        if (index == 0) head = head.next;
        else { Node prev = head; for (int i = 0; i < index - 1; i++) prev = prev.next; prev.next = prev.next.next; }
        size--;
    }
}
```

## Complexity
| Metric | Complexity |
|---|---|
| Time | O(n) per indexed/traversal operation |
| Space | O(1) |

---

**Practice #20** · DSA Java