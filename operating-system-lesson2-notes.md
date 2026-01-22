# Operating System - Lesson 2: Complete Notes

## History, Functions & Types of Operating Systems

---

## Table of Contents

1. [Quick Recap from Lesson 1](#1-quick-recap-from-lesson-1)
2. [History of Operating System](#2-history-of-operating-system)
3. [UNIX - The Revolutionary OS](#3-unix---the-revolutionary-os)
4. [Windows History](#4-windows-history)
5. [Functions of Operating System](#5-functions-of-operating-system)
6. [Types of Operating Systems](#6-types-of-operating-systems)
7. [Batch Processing Operating System](#7-batch-processing-operating-system)
8. [Multi-Programming Operating System](#8-multi-programming-operating-system)
9. [Important Full Forms](#9-important-full-forms)
10. [Summary & Key Points](#10-summary--key-points)

---

## 1. Quick Recap from Lesson 1

### Why Do We Need an Operating System?

- Initially, we created **calculators** (single-task devices)
- Then upgraded them to **computers** (multi-task devices)
- **Hardware is always created FIRST**, then software is developed

### Key Point
> Operating System is needed when a device is **capable of performing multiple tasks**.

### The Evolution Flow:
```
Hardware Created → Software Developed → OS Needed for Multi-tasking
```

---

## 2. History of Operating System

### First Machine Capable of Running OS

| Detail | Information |
|--------|-------------|
| **Name** | IBM System/360 |
| **Significance** | First machine/device that had the capability to install an Operating System |

### IBM Full Form
> **IBM = International Business Machines**

### First Operating System

| Detail | Information |
|--------|-------------|
| **Name** | MULTICS |
| **Status** | First OS ever created |
| **Success** | Not very successful, not widely used |

---

## 3. UNIX - The Revolutionary OS

### About UNIX
- A **revolutionary** operating system
- Changed computing forever
- Still the **first choice for servers** today

### Creators of UNIX

| Creator | Additional Info |
|---------|-----------------|
| **Ken Thompson** | Co-creator of UNIX |
| **Dennis Ritchie** | Co-creator of UNIX + **Father of C Language** |

> **Important:** Dennis Ritchie is known as the "Father of C Language"

### Why UNIX is Important
- Highly reliable and secure
- Foundation for many modern operating systems
- Still preferred for server environments

---

## 4. Windows History

### OS Timeline

| OS Name | Notes |
|---------|-------|
| MULTICS | First OS (Not popular) |
| UNIX | Revolutionary OS (Ken Thompson & Dennis Ritchie) |
| Linux | Started as CLI, now GUI-based |
| Macintosh (macOS) | Apple's Operating System |
| DOS | Disk Operating System (Created by IBM) |
| MS-DOS | Microsoft acquired DOS |

### Important Note
> All OS before Macintosh were **Command Line Interface (CLI)** or **Character User Interface (CUI)**

### About IBM
- **Oldest computer company** in the industry
- Created DOS originally
- Later, Bill Gates/Microsoft acquired DOS

### DOS Full Form
> **DOS = Disk Operating System**

### Windows Evolution

| Version | Notes |
|---------|-------|
| Windows 3.0 | First popular Windows version |
| Windows 2000 (ME) | ME = Millennium Edition |
| Windows XP | XP = Experience / Expert Programming |
| Windows 7 | First with integrated drivers |
| Windows 10 | Modern Windows |
| Windows 11 | Current version |

### Important Full Forms

| Abbreviation | Full Form |
|--------------|-----------|
| Windows ME | Millennium Edition (Windows 2000) |
| Windows XP | Experience / Expert Programming |

> **Exam Tip:** Windows XP full form is frequently asked in exams!

---

## 5. Functions of Operating System

### 1. Processor Management
- The processor (CPU) is the **most expensive** component in a computer
- OS ensures **maximum utilization** of the processor
- Different types of OS handle this differently

### 2. Resource Manager
When multiple programs run simultaneously, OS manages:
- When to give resources to which program
- When to take back resources
- All programs ultimately run on CPU and RAM

### 3. Memory Management
OS manages all types of memory:
- **RAM** - Primary memory
- **Cache** - Fast temporary memory
- **Hard Disk Drive** - Secondary storage

### 4. File Management
OS manages file systems using file formats:

| Format | Full Form | Status |
|--------|-----------|--------|
| **FAT** | File Allocation Table | Old, not used now |
| **NTFS** | New Technology File System | Currently used |

### 5. Security Management

| Component | Function |
|-----------|----------|
| **Firewall** | Prevents unauthorized access (Built-in with OS) |
| **Antivirus** | Prevents virus attacks (Installed separately) |

> **Analogy:** Firewall is like WBC (White Blood Cells) in our body - the bodyguard!

### 6. Device Management
- Managing external equipment connected to computer
- **Drivers:** Software that introduces external devices to the computer

**How Drivers Work:**
```
Connect Device → Computer asks for Driver → Install Driver → Device Works!
```

> **Note:** Windows 7 was the first OS with most common drivers pre-integrated.

### 7. Deadlock Prevention

| Situation | Description |
|-----------|-------------|
| Fast Response | Computer responds at maximum speed |
| Slow Response | Computer has too much work (overloaded) |
| **Deadlock** | NO response due to high number of requests |

> **Deadlock Definition:** A situation where computer gives no response due to high number of requests.

### 8. Time Management
- OS tries to provide **fastest response possible**
- As soon as possible (ASAP)

---

## 6. Types of Operating Systems

### Five Main Types:

1. **Batch Processing OS** - Processes jobs in batches
2. **Multi-Programming OS** - Multiple programs, one CPU
3. **Multi-Tasking OS** - (Covered in next lesson)
4. **Time Sharing OS** - (Covered in next lesson)
5. **Real-Time OS** - (Covered in next lesson)

---

## 7. Batch Processing Operating System

### What is a "Batch"?

**Batch = Group**

For a group to exist, two conditions must be met:
1. **More than one item** (multiple items)
2. **Same type** (all items must be similar)

### Historical Context (1980s)

In 1980, computers were:
- NOT in common people's homes
- Only in research institutes, universities
- Far from common man's reach
- Very expensive and rare

### How Did People Give Input?

People used:
- **Punch Cards**
- **Magnetic Tapes**

They would store their instructions in these and give them to an expert at the computer center.

### How Batch Processing Works

```
Input 1 ─┐
Input 2 ─┼─→ Wait for Batch Formation → CPU Processes Entire Batch
Input 3 ─┘
```

### Key Characteristics

| Feature | Description |
|---------|-------------|
| Input Type | Multiple inputs, **same type only** |
| Processing | Waits until batch is formed |
| CPU | Single CPU |

### Problems with Batch Processing

| Problem | Description |
|---------|-------------|
| ❌ Single input must WAIT | Until batch is formed |
| ❌ CPU remains IDLE | While waiting for batch |
| ❌ Costly processor not utilized | Properly |
| ❌ Only same type jobs | Different types not allowed |

### Real-Life Example: NEFT

> **NEFT = National Electronic Fund Transfer**

**Money Transfer Methods:**

| Method | Type | Speed |
|--------|------|-------|
| NEFT | Batch Processing | 30-60 minutes |
| IMPS | Immediate | 10-15 seconds |
| RTGS | Immediate | 10-15 seconds (Min ₹2 Lakh) |

**Why NEFT is slow?**
- Uses batch processing
- Approximately 48 transactions per batch
- Waits until batch is complete

> **Exam Question:** Bank account opening is an example of Batch Processing - forms are collected and processed together!

---

## 8. Multi-Programming Operating System

### What is Multi-Programming?

> Allows processing of **one OR more than one** program.
> Programs can be **same type OR different type**.

### Improvements over Batch Processing

| Batch Processing Problem | Multi-Programming Solution |
|-------------------------|---------------------------|
| Single program must wait | ✅ Single program processed immediately |
| CPU idle during batch formation | ✅ CPU starts working immediately |
| Only same type programs | ✅ Any type of programs allowed |

### Key Feature
> Uses **Single CPU/Processor**

### How It Works

```
Program P1 → CPU → Process Immediately!
```

### Two Types of Programs

| Type | Description | Example |
|------|-------------|---------|
| **Type 1** | Start → End → Exit | Playing a movie |
| **Type 2** | Start → Pause → Continue → End | Filling a form |

### The Remaining Problem

**Scenario:**
1. P1 (complete program) → CPU → Processes → Exit ✅
2. P2 (needs I/O) → CPU → Partial process → Back to RAM (waiting)
3. **CPU becomes IDLE while P2 waits!**
4. P3, P4 have very long waiting time

### RAM = Waiting Room

> Programs wait in RAM before going to CPU and return to RAM during I/O operations.

### Teacher's Analogy

Imagine a teacher solving doubts:
- **Student P1:** Has 5 doubts → Teacher solves all 5 → Done ✅
- **Student P2:** Has 8 doubts → Teacher solves 3 → P2 says "I want to try myself"
- **Teacher waits** for P2 instead of going to P3
- **P3, P4 have to wait** for a long time!

### Problem Summary

| Issue | Description |
|-------|-------------|
| CPU Idle | During I/O operations |
| Long Waiting | For other programs |
| Not Efficient | Resource utilization |

> **Next Lesson:** Multi-Tasking OS will solve these problems!

---

## 9. Important Full Forms

| Abbreviation | Full Form |
|--------------|-----------|
| IBM | International Business Machines |
| DOS | Disk Operating System |
| MS-DOS | Microsoft Disk Operating System |
| FAT | File Allocation Table |
| NTFS | New Technology File System |
| CLI | Command Line Interface |
| CUI | Character User Interface |
| GUI | Graphical User Interface |
| ME | Millennium Edition |
| XP | Experience / Expert Programming |
| NEFT | National Electronic Fund Transfer |
| IMPS | Immediate Payment Service |
| RTGS | Real Time Gross Settlement |
| CPU | Central Processing Unit |
| RAM | Random Access Memory |
| I/O | Input/Output |

---

## 10. Summary & Key Points

### Must Remember - History

| Topic | Answer |
|-------|--------|
| First Machine for OS | IBM System/360 |
| First OS | MULTICS |
| Revolutionary OS | UNIX |
| UNIX Creators | Ken Thompson & Dennis Ritchie |
| Father of C Language | Dennis Ritchie |
| Oldest Computer Company | IBM |
| First Popular Windows | Windows 3.0 |
| First Windows with Integrated Drivers | Windows 7 |

### Must Remember - Functions

1. **Processor Management** - Maximum CPU utilization
2. **Resource Management** - Allocate resources to programs
3. **Memory Management** - RAM, Cache, HDD
4. **File Management** - FAT, NTFS
5. **Security** - Firewall, Antivirus
6. **Device Management** - Drivers
7. **Deadlock Prevention** - Handle no-response situations
8. **Time Management** - Fast response

### OS Types Comparison

| Feature | Batch Processing | Multi-Programming |
|---------|-----------------|-------------------|
| Input Type | Multiple, Same type only | One or more, Any type |
| Processing | Waits for batch | Immediate |
| CPU | Single | Single |
| Problem | CPU idle during batch formation | CPU idle during I/O operations |

### Key Definitions

| Term | Definition |
|------|------------|
| **Batch** | Group of similar items (more than one, same type) |
| **Deadlock** | No response from computer due to high requests |
| **Driver** | Software that introduces devices to computer |
| **Firewall** | Prevents unauthorized access |
| **RAM** | Waiting room for programs |

---

## Quick Revision Points

1. ✅ Hardware is created FIRST, then software
2. ✅ IBM System/360 - First machine capable of running OS
3. ✅ MULTICS - First OS (not successful)
4. ✅ UNIX - Revolutionary OS, still used in servers
5. ✅ Dennis Ritchie = UNIX creator + Father of C Language
6. ✅ IBM = Oldest computer company
7. ✅ DOS created by IBM, acquired by Microsoft
8. ✅ Windows 7 = First with integrated drivers
9. ✅ FAT (old) vs NTFS (current) file systems
10. ✅ Firewall = Built-in security (like WBC in body)
11. ✅ Batch Processing = Wait for batch, same type only
12. ✅ Multi-Programming = Immediate processing, any type
13. ✅ Both use Single CPU
14. ✅ NEFT = Example of Batch Processing
15. ✅ RAM = Waiting Room for programs

---

## Next Lesson Preview

**Topic:** Multi-Tasking Operating System
- Will solve the problems of Multi-Programming
- Better CPU utilization
- No idle time during I/O operations

---

*Notes prepared from Operating System Lesson 2*
*Computer Foundation Course - Khan Global Studies*
