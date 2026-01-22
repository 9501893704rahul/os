# Operating System - Lesson 4: Complete Notes

## SJF Scheduling, Round Robin & Spooling Concepts

---

## Table of Contents

1. [Shortest Job First (SJF) Scheduling](#1-shortest-job-first-sjf-scheduling)
2. [SJF Example with Calculations](#2-sjf-example-with-calculations)
3. [Round Robin Scheduling](#3-round-robin-scheduling)
4. [Round Robin Example with Calculations](#4-round-robin-example-with-calculations)
5. [Preemptive vs Non-Preemptive Summary](#5-preemptive-vs-non-preemptive-summary)
6. [Spooling Concept](#6-spooling-concept)
7. [Important MCQs](#7-important-mcqs)
8. [Summary & Key Points](#8-summary--key-points)

---

## 1. Shortest Job First (SJF) Scheduling

### Definition

> **SJF** = Process with the **shortest burst time** gets served first!

| Property | Value |
|----------|-------|
| **Mode** | Non-Preemptive |
| **Priority** | Smaller Burst Time = Higher Priority |
| **Comparison** | Required to determine shortest job |

### Key Rules

1. **Smaller burst time** = Higher priority
2. **Larger burst time** = Lower priority
3. Need **comparison** to determine which job is shorter
4. **First job** has no comparison - runs immediately

### When Burst Times are Equal

> If two jobs have **same burst time**, priority is given based on **Arrival Time** (who came first).

### Real-Life Analogy

Imagine a hotel owner says: "Whoever eats less will be served first, whoever eats more will be served later." That's SJF - shortest job (smallest burst time) gets priority!

---

## 2. SJF Example with Calculations

### Given Data

| Process | Arrival Time (AT) | Burst Time (BT) |
|---------|-------------------|-----------------|
| P1 | 0 | 7 |
| P2 | 1 | 5 |
| P3 | 2 | 3 |
| P4 | 3 | 1 |
| P5 | 4 | 2 |
| P6 | 5 | 1 |

### Step-by-Step Solution

**Step 1:** P1 arrives first (AT=0) - No comparison needed, goes to CPU immediately. WT=0

**Step 2:** While P1 processes (0-7), all other jobs arrive in Ready Queue: P2, P3, P4, P5, P6

**Step 3:** Compare burst times after P1 completes:
- P4 = 1 (smallest)
- P6 = 1 (same as P4, but arrived later)
- P5 = 2
- P3 = 3
- P2 = 5 (largest)

**Step 4:** P4 and P6 have same BT, so check AT:
- P4 arrived at 3
- P6 arrived at 5
- P4 goes first!

### Execution Order

```
P1 → P4 → P6 → P5 → P3 → P2
```

### Gantt Chart

```
|----P1----|--P4--|--P6--|--P5--|---P3---|-----P2-----|
0          7      8      9      11       14           19
```

### Complete Calculations

| Process | AT | BT | CT | TAT (CT-AT) | WT (TAT-BT) | RT |
|---------|----|----|----|----|----|----|
| P1 | 0 | 7 | 7 | 7 | 0 | 0 |
| P2 | 1 | 5 | 19 | 18 | 13 | 13 |
| P3 | 2 | 3 | 14 | 12 | 9 | 9 |
| P4 | 3 | 1 | 8 | 5 | 4 | 4 |
| P5 | 4 | 2 | 11 | 7 | 5 | 5 |
| P6 | 5 | 1 | 9 | 4 | 3 | 3 |

### Key Observation

> In SJF (Non-Preemptive), **Waiting Time = Response Time** for all processes!

This is true for ALL Non-Preemptive scheduling algorithms.

---

## 3. Round Robin Scheduling

### Definition

> Each process gets a small unit of CPU time called **Time Quantum**. After this time expires, process is preempted and added to end of Ready Queue.

| Property | Value |
|----------|-------|
| **Mode** | Preemptive |
| **Key Concept** | Time Quantum (Time Slice) |
| **Typical Quantum** | 10-100 milliseconds |

### How It Works

1. Each process gets a **fixed time slice** (Time Quantum)
2. After time quantum expires, process is **preempted**
3. Process goes back to **end of Ready Queue**
4. Next process in queue gets CPU
5. Cycle continues until all processes complete

### Real-Life Analogy

Like a hotel that says: "No matter how hungry you are, we'll give only 2 rotis at a time. Want more? Go back in line!" Everyone gets fair share!

### Key Features

- **Prevents CPU monopolization**
- **Fair distribution** of CPU time
- Process may visit CPU **multiple times**
- **WT ≠ RT** (usually different)

---

## 4. Round Robin Example with Calculations

### Given Data

| Process | Arrival Time (AT) | Burst Time (BT) |
|---------|-------------------|-----------------|
| P1 | 0 | 5 |
| P2 | 1 | 3 |
| P3 | 2 | 1 |
| P4 | 3 | 2 |
| P5 | 4 | 3 |

**Time Quantum = 2 units**

### Step-by-Step Execution

| Step | Process | Action | Remaining BT | Queue After |
|------|---------|--------|--------------|-------------|
| 1 | P1 | Process 2 units (0→2) | 3 | P2, P3, P1 |
| 2 | P2 | Process 2 units (2→4) | 1 | P3, P1, P4, P5, P2 |
| 3 | P3 | Process 1 unit (4→5) | 0 | P1, P4, P5, P2 (P3 exits) |
| 4 | P1 | Process 2 units (5→7) | 1 | P4, P5, P2, P1 |
| 5 | P4 | Process 2 units (7→9) | 0 | P5, P2, P1 (P4 exits) |
| 6 | P5 | Process 2 units (9→11) | 1 | P2, P1, P5 |
| 7 | P2 | Process 1 unit (11→12) | 0 | P1, P5 (P2 exits) |
| 8 | P1 | Process 1 unit (12→13) | 0 | P5 (P1 exits) |
| 9 | P5 | Process 1 unit (13→14) | 0 | Empty (P5 exits) |

### Gantt Chart

```
|P1|P2|P3|P1|P4|P5|P2|P1|P5|
0  2  4  5  7  9  11 12 13 14
```

### Complete Calculations

| Process | AT | BT | CT | TAT (CT-AT) | WT (TAT-BT) | RT (First CPU - AT) |
|---------|----|----|----|----|----|----|
| P1 | 0 | 5 | 13 | 13 | 8 | 0 |
| P2 | 1 | 3 | 12 | 11 | 8 | 1 |
| P3 | 2 | 1 | 5 | 3 | 2 | 2 |
| P4 | 3 | 2 | 9 | 6 | 4 | 4 |
| P5 | 4 | 3 | 14 | 10 | 7 | 5 |

### Response Time Calculation

**Formula:** RT = CPU First Arrival - Original Arrival Time

| Process | First CPU Arrival | AT | RT |
|---------|-------------------|----|----|
| P1 | 0 | 0 | 0 |
| P2 | 2 | 1 | 1 |
| P3 | 4 | 2 | 2 |
| P4 | 7 | 3 | 4 |
| P5 | 9 | 4 | 5 |

### Key Observation

> In Round Robin (Preemptive), **WT ≠ RT**!

This is because processes visit CPU multiple times.

---

## 5. Preemptive vs Non-Preemptive Summary

### Comparison Table

| Feature | Non-Preemptive | Preemptive |
|---------|----------------|------------|
| **Examples** | FCFS, SJF | Round Robin |
| **Process Execution** | Start to finish | In small chunks |
| **Switching** | No mid-process switching | Frequent switching |
| **CPU Monopolization** | Possible | Prevented |
| **WT vs RT** | **WT = RT** (always) | **WT ≠ RT** (usually) |

### Analogy

| Type | Real-Life Example |
|------|-------------------|
| **Non-Preemptive** | Visiting doctor for fever - one visit, done |
| **Preemptive** | Being hospitalized - doctor visits multiple times over days |

### Important Exam Question

> **Q:** Which scheduling prevents CPU monopolization?
> 
> **A:** Preemptive Scheduling (like Round Robin)

---

## 6. Spooling Concept

### When is Spooling Used?

> When **User's requirement > Machine's execution power**

### SPOOL Full Form

```
SPOOL = Simultaneous Peripheral Operations Online
```

### Real-Life Analogy

Think of a barber shop on Sunday:
- Many customers (high input)
- Barber can only cut one person's hair at a time (limited execution)
- A queue forms!

Similarly, when input is more than execution capacity, a queue (spool) forms.

### Key Insight

> If input speed = execution speed, **no queue forms**!

### Best Example: Printer

**Scenario:** Computer Lab with Shared Printer

- 5 Computers (A, B, C, D, E) connected to 1 Printer via Network

**What Happens:**

1. Computer A sends 20-page print job
2. While printing, Computer B sends 25-page job
3. Computer C sends 15-page job
4. Computer D sends 30-page job

**Result:**
- Jobs form a **queue** (First Come First Serve)
- A's 20 pages won't stop for B's larger job
- C's smaller job won't jump the queue
- This queue area is called **SPOOL**

### Important Points

| Point | Description |
|-------|-------------|
| **To Cancel Print Job** | Go to Spooler (Print Queue Manager) |
| **Shareable Device** | Printer is shareable in network |
| **Scheduling Used** | First Come First Serve (FCFS) |
| **Queue Location** | Memory area called SPOOL |

---

## 7. Important MCQs

### Operating System Basics

| Question | Answer |
|----------|--------|
| OS that allows only one user at a time? | Single User OS (e.g., DOS) |
| BIOS full form? | Basic Input Output System |
| BIOS is also called? | Firmware |
| What acts as interface between user and hardware? | Operating System |

### Booting

| Question | Answer |
|----------|--------|
| Cold Boot? | Starting computer from OFF state |
| Warm Boot? | Restarting computer (Ctrl+Alt+Delete) |
| Who created Ctrl+Alt+Delete? | David Bradley |

### Shortcuts

| Shortcut | Function |
|----------|----------|
| Ctrl+Alt+Delete | Restart / Task Manager |
| Ctrl+Shift+Escape | Direct Windows Task Manager |

### Other Important MCQs

| Question | Answer |
|----------|--------|
| Log Off means? | Switch from one account to another within a computer |
| Sleep mode? | Programs remain in RAM, low power state |
| UNIX is typically used for? | Servers (First choice for server OS) |
| Which scheduling prevents monopolization? | Preemptive Scheduling |
| Jobs executed as a group? | Batch Processing |
| Shareable device in network? | Printer |
| SPOOL full form? | Simultaneous Peripheral Operations Online |

### Memory Management

| Question | Answer |
|----------|--------|
| Breaking task into blocks/portions? | Paging |
| What plays important role in memory management? | Paging |

### Multi-Processing

| Question | Answer |
|----------|--------|
| More than one CPU? | Multi-Processing |
| Time quantum based scheduling? | Multi-Tasking |

---

## 8. Summary & Key Points

### Scheduling Algorithms Summary

| Algorithm | Mode | Priority Based On | WT vs RT |
|-----------|------|-------------------|----------|
| FCFS | Non-Preemptive | Arrival Time | WT = RT |
| SJF | Non-Preemptive | Burst Time (shortest first) | WT = RT |
| Round Robin | Preemptive | Time Quantum | WT ≠ RT |

### Formula Summary

```
┌─────────────────────────────────────────────────────┐
│  Turn Around Time (TAT) = Completion Time - Arrival Time  │
│                    TAT = CT - AT                          │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│  Waiting Time (WT) = Turn Around Time - Burst Time       │
│                 WT = TAT - BT                            │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│  Response Time (RT) = CPU First Arrival - Arrival Time   │
│                  RT = CPU_FA - AT                        │
└─────────────────────────────────────────────────────┘
```

### SJF Special Rule

> When Burst Times are equal, use **Arrival Time** to decide priority (who came first).

### Round Robin Key Points

1. Uses **Time Quantum** (fixed time slice)
2. Process goes to **end of queue** after quantum expires
3. **Preemptive** - prevents monopolization
4. **WT ≠ RT** because process visits CPU multiple times

### Spooling Key Points

1. **SPOOL** = Simultaneous Peripheral Operations Online
2. Used when input > execution capacity
3. **Printer** is best example
4. Uses **FCFS** scheduling
5. Printer is **shareable device** in network

### Important Full Forms

| Abbreviation | Full Form |
|--------------|-----------|
| SPOOL | Simultaneous Peripheral Operations Online |
| BIOS | Basic Input Output System |
| FCFS | First Come First Serve |
| SJF | Shortest Job First |
| AT | Arrival Time |
| BT | Burst Time |
| CT | Completion Time |
| TAT | Turn Around Time |
| WT | Waiting Time |
| RT | Response Time |

---

## Quick Revision Points

1. ✅ SJF = Shortest Burst Time gets priority
2. ✅ When BT equal, use AT to decide
3. ✅ Non-Preemptive: WT = RT (always)
4. ✅ Preemptive: WT ≠ RT (usually)
5. ✅ Round Robin uses Time Quantum
6. ✅ Round Robin prevents CPU monopolization
7. ✅ SPOOL = Simultaneous Peripheral Operations Online
8. ✅ Printer is shareable device in network
9. ✅ Spooling uses FCFS scheduling
10. ✅ Cold Boot = Start from OFF, Warm Boot = Restart
11. ✅ Ctrl+Alt+Delete created by David Bradley
12. ✅ Ctrl+Shift+Escape = Direct Task Manager

---

## Next Topic

**MS Word** - Starting from next class!

---

*Notes prepared from Operating System Lesson 4*
*Computer Foundation Course - Khan Global Studies*
