# GitHub Mermaid Rendering Probe (2026-06-11)

## 00 info (version probe)

```mermaid
info
```

## 01 flowchart

```mermaid
flowchart TD
    A[Start] --> B{Check}
    B -->|yes| C[Done]
    B -->|no| A
```

## 02 sequenceDiagram

```mermaid
sequenceDiagram
    Alice->>Bob: Hello
    Bob-->>Alice: Hi
```

## 03 classDiagram

```mermaid
classDiagram
    class Order {
        +int amount
        +confirm()
    }
    Order <|-- RushOrder
```

## 04 stateDiagram-v2

```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Running: start
    Running --> [*]
```

## 05 erDiagram

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE_ITEM : contains
```

## 06 journey

```mermaid
journey
    title My day
    section Work
      Code: 5: Me
      Review: 3: Me
```

## 07 gantt

```mermaid
gantt
    title Plan
    dateFormat YYYY-MM-DD
    section A
    Task1 :a1, 2026-06-01, 3d
    Task2 :after a1, 2d
```

## 08 pie

```mermaid
pie title Pets
    "Dogs" : 40
    "Cats" : 60
```

## 09 gitGraph

```mermaid
gitGraph
    commit
    branch develop
    commit
    checkout main
    merge develop
```

## 10 C4Context

```mermaid
C4Context
    title System Context
    Person(user, "User")
    System(sys, "System")
    Rel(user, sys, "uses")
```

## 11 mindmap

```mermaid
mindmap
  root((idea))
    A
      A1
    B
```

## 12 timeline

```mermaid
timeline
    title History
    2024 : v1
    2025 : v2
    2026 : v3
```

## 13 quadrantChart

```mermaid
quadrantChart
    title Reach vs Effort
    x-axis Low Reach --> High Reach
    y-axis Low Effort --> High Effort
    quadrant-1 Plan
    quadrant-2 Do
    quadrant-3 Skip
    quadrant-4 Maybe
    A: [0.3, 0.6]
    B: [0.7, 0.2]
```

## 14 requirementDiagram

```mermaid
requirementDiagram
    requirement req1 {
      id: 1
      text: must work
      risk: high
      verifymethod: test
    }
    element sys {
      type: system
    }
    sys - satisfies -> req1
```

## 15 sankey-beta

```mermaid
sankey-beta
A,B,10
A,C,5
B,D,8
```

## 16 xychart-beta

```mermaid
xychart-beta
    title "Sales"
    x-axis [jan, feb, mar]
    y-axis "Revenue" 0 --> 100
    bar [20, 50, 80]
    line [10, 40, 90]
```

## 17 block-beta

```mermaid
block-beta
columns 3
  a b c
  d:3
```

## 18 packet-beta

```mermaid
packet-beta
0-15: "Source Port"
16-31: "Destination Port"
```

## 19 kanban

```mermaid
kanban
  Todo
    t1[Write docs]
  Done
    t2[Ship it]
```

## 20 architecture-beta

```mermaid
architecture-beta
    group api(cloud)[API]
    service db(database)[DB] in api
    service web(server)[Web] in api
    web:R -- L:db
```

## 21 radar-beta

```mermaid
radar-beta
  axis a["A"], b["B"], c["C"]
  curve x{3, 4, 5}
  max 10
```

## 22 treemap-beta

```mermaid
treemap-beta
"Root"
    "Child A": 30
    "Child B": 70
```

## 23 zenuml (external plugin)

```mermaid
zenuml
    title Demo
    A->B: hello
```

## 24 Korean text probe (flowchart)

```mermaid
flowchart LR
    A[주문 생성] --> B{재고 확인}
    B -->|충분| C[결제 진행]
    B -->|부족| D[입고 대기 — 알림 발송]
```

## 25 Korean text probe (sequenceDiagram)

```mermaid
sequenceDiagram
    participant 사용자
    participant 서버
    사용자->>서버: 장바구니 담기 요청
    서버-->>사용자: 룰렛 게이지 갱신 응답
```

## 26 click interaction probe

```mermaid
flowchart LR
    A[Click me] --> B[Target]
    click A "https://example.com" "tooltip"
```

## 27 frontmatter config probe

```mermaid
---
config:
  theme: forest
  flowchart:
    curve: linear
---
flowchart LR
    X[Config] --> Y[Applied?]
```
