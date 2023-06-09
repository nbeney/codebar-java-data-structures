# codebar-java-data-structures

## Empty list

```mermaid
flowchart LR
    classDef LIST fill:pink
    classDef NODE fill:lightgreen

    L[LIST]:::LIST
```

* head == tail
* head == null
* tail == null

## List with 1 element

```mermaid
flowchart LR
    classDef LIST fill:pink
    classDef NODE fill:lightgreen

    L[LIST]:::LIST
    N1[Alice]:::NODE
    L -.->|head| N1
    L -.->|tail| N1
```

* head == tail
* head != null
* tail != null

## List with 2 elements

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

* head != tail
* head != null
* tail != null

## List with 3 elements

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

* head != tail
* head != null
* tail != null

## List with 4 elements

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

* head != tail
* head != null
* tail != null
