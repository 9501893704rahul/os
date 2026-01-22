# Operating System - Lesson 3: Complete Notes

## Multi-Tasking, Multi-Processing, Real-Time OS & CPU Scheduling

---

## Table of Contents

1. [Recap: Multi-Programming Problem](#1-recap-multi-programming-problem)
2. [Multi-Tasking Operating System](#2-multi-tasking-operating-system)
3. [How Multi-Tasking Works](#3-how-multi-tasking-works)
4. [OS Evolution - Software vs Hardware](#4-os-evolution---software-vs-hardware)
5. [Multi-Processing Operating System](#5-multi-processing-operating-system)
6. [Real-Time Operating System (RTOS)](#6-real-time-operating-system-rtos)
7. [Soft RTOS vs Hard RTOS](#7-soft-rtos-vs-hard-rtos)
8. [CPU Scheduling Introduction](#8-cpu-scheduling-introduction)
9. [CPU Scheduling Terms & Formulas](#9-cpu-scheduling-terms--formulas)
10. [Preemptive vs Non-Preemptive](#10-preemptive-vs-non-preemptive)
11. [FCFS Algorithm with Example](#11-fcfs-algorithm-with-example)
12. [Summary & Key Points](#12-summary--key-points)

---

## 1. Recap: Multi-Programming Problem

### The Problem from Last Lesson

In Multi-Programming:
- When CPU is assigned a task, it processes until the task is **completely finished and exits**
- During I/O operations, CPU remains in **IDLE state**
- CPU doesn't process other tasks while waiting

### The Solution: Scheduling

> **Scheduling** = Planning how to complete work with minimum time, minimum effort, and maximum efficiency.

**Analogy:** If 10 students are given the same task, all will complete it but in different times. The one who finishes fastest has better "processing speed" - that's scheduling optimization!

---

## 2. Multi-Tasking Operating System

### Definition

> **Multi-Tasking is the upgraded version of Multi-Programming.**

This exact line has appeared in previous year exam papers!

### Exam Strategy

| Situation | Answer |
|-----------|--------|
| Only Multi-Programming in options | Select Multi-Programming |
| Only Multi-Tasking in options | Select Multi-Tasking |
| BOTH in options | Select **Multi-Tasking** (more advanced) |

### Also Known As

> Multi-Tasking is also called **Time Sharing**

CPU time is shared between multiple users/processes simultaneously.

---

## 3. How Multi-Tasking Works

### The Concept

Instead of completing one program fully before moving to next, CPU **switches between programs** very quickly.

```
Process P1 (bit) → Switch to P2
Process P2 (bit) → Switch to P3
Process P3 (bit) → Switch to P4
Back to P1 → Continue cycle
```

### Real-Life Analogy

Imagine 4 guests come for dinner, each eating 4 rotis. You have only 8 rotis ready.

**Bad approach:** Serve 2 people fully, make others wait hungry.

**Good approach (Multi-Tasking):** Give 1 roti to everyone, then repeat. Everyone feels served!

### Key Insight

| Reality | Perception |
|---------|------------|
| Programs run **ALTERNATIVELY** (one by one) | Programs appear to run **SIMULTANEOUSLY** |

The switching is **SO FAST** that it creates an illusion of simultaneous execution!

---

## 4. OS Evolution - Software vs Hardware

### Evolution Path (Software Level)

```
Batch Processing → Multi-Programming → Multi-Tasking
```

### Important Observation

| Feature | Batch Processing | Multi-Programming | Multi-Tasking |
|---------|-----------------|-------------------|---------------|
| CPU Count | Single | Single | Single |
| Upgrade Type | Software | Software | Software |

**All three use SINGLE PROCESSOR!**

### The Risk

> What if this single processor **FAILS**?

- All software advancements become **useless**
- For systems handling millions of requests, this is a **major problem**
- Solution needed: **Hardware level upgrade**

---

## 5. Multi-Processing Operating System

### Definition

> Multi-Processing OS uses **MORE THAN ONE CPU/Processor** in a single computer system.

### Key Features

- Uses **2 or more CPUs** in single computer
- Multiple processors share: Computer Bus, Clock, Memory
- Resources are shared between processors
- If one processor fails, others continue working
- **Hardware level** advancement (not just software)

### Real-Life Analogy

Think of your family: Dad is the main "processor" earning for everyone. But what if he gets sick? That's why YOU want to become independent - to become another "processor" and share the load!

### Important MCQ Patterns

**Question Type 1:**
> "Which OS allows processing more than one program at a time?"

**Answer:** Multi-Programming

**Question Type 2:**
> "Which OS allows processing more than one program at a time **with help of multiple processors**?"

**Answer:** Multi-Processing

### Comparison Table

| Feature | Multi-Programming | Multi-Tasking | Multi-Processing |
|---------|-------------------|---------------|------------------|
| Number of CPUs | Single | Single | **Multiple** |
| Upgrade Type | Software | Software | **Hardware** |
| Multiple Programs | Yes | Yes | Yes |

---

## 6. Real-Time Operating System (RTOS)

### Main Characteristic

> Tasks are given a **FIXED TIME LIMIT** to complete.

Expected to finish within that time limit!

### Definition

> In RTOS, as soon as input is entered, system provides **IMMEDIATE or QUICK response**.

**RTOS = They are FAST!**

### Real-Life Analogy

Like an exam: You have 2 hours to solve 150 questions. The examiner doesn't need students who can solve 150 questions - they need students who can solve them **IN 2 HOURS**!

### Examples of RTOS

| Example | Why RTOS? |
|---------|-----------|
| 🏧 ATM Machines | Millions transacting simultaneously, yet instant response |
| 🚂 Railway Reservation | Lakhs booking at same time, immediate confirmation |
| 🚦 Traffic Lights | Must switch exactly on time |
| 🚗 Car Airbags | Must deploy instantly on collision |

### ATM Full Form

> **ATM = Automated Teller Machine**

---

## 7. Soft RTOS vs Hard RTOS

### Soft Real-Time OS

**Characteristics:**
- Time limit is fixed
- If task fails: **RE-ATTEMPT is possible**
- No major disaster
- System continues working

**Examples:**
- ATM transactions (retry possible)
- Railway reservations
- Online examinations

**Analogy:** You fail an exam? You can appear next year!

### Hard Real-Time OS

**Characteristics:**
- Time limit is fixed
- If task fails: **NO re-attempt possible**
- Major disaster/damage occurs
- Critical failure

**Examples:**
- Traffic lights (wrong timing = accidents)
- Car airbags (late deployment = injury/death)
- Medical equipment
- Nuclear plant systems

**Analogy:** Traffic light turns green on both sides at same time = DISASTER!

### Comparison

| Feature | Soft RTOS | Hard RTOS |
|---------|-----------|-----------|
| Failure Recovery | ✅ Possible | ❌ Not possible |
| Consequence | Minor inconvenience | Catastrophic |
| Re-attempt | ✅ Allowed | ❌ Not allowed |
| Examples | ATM, Reservations | Traffic lights, Airbags |

---

## 8. CPU Scheduling Introduction

### What is CPU Scheduling?

> The **strategy** used by CPU to process inputs and provide outputs as quickly as possible with minimum effort.

### Important Concepts

#### 1. CPU Utilization
- Keep the CPU as **busy as possible**
- CPU is the brain - it should always be working!
- Like heart and brain in human body - works 24/7

#### 2. Throughput
- Use CPU to maximum capacity
- Get **maximum outputs** from it
- More work done = Higher throughput

---

## 9. CPU Scheduling Terms & Formulas

### Understanding with Doctor's Clinic Example

Imagine visiting a doctor:
- You arrive at **10:00 AM**
- Doctor calls you at **12:30 PM**
- Doctor treats you till **1:00 PM**
- You leave at **2:00 PM**

### Important Terms

| Term | Definition | Example |
|------|------------|---------|
| **Arrival Time (AT)** | Time when process enters system (RAM) | 10:00 AM |
| **Burst Time (BT)** | Time taken by CPU to process the task | 30 minutes |
| **Completion Time (CT)** | Time when process finishes execution | 1:00 PM |
| **Exit Time** | Time when process leaves the system | 2:00 PM |
| **Waiting Time (WT)** | Time spent waiting (not being processed) | 2.5 hours |
| **Response Time (RT)** | Time until CPU first responds | 2.5 hours |
| **Turn Around Time (TAT)** | Total time from arrival to completion | 3 hours |

### Important Formulas

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
│  Response Time (RT) = CPU First Arrival - Original AT    │
│                  RT = CPU_FA - AT                        │
└─────────────────────────────────────────────────────┘
```

### Doctor's Clinic Calculation

| Term | Calculation | Value |
|------|-------------|-------|
| Arrival Time | Given | 10:00 AM |
| Response Time | 12:30 - 10:00 | 2.5 hours |
| Burst Time | 1:00 - 12:30 | 30 minutes |
| Completion Time | Given | 1:00 PM |
| TAT | 1:00 PM - 10:00 AM | 3 hours |
| Waiting Time | 3 hours - 0.5 hours | 2.5 hours |

---

## 10. Preemptive vs Non-Preemptive

### Two Types of Scheduling Algorithms

#### Preemptive Algorithm

**How it works:**
- Task is processed **bit by bit**
- Start → Process a little → Switch to another task
- Come back → Process more → Switch again
- Continue until complete

**Key Feature:** **Prevents CPU Monopolization**

#### Non-Preemptive Algorithm

**How it works:**
- Task runs **start to finish**
- Start → Process completely → Exit
- Won't leave CPU until done
- Other tasks must wait

**Key Feature:** **CPU Monopolization occurs**

### Comparison

| Feature | Preemptive | Non-Preemptive |
|---------|------------|----------------|
| Processing Style | Bit by bit | Complete at once |
| CPU Monopolization | ❌ Prevented | ✅ Occurs |
| Switching | Frequent | No switching |
| WT vs RT | Usually different | **WT = RT** |

### Important Exam Question

> Q: Which algorithm prevents CPU monopolization?
> 
> A: **Preemptive Algorithm**

### Key Point for Non-Preemptive

> In Non-Preemptive algorithms: **Waiting Time = Response Time**

---

## 11. FCFS Algorithm with Example

### First Come First Serve (FCFS)

| Property | Value |
|----------|-------|
| **Type** | Non-Preemptive |
| **Rule** | Whoever arrives first gets served first |

### Important Concepts

#### Ready Queue (RAM)
- Where processes wait before going to CPU
- Shows the order of processes waiting

#### Gantt Chart (CPU)
- Shows how CPU processes each task
- Visual representation of execution order
- Left side = Start time
- Right side = Completion time

### Key Points

1. Input goes to **RAM first**, then to **CPU**
2. First process to arrive has **Waiting Time = 0**
3. Completion Time is read from **right side** of Gantt Chart
4. CPU First Arrival is read from **left side** of Gantt Chart

### Example Problem

**Given Data:**

| Process | Arrival Time (AT) | Burst Time (BT) |
|---------|-------------------|-----------------|
| P1 | 2 | 6 |
| P2 | 5 | 3 |
| P3 | 1 | 8 |
| P4 | 0 | 3 |
| P5 | 4 | 4 |

### Step 1: Determine Order (by Arrival Time)

Order: P4 (AT=0) → P3 (AT=1) → P1 (AT=2) → P5 (AT=4) → P2 (AT=5)

### Step 2: Create Gantt Chart

```
|----P4----|--------P3--------|------P1------|----P5----|--P2--|
0          3                  11             17         21     24
```

### Step 3: Calculate All Values

| Process | AT | BT | CT | TAT (CT-AT) | WT (TAT-BT) | RT |
|---------|----|----|----|----|----|----|
| P4 | 0 | 3 | 3 | 3 | 0 | 0 |
| P3 | 1 | 8 | 11 | 10 | 2 | 2 |
| P1 | 2 | 6 | 17 | 15 | 9 | 9 |
| P5 | 4 | 4 | 21 | 17 | 13 | 13 |
| P2 | 5 | 3 | 24 | 19 | 16 | 16 |

### Observations

1. **P4 has WT = 0** because it's the first to arrive (no waiting!)
2. **WT = RT for all processes** because FCFS is Non-Preemptive
3. Each process's waiting time = Sum of burst times of all processes before it

### Waiting Time Logic

> If you're at a ticket counter:
> - If you're FIRST → Waiting Time = 0
> - If 1 person ahead → WT = Their processing time
> - If 10 people ahead → WT = Sum of all their processing times

---

## 12. Summary & Key Points

### OS Types Summary

| OS Type | Key Feature |
|---------|-------------|
| Multi-Tasking | Upgraded Multi-Programming, Time Sharing |
| Multi-Processing | Multiple CPUs (Hardware upgrade) |
| Soft RTOS | Re-attempt possible on failure |
| Hard RTOS | No second chance, critical systems |

### CPU Count Summary

| OS Type | Number of CPUs |
|---------|----------------|
| Batch Processing | Single |
| Multi-Programming | Single |
| Multi-Tasking | Single |
| Multi-Processing | **Multiple** |

### Formula Summary

| Formula | Expression |
|---------|------------|
| Turn Around Time | TAT = CT - AT |
| Waiting Time | WT = TAT - BT |
| Response Time | RT = CPU First Arrival - AT |

### Algorithm Types

| Type | Characteristic | WT vs RT |
|------|----------------|----------|
| Preemptive | Prevents monopolization | Usually different |
| Non-Preemptive | CPU monopolization | **WT = RT** |

### FCFS Key Points

1. Type: **Non-Preemptive**
2. Rule: First come, first served
3. First process: **WT = 0**
4. All processes: **WT = RT**

### Important Full Forms

| Abbreviation | Full Form |
|--------------|-----------|
| RTOS | Real-Time Operating System |
| ATM | Automated Teller Machine |
| FCFS | First Come First Serve |
| AT | Arrival Time |
| BT | Burst Time |
| CT | Completion Time |
| TAT | Turn Around Time |
| WT | Waiting Time |
| RT | Response Time |

---

## Quick Revision Points

1. ✅ Multi-Tasking = Upgraded Multi-Programming = Time Sharing
2. ✅ Multi-Processing = Multiple CPUs (Hardware upgrade)
3. ✅ Soft RTOS = Can retry on failure
4. ✅ Hard RTOS = No retry, critical failure
5. ✅ TAT = CT - AT
6. ✅ WT = TAT - BT
7. ✅ Preemptive prevents CPU monopolization
8. ✅ Non-Preemptive: WT = RT
9. ✅ FCFS is Non-Preemptive
10. ✅ First process in FCFS has WT = 0

---

## Next Lesson Preview

**Topics to be covered:**
- More CPU Scheduling Algorithms
- Shortest Job First (SJF)
- Priority Scheduling
- Round Robin

---

*Notes prepared from Operating System Lesson 3*
*Computer Foundation Course - Khan Global Studies*
