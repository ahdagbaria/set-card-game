# Set Card Game — Concurrent Java Implementation

A multi-threaded implementation of the **Set card game**, focused on solving real-world concurrency challenges using Java.  
Built as part of an academic project, emphasizing **thread synchronization, fairness, and performance**.

> **Authors:** Ahd Agbaria & Hadeel Ganem

---

## About the game

Set is a real-time pattern-matching card game. The deck contains 81 cards, each with four features (color, number, shape, shading). A **legal set** is three cards where every feature is *either all the same or all different* across the three. Players compete simultaneously to find sets on a 3×4 grid — correct claims score a point, incorrect claims trigger a freeze penalty.

---

## Highlights

- Designed a **concurrent game engine** with multiple interacting threads (Dealer & Players)
- Implemented **thread-safe synchronization mechanisms**
- Ensured **fair scheduling (FIFO)** for player actions
- Supported both **human and AI players**
- Maintained responsiveness under concurrent workloads


---


---

## Build & run

```bash
mvn clean compile exec:java   # build and run the game
mvn test                      # run unit tests
```

---


---

## What I learned

This was the project where Java threading really clicked for me. The hardest parts weren't the synchronization primitives themselves — they were figuring out *where* synchronization was actually needed versus where it would be redundant, and designing the dealer–player handshake so that no one waits longer than they have to.