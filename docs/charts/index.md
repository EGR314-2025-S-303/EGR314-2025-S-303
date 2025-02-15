---
title: Charts
---

## **Block Diagram**
<img src="Team-Block-Diagram.png">

## **Sequence Diagram**
``` mermaid
sequenceDiagram
    Cade-->>+Dan: Start Motor
    Dan-->>-Dan: Start Motor Trash 
    Jahmel-->>+Tyler: Set Motor Speed
    Tyler-->>+Cade: Motor Speed
    Cade-->>+Dan: Motor Speed
    Dan-->>-Dan: Set Motor Speed Trash
    loop Every second
    Tyler-->>+Cade: Sensor Data
    Cade-->>+Dan: Sensor Data
    Dan-->>+Jahmel: Sensor Data
    Jahmel-->>+Tyler: Sensor Data
    Tyler-->>-Tyler: Sesnor Data Trash
    end
```

