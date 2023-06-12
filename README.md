# codebar-java-data-structures

## Class diagram

```mermaid
classDiagram
    class Node["Node&lt;T&gt;"] {
        T value
        Node previous
        Node next
        +String toString()
    }

    Node --> "0..1" Node : previous
    Node --> "0..1" Node : next

    class List["List&lt;T&gt;"] {
        -Node head
        -Node tail
        +int size()
        +void add(T elt)
        +void push(T elt)
        +T pop()
        +Iterator iter()
    }

    List --> "0..1" Node : head
    List --> "0..1" Node : tail

    class ListIterator["ListIterator&lt;T&gt;"] {
        -Node current
        +boolean hasNext()
        +T next()
    }

    ListIterator ..> Node : current
```

## Empty list

* The head and the tail are identical (`head == tail`).
* There is no head and no tail (`head == null && tail == null`).
* There are no nodes.

```mermaid
flowchart LR
    classDef LIST fill:pink
    classDef NODE fill:lightgreen

    L[LIST]:::LIST
```

## List with a single element

* The head and the tail are identical (`head == tail`).
* There is a head and a tail (`head != null && tail != null`).
* The single node has no predecessor and no successor (`previous == null && next == null`).

```mermaid
flowchart LR
    classDef LIST fill:pink
    classDef NODE fill:lightgreen

    L[LIST]:::LIST
    N1[Alice]:::NODE
    L -.->|head| N1
    L -.->|tail| N1
```

## List with multiple elements

* The head and the tail are different (`head != tail`).
* There is a head and a tail (`head != null && tail != null`).
* The first node (head) has no predecessor and a successor (`previous == null && next != null`).
* The middle nodes, if any, have a predecessor and a successor (`previous != null && next != null`).
* The last node (tail) has a predecesssor and no successor (`previous != null && next == null`).

```mermaid
flowchart LR
    classDef LIST fill:pink
    classDef NODE fill:lightgreen

    L[LIST]:::LIST
    N1[Alice]:::NODE
    N2[Bob]:::NODE
    L -.->|head| N1
    L -.->|tail| N2
    N1 -->|next| N2
    N2 -->|prev| N1
```

```mermaid
flowchart LR
    classDef LIST fill:pink
    classDef NODE fill:lightgreen

    L[LIST]:::LIST
    N1[Alice]:::NODE
    N2[Bob]:::NODE
    N3[Cloe]:::NODE
    L -.->|head| N1
    L -.->|tail| N3
    N1 -->|next| N2
    N2 -->|prev| N1
    N2 -->|next| N3
    N3 -->|prev| N2
```

```mermaid
flowchart LR
    classDef LIST fill:pink
    classDef NODE fill:lightgreen

    L[LIST]:::LIST
    N1[Alice]:::NODE
    N2[Bob]:::NODE
    N3[Cloe]:::NODE
    N4[David]:::NODE
    L -.->|head| N1
    L -.->|tail| N4
    N1 -->|next| N2
    N2 -->|prev| N1
    N2 -->|next| N3
    N3 -->|prev| N2
    N3 -->|next| N4
    N4 -->|prev| N3
```
