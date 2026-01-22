# Operating System - Complete JOA IT Exam Notes

## 🎯 One-Stop Revision Guide for Government Exams

---

# 📑 TABLE OF CONTENTS

1. [Operating System Basics](#1-operating-system-basics)
2. [History of Operating System](#2-history-of-operating-system)
3. [Functions of Operating System](#3-functions-of-operating-system)
4. [Types of Operating System](#4-types-of-operating-system)
5. [CPU Scheduling Concepts](#5-cpu-scheduling-concepts)
6. [Scheduling Algorithms](#6-scheduling-algorithms)
7. [Spooling](#7-spooling)
8. [Important Full Forms](#8-important-full-forms)
9. [Important MCQs - Previous Year Pattern](#9-important-mcqs---previous-year-pattern)
10. [Quick Revision Tables](#10-quick-revision-tables)

---

# 1. Operating System Basics

## Definition

> **Operating System** is a set of programs that controls the execution of application programs and acts as an intermediary between user and computer hardware.

## Key Points

| Point | Description |
|-------|-------------|
| Type | System Software |
| Function | Manages hardware + Provides environment for applications |
| Position | Between User and Hardware |
| Mandatory | Yes - Computer won't work without OS |

## OS Components

```
┌─────────────────────────────────────────┐
│              USER                        │
├─────────────────────────────────────────┤
│        APPLICATION SOFTWARE              │
├─────────────────────────────────────────┤
│    OPERATING SYSTEM (Shell + Kernel)     │
├─────────────────────────────────────────┤
│            HARDWARE                      │
└─────────────────────────────────────────┘
```

## Shell and Kernel

| Component | Description | Also Called |
|-----------|-------------|-------------|
| **Kernel** | Heart/Core of OS, manages hardware | Heart of OS |
| **Shell** | Converts user commands to machine language | Command Interpreter |

### Important Points:
- **Kernel** loads first during booting, exits last during shutdown
- **Shell** contains language translators (Compiler, Interpreter, Assembler)
- Kernel understands only **Machine Language**

## Booting

> **Booting** = Process of starting a computer (Loading OS from Hard Disk to RAM)

### Types of Booting

| Type | Description | Method |
|------|-------------|--------|
| **Cold Boot** | Starting computer from OFF state | Power button |
| **Warm Boot** | Restarting computer | Ctrl+Alt+Delete |

### Boot Process Components

| Component | Location | Function |
|-----------|----------|----------|
| **BIOS** | ROM | Basic Input Output System |
| **Boot Loader** | Inside BIOS | Initiates booting process |
| **POST** | BIOS | Power On Self Test - checks components |

---

# 2. History of Operating System

## Timeline (Must Remember!)

| OS Name | Key Information |
|---------|-----------------|
| **IBM System/360** | First machine capable of running OS |
| **MULTICS** | First Operating System (not successful) |
| **UNIX** | Revolutionary OS, still used in servers |
| **Linux** | Started as CLI, now GUI |
| **Macintosh** | Apple's OS |
| **DOS** | Disk Operating System (by IBM) |
| **MS-DOS** | Microsoft acquired DOS |

## UNIX Creators (Very Important!)

| Creator | Additional Info |
|---------|-----------------|
| **Ken Thompson** | Co-creator of UNIX |
| **Dennis Ritchie** | Co-creator of UNIX + **Father of C Language** |

## Windows Evolution

| Version | Special Name/Feature |
|---------|---------------------|
| Windows 3.0 | First popular Windows |
| Windows 2000 | **ME** (Millennium Edition) |
| Windows XP | **Experience / Expert Programming** |
| Windows 7 | First with integrated drivers |
| Windows 10/11 | Current versions |

## Important Facts

- **IBM** = Oldest computer company
- **UNIX** = First choice for servers
- All OS before Macintosh were **CLI/CUI** (Command Line Interface)

---

# 3. Functions of Operating System

## 8 Main Functions

| # | Function | Description |
|---|----------|-------------|
| 1 | **Processor Management** | Maximum CPU utilization |
| 2 | **Resource Management** | Allocate resources to programs |
| 3 | **Memory Management** | Manage RAM, Cache, HDD |
| 4 | **File Management** | Manage file systems (FAT, NTFS) |
| 5 | **Security Management** | Firewall, protect from unauthorized access |
| 6 | **Device Management** | Manage external devices via drivers |
| 7 | **Deadlock Prevention** | Handle no-response situations |
| 8 | **Time Management** | Provide fastest response |

## File Systems

| Format | Full Form | Status |
|--------|-----------|--------|
| **FAT** | File Allocation Table | Old, not used |
| **NTFS** | New Technology File System | Currently used |

## Security Components

| Component | Function |
|-----------|----------|
| **Firewall** | Prevents unauthorized access (built-in) |
| **Antivirus** | Prevents virus attacks (installed separately) |

> **Analogy:** Firewall is like WBC (White Blood Cells) - body's guard!

## Drivers

> **Driver** = Software that introduces external devices to computer

- Windows 7 was first OS with most drivers pre-integrated
- External devices need driver installation

## Deadlock

> **Deadlock** = No response from computer due to high number of requests

---

# 4. Types of Operating System

## 5 Main Types

| Type | Key Feature | CPU Count |
|------|-------------|-----------|
| **Batch Processing** | Jobs processed in batches | Single |
| **Multi-Programming** | Multiple programs, one at a time | Single |
| **Multi-Tasking** | Time sharing, fast switching | Single |
| **Multi-Processing** | Multiple CPUs | **Multiple** |
| **Real-Time OS** | Immediate response | Varies |

## Batch Processing OS

### Characteristics:
- Jobs must be **same type**
- Jobs must be **more than one**
- Single program must **WAIT** for batch
- CPU remains **IDLE** while waiting

### Example: **NEFT** (National Electronic Fund Transfer)
- Transactions collected in batches (~48 transactions)
- Takes 30-60 minutes (not instant)
- Bank account opening is also batch processing

## Multi-Programming OS

### Characteristics:
- Processes **one OR more** programs
- Programs can be **same OR different** type
- **Single CPU**
- No waiting for batch formation

### Problem:
- CPU idle during I/O operations
- Other programs wait too long

## Multi-Tasking OS

> **Multi-Tasking = Upgraded version of Multi-Programming**

### Characteristics:
- Also called **Time Sharing**
- CPU switches between programs **very fast**
- Appears **simultaneous**, actually **alternative**
- Prevents CPU monopolization

### Key Point:
- If both Multi-Programming and Multi-Tasking in options → Choose **Multi-Tasking**

## Multi-Processing OS

> Uses **MORE THAN ONE CPU** in single computer

### Characteristics:
- **Hardware level** advancement
- Multiple processors share resources
- If one CPU fails, others continue
- More reliable

### Exam Tip:
- Multi-Processing = Multiple Processors (Hardware)
- Multi-Programming/Tasking = Single Processor (Software)

## Real-Time OS (RTOS)

> Tasks given **FIXED TIME LIMIT** to complete

### Types of RTOS:

| Type | Failure Recovery | Examples |
|------|------------------|----------|
| **Soft RTOS** | Re-attempt possible | ATM, Railway booking, Online exams |
| **Hard RTOS** | NO re-attempt, critical failure | Traffic lights, Car airbags, Medical equipment |

### Examples:
- **ATM** (Automated Teller Machine) - Soft RTOS
- **Traffic Lights** - Hard RTOS
- **Railway Reservation** - Soft RTOS

---

# 5. CPU Scheduling Concepts

## Important Terms

| Term | Full Form | Definition |
|------|-----------|------------|
| **AT** | Arrival Time | When process enters system (RAM) |
| **BT** | Burst Time | Time CPU takes to process |
| **CT** | Completion Time | When process finishes |
| **TAT** | Turn Around Time | Total time from arrival to completion |
| **WT** | Waiting Time | Time spent waiting |
| **RT** | Response Time | Time until CPU first responds |

## Formulas (Must Memorize!)

```
┌─────────────────────────────────────────────────────┐
│  TAT = CT - AT                                       │
│  (Turn Around Time = Completion Time - Arrival Time) │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│  WT = TAT - BT                                       │
│  (Waiting Time = Turn Around Time - Burst Time)      │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│  RT = CPU First Arrival - AT                         │
│  (Response Time = First CPU access - Arrival Time)   │
└─────────────────────────────────────────────────────┘
```

## Preemptive vs Non-Preemptive

| Feature | Non-Preemptive | Preemptive |
|---------|----------------|------------|
| **Execution** | Start to finish | In chunks |
| **Switching** | No mid-process | Frequent |
| **CPU Monopolization** | Possible | Prevented |
| **WT vs RT** | **WT = RT** | **WT ≠ RT** |
| **Examples** | FCFS, SJF | Round Robin |

### Key Exam Point:
> **Q:** Which scheduling prevents CPU monopolization?
> **A:** Preemptive Scheduling

---

# 6. Scheduling Algorithms

## 1. FCFS (First Come First Serve)

| Property | Value |
|----------|-------|
| Mode | Non-Preemptive |
| Rule | First arrived = First served |
| WT vs RT | WT = RT |

### Key Points:
- First process has **WT = 0**
- Simple but not efficient
- Can cause long waiting times

## 2. SJF (Shortest Job First)

| Property | Value |
|----------|-------|
| Mode | Non-Preemptive |
| Rule | Shortest burst time first |
| WT vs RT | WT = RT |

### Special Rule:
> When Burst Times are equal → Use **Arrival Time** to decide (who came first)

### Key Points:
- Smaller BT = Higher priority
- First process runs immediately (no comparison)
- More efficient than FCFS

## 3. Round Robin

| Property | Value |
|----------|-------|
| Mode | **Preemptive** |
| Rule | Fixed time quantum for each |
| WT vs RT | **WT ≠ RT** |

### Key Concepts:
- **Time Quantum** = Fixed time slice (10-100 ms)
- After quantum expires → Process goes to end of queue
- Prevents monopolization
- Fair distribution

### Process Flow:
```
Process → CPU (for quantum time) → Back to Queue → Wait → CPU again → ...
```

## Algorithm Comparison Table

| Algorithm | Mode | Priority | WT = RT? |
|-----------|------|----------|----------|
| FCFS | Non-Preemptive | Arrival Time | Yes |
| SJF | Non-Preemptive | Burst Time | Yes |
| Round Robin | Preemptive | Time Quantum | No |

---

# 7. Spooling

## Definition

> **SPOOL** = Simultaneous Peripheral Operations Online

Used when: **User's requirement > Machine's execution power**

## Best Example: Printer

### Scenario:
- Multiple computers connected to one printer
- Each sends print jobs
- Jobs form a **queue** (FCFS)
- Queue area = **SPOOL**

### Key Points:

| Point | Description |
|-------|-------------|
| Scheduling | FCFS (First Come First Serve) |
| Cancel Job | Go to Spooler |
| Printer | Shareable device in network |
| Queue Location | Memory area called SPOOL |

## Exam Important:
> **Q:** Which device is shareable in network?
> **A:** Printer

---

# 8. Important Full Forms

## Must Remember for Exam!

| Abbreviation | Full Form |
|--------------|-----------|
| **OS** | Operating System |
| **BIOS** | Basic Input Output System |
| **POST** | Power On Self Test |
| **DOS** | Disk Operating System |
| **GUI** | Graphical User Interface |
| **CLI** | Command Line Interface |
| **CUI** | Character User Interface |
| **IBM** | International Business Machines |
| **FAT** | File Allocation Table |
| **NTFS** | New Technology File System |
| **SPOOL** | Simultaneous Peripheral Operations Online |
| **ATM** | Automated Teller Machine |
| **NEFT** | National Electronic Fund Transfer |
| **IMPS** | Immediate Payment Service |
| **RTGS** | Real Time Gross Settlement |
| **RTOS** | Real Time Operating System |

## Windows Versions

| Version | Full Form |
|---------|-----------|
| **ME** | Millennium Edition |
| **XP** | Experience / Expert Programming |

## Scheduling Terms

| Abbreviation | Full Form |
|--------------|-----------|
| **FCFS** | First Come First Serve |
| **SJF** | Shortest Job First |
| **AT** | Arrival Time |
| **BT** | Burst Time |
| **CT** | Completion Time |
| **TAT** | Turn Around Time |
| **WT** | Waiting Time |
| **RT** | Response Time |

---

# 9. Important MCQs - Previous Year Pattern

## Operating System Basics

**Q1:** A _____ consists of set of programs that control and coordinate activities of computer.
**A:** Operating System

**Q2:** _____ program acts as interface between user and hardware.
**A:** Operating System

**Q3:** Heart/Core of Operating System is called?
**A:** Kernel

**Q4:** Shell is also known as?
**A:** Command Interpreter

**Q5:** BIOS full form?
**A:** Basic Input Output System

**Q6:** BIOS is also called?
**A:** Firmware

## History

**Q7:** First Operating System was?
**A:** MULTICS

**Q8:** Father of C Language?
**A:** Dennis Ritchie

**Q9:** UNIX creators?
**A:** Ken Thompson and Dennis Ritchie

**Q10:** First machine capable of running OS?
**A:** IBM System/360

**Q11:** Windows XP full form?
**A:** Experience / Expert Programming

**Q12:** Oldest computer company?
**A:** IBM (International Business Machines)

## Types of OS

**Q13:** OS that allows only one user at a time?
**A:** Single User OS (DOS)

**Q14:** Multiple programs running with single CPU?
**A:** Multi-Programming

**Q15:** Multiple programs with multiple CPUs?
**A:** Multi-Processing

**Q16:** Upgraded version of Multi-Programming?
**A:** Multi-Tasking

**Q17:** Time Sharing is also called?
**A:** Multi-Tasking

**Q18:** Jobs executed as a group?
**A:** Batch Processing

**Q19:** Example of Batch Processing?
**A:** NEFT, Bank Account Opening

## Scheduling

**Q20:** Which scheduling prevents CPU monopolization?
**A:** Preemptive Scheduling

**Q21:** In Non-Preemptive scheduling, WT and RT are?
**A:** Equal (WT = RT)

**Q22:** Round Robin uses which mode?
**A:** Preemptive

**Q23:** Fixed time slice in Round Robin is called?
**A:** Time Quantum

## Booting

**Q24:** Starting computer from OFF state?
**A:** Cold Boot

**Q25:** Restarting computer?
**A:** Warm Boot

**Q26:** Shortcut for Warm Boot?
**A:** Ctrl + Alt + Delete

**Q27:** Who created Ctrl+Alt+Delete?
**A:** David Bradley

**Q28:** Direct shortcut for Task Manager?
**A:** Ctrl + Shift + Escape

## File System & Security

**Q29:** Current file system used in Windows?
**A:** NTFS (New Technology File System)

**Q30:** Old file system (not used now)?
**A:** FAT (File Allocation Table)

**Q31:** Prevents unauthorized access?
**A:** Firewall

**Q32:** Prevents virus attacks?
**A:** Antivirus

## Spooling

**Q33:** SPOOL full form?
**A:** Simultaneous Peripheral Operations Online

**Q34:** Shareable device in network?
**A:** Printer

**Q35:** To cancel print job, go to?
**A:** Spooler

## RTOS

**Q36:** ATM uses which type of OS?
**A:** Real Time OS (Soft RTOS)

**Q37:** Traffic lights use which type of OS?
**A:** Hard RTOS

**Q38:** UNIX is typically used for?
**A:** Servers

## Memory & Others

**Q39:** RAM is also called?
**A:** Waiting Room (for processes)

**Q40:** No response from computer due to high requests?
**A:** Deadlock

**Q41:** Software that introduces devices to computer?
**A:** Driver

**Q42:** First Windows with integrated drivers?
**A:** Windows 7

**Q43:** Log Off means?
**A:** Switch from one account to another

**Q44:** Sleep mode keeps programs in?
**A:** RAM

**Q45:** Breaking task into blocks?
**A:** Paging

---

# 10. Quick Revision Tables

## OS Types at a Glance

| Type | CPU | Key Feature | Example |
|------|-----|-------------|---------|
| Batch | Single | Same type jobs in batch | NEFT |
| Multi-Programming | Single | Multiple programs | - |
| Multi-Tasking | Single | Time sharing, fast switching | Windows |
| Multi-Processing | Multiple | Hardware upgrade | Servers |
| RTOS | Varies | Immediate response | ATM |

## Scheduling at a Glance

| Algorithm | Mode | WT=RT? | Key Rule |
|-----------|------|--------|----------|
| FCFS | Non-Preemptive | Yes | First come first |
| SJF | Non-Preemptive | Yes | Shortest BT first |
| Round Robin | Preemptive | No | Time quantum |

## Formulas at a Glance

| Formula | Expression |
|---------|------------|
| Turn Around Time | CT - AT |
| Waiting Time | TAT - BT |
| Response Time | CPU First Arrival - AT |

## Key Persons

| Person | Known For |
|--------|-----------|
| Dennis Ritchie | UNIX + C Language |
| Ken Thompson | UNIX |
| David Bradley | Ctrl+Alt+Delete |

## Important Shortcuts

| Shortcut | Function |
|----------|----------|
| Ctrl+Alt+Delete | Restart / Task Manager |
| Ctrl+Shift+Escape | Direct Task Manager |

---

# 🎯 EXAM DAY QUICK POINTS

1. ✅ **Kernel** = Heart of OS
2. ✅ **Shell** = Command Interpreter
3. ✅ **Dennis Ritchie** = Father of C + UNIX creator
4. ✅ **MULTICS** = First OS
5. ✅ **IBM System/360** = First machine for OS
6. ✅ **NTFS** = Current file system
7. ✅ **FAT** = Old file system
8. ✅ **Firewall** = Prevents unauthorized access
9. ✅ **Cold Boot** = Start from OFF
10. ✅ **Warm Boot** = Restart (Ctrl+Alt+Del)
11. ✅ **Multi-Processing** = Multiple CPUs
12. ✅ **Multi-Tasking** = Time Sharing
13. ✅ **Preemptive** = Prevents monopolization
14. ✅ **Non-Preemptive** = WT = RT
15. ✅ **SPOOL** = Simultaneous Peripheral Operations Online
16. ✅ **Printer** = Shareable in network
17. ✅ **NEFT** = Batch Processing example
18. ✅ **ATM** = Soft RTOS example
19. ✅ **Traffic Light** = Hard RTOS example
20. ✅ **Windows XP** = Experience/Expert Programming

---

## 📝 Last Minute Tips

1. **Focus on Full Forms** - Most asked in exams
2. **Remember Formulas** - TAT, WT, RT
3. **Know the Differences** - Preemptive vs Non-Preemptive
4. **OS Types** - Know CPU count for each
5. **RTOS Types** - Soft (retry possible) vs Hard (no retry)
6. **Shortcuts** - Ctrl+Alt+Del, Ctrl+Shift+Esc
7. **Key Persons** - Dennis Ritchie, Ken Thompson, David Bradley

---

**Best of Luck for Your JOA IT Exam! 🍀**

---

*Compiled from Operating System Lessons 1-4*
*Computer Foundation Course - Khan Global Studies*
