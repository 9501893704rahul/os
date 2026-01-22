# Operating System - Lesson 1: Complete Notes

## Table of Contents
1. [What is an Operating System?](#1-what-is-an-operating-system)
2. [Why Do We Need an Operating System?](#2-why-do-we-need-an-operating-system)
3. [Calculator vs Computer](#3-calculator-vs-computer)
4. [Hardware and Software Relationship](#4-hardware-and-software-relationship)
5. [Understanding OS Through Real-Life Examples](#5-understanding-os-through-real-life-examples)
6. [Devices That Don't Need an Operating System](#6-devices-that-dont-need-an-operating-system)
7. [Objectives of Operating System](#7-objectives-of-operating-system)
8. [Four Components of a Computer System](#8-four-components-of-a-computer-system)
9. [Operating System is Like a Government](#9-operating-system-is-like-a-government)
10. [Parts of Operating System: Kernel and Shell](#10-parts-of-operating-system-kernel-and-shell)
11. [Understanding Booting Process](#11-understanding-booting-process)
12. [Shell - The Command Interpreter](#12-shell---the-command-interpreter)
13. [Examples of Operating Systems](#13-examples-of-operating-systems)

---

## 1. What is an Operating System?

### Definition
> **An Operating System (OS) is a set of programs that control the execution of application programs and act as an intermediary between the user of a computer and the computer hardware.**

### Key Points
- Operating System is technically an example of **System Software**
- Since it's system software, its basic nature is to **interact with hardware**
- Without hardware interaction, OS cannot function - this is its primary purpose
- OS provides an **interface** for application software to work
- It facilitates **interaction between user and computer hardware**

### Simple Definition
> **Operating System is a software that manages computer hardware as well as provides an environment for application programs to run.**

---

## 2. Why Do We Need an Operating System?

### The Evolution Story
- Initially, humans didn't create computers
- We first created **calculating machines** (calculators)
- By upgrading calculators, we eventually created **computers**

### The Fundamental Difference

| Aspect | Calculator | Computer/Mobile |
|--------|------------|-----------------|
| Purpose | Single task (calculation only) | Multiple tasks |
| Complexity | Simple | Complex |
| OS Required | No | Yes |
| Software Type | Embedded software | Operating System + Applications |

### The Core Need
When a device can perform **multiple tasks simultaneously**, it needs:
- Something to **manage resources**
- Something to **decide priorities**
- Something to **allocate resources**

**That "something" is the Operating System!**

---

## 3. Calculator vs Computer

### Calculator
- Used **only for calculations**
- Performs a **single task**
- No operating system required
- Uses embedded software

### Computer/Mobile
- Used for **many different types of tasks**
- Performs **multiple tasks simultaneously**
- **Operating system is mandatory**
- Can run various application software

---

## 4. Hardware and Software Relationship

### Mutual Relationship
- **Hardware without software** = Useless
- **Software without hardware** = Useless
- They have a **mutual dependency**

### Order of Creation
1. **Hardware is created first**
2. **Software is created afterwards**

### Analogy
| Computer Component | Human Body Equivalent |
|-------------------|----------------------|
| Hardware | Body (शरीर) |
| Software | Soul (आत्मा) |

> Just as a body without soul is useless, hardware without software is a **dead machine** - just a piece of hardware.

---

## 5. Understanding OS Through Real-Life Examples

### Example 1: Multitasking on Mobile
Imagine you're doing these tasks simultaneously on your mobile:
1. ✅ Calculating something
2. ✅ Chatting with friends
3. ✅ Listening to audio songs with earphones

**All three tasks run at the same time** because they have **equal priority** in the mobile's perspective.

### Example 2: Priority Management
**Scenario:** While listening to an audio song, you receive a video link and play it.

**What happens?**
- The **audio song automatically pauses**
- You didn't manually pause it
- This shows **video has higher priority than audio**

**Why?** Because video needs to be both **seen AND heard**, while audio only needs to be heard.

### Example 3: Screen Lock Behavior
**Scenario:** You're playing an audio song and you lock your phone (instant lock).

**What happens?**
- ✅ Audio song **continues playing**
- ❌ Video song **stops**

**Why does video stop?**
- Video needs to be **watched and listened**
- When you lock the screen, you can't watch
- So the OS automatically stops the video

### Example 4: Incoming Call (Highest Priority)
**Scenario:** While doing all activities, you receive a phone call.

**What happens?**
- **ALL activities go to background automatically**
- **Call takes over** - it's the **highest priority task**

### What This Teaches Us
Someone inside the computer/mobile:
- **Realizes** what's happening
- **Understands** the mechanism
- **Manages** priorities
- **Allocates** resources

**That "someone" is the Operating System!**

---

## 6. Devices That Don't Need an Operating System

### Examples of Single-Purpose Devices
- 🧺 Washing Machine
- 🍳 Microwave Oven
- ❄️ Air Conditioner (AC)
- 🏧 ATM Machines
- 🎵 iPod (media player only)

### Why No OS?
- These devices perform **only ONE specific task**
- They use **Embedded Software**
- **No updates required**
- Software is permanently embedded in the device

### What is Embedded Software?
> **Embedded Software** is software that is permanently programmed into a device for a specific, single purpose. It requires no updates or modifications.

### Key Difference
| Feature | Embedded Software | Operating System |
|---------|------------------|------------------|
| Purpose | Single task | Multiple tasks |
| Updates | Not required | Regular updates |
| Flexibility | Fixed | Flexible |
| Examples | Washing machine, Microwave | Windows, Android, iOS |

---

## 7. Objectives of Operating System

### Primary Objectives

1. **User Convenience**
   - Make the computer system convenient and easy to use for the user

2. **Efficient Hardware Usage**
   - Use computer hardware in an efficient way

3. **Program Execution**
   - Execute user programs and make solving user problems easier

---

## 8. Four Components of a Computer System

### Visual Representation
```
┌─────────────────────────────────────┐
│              USER                    │
│  (People, Machines, Robots)          │
├─────────────────────────────────────┤
│      APPLICATION SOFTWARE            │
│  (MS Office, Games, Browsers)        │
├─────────────────────────────────────┤
│       OPERATING SYSTEM               │
│  (Windows, Linux, macOS)             │
├─────────────────────────────────────┤
│           HARDWARE                   │
│  (CPU, Memory, I/O Devices)          │
└─────────────────────────────────────┘
```

### 1. Hardware
- CPU (Central Processing Unit)
- Memory (RAM, ROM)
- Input/Output Devices
- Provides basic computing resources

### 2. Operating System
- **Mandatory** for computers
- Controls and coordinates hardware usage
- Manages resources among various applications

### 3. Application Software
- **Optional** - based on user requirements
- Examples: MS Office, Adobe Reader, Media Players, Design Software
- Installed as per user needs

### 4. Users
- People (you and me)
- Machines
- Robots
- Other computers

### Important Note
| Component | Requirement |
|-----------|-------------|
| Operating System | **Mandatory** |
| Application Software | **As per requirement** (Optional) |

---

## 9. Operating System is Like a Government

### The Analogy

| Government | Operating System |
|------------|------------------|
| Doesn't manufacture products | Doesn't create data |
| Doesn't do research | Doesn't process data |
| Only **regulates** | Only **manages** |
| Ensures smooth functioning | Ensures smooth operation |
| Allocates national resources | Allocates computer resources |

### What Government Does
- Creates **rules and regulations**
- Ensures private organizations don't harm citizens
- Manages multiple organizations working in the same country
- **Regulates** but doesn't **produce**

### What OS Does Similarly
- Manages multiple applications running simultaneously
- Ensures smooth operation of all programs
- Allocates resources (CPU time, memory, etc.)
- **Regulates** but doesn't **produce**

### Real Example
During COVID-19:
- **Government's job:** Ensure vaccines reach everyone, create policies
- **Actual vaccination:** Done by doctors, nurses, labs
- Similarly, OS manages resources; actual work is done by applications

---

## 10. Parts of Operating System: Kernel and Shell

### Two Major Components

```
┌─────────────────────────────────────────┐
│                 USER                     │
├─────────────────────────────────────────┤
│         APPLICATION SOFTWARE             │
├─────────────────────────────────────────┤
│              SHELL                       │
│        (Command Interpreter)             │
├─────────────────────────────────────────┤
│              KERNEL                      │
│        (Heart/Core of OS)                │
├─────────────────────────────────────────┤
│               CPU                        │
└─────────────────────────────────────────┘
```

### 1. KERNEL

> **Kernel is called the Heart/Core of the Operating System**

#### Key Points about Kernel
- Most essential part of OS
- Directly interacts with hardware
- Manages system resources
- **Only the Kernel loads into RAM during booting** (not the entire OS)
- **Last program to leave RAM** during shutdown

#### Important Exam Question
**Q: What is called the Heart/Core of Operating System?**
**A: Kernel**

### 2. SHELL

> **Shell is called the Command Interpreter**

#### Key Points about Shell
- Outer layer of OS
- Interface between user and kernel
- Translates user commands to machine language
- Contains **Language Translators**

#### Language Translators in Shell
1. **Interpreter** - Translates line by line
2. **Compiler** - Translates entire program at once
3. **Assembler** - Converts assembly language to machine code

---

## 11. Understanding Booting Process

### What is Booting?

> **Booting is the process of loading the Operating System from Hard Disk to RAM. This is called the Startup of Computer.**

### Technical Definition
> **To load Operating System from Hard Disk to RAM is called Booting.**

### Booting Process Steps

```
1. Power Button ON
        ↓
2. Current flows to all components
        ↓
3. ROM activates first
        ↓
4. BIOS (in ROM) starts
        ↓
5. Bootstrap Loader (in BIOS) initiates
        ↓
6. OS Kernel loads from Hard Disk to RAM
        ↓
7. Computer is ready to use!
```

### Key Components

| Component | Location | Function |
|-----------|----------|----------|
| BIOS | ROM | Basic Input/Output System |
| Bootstrap Loader | Inside BIOS | Initiates OS loading |
| Kernel | Hard Disk → RAM | Core OS that gets loaded |

### Important Clarification: Does Entire OS Load to RAM?

**Example Calculation:**
- Hard Disk (C: Drive): 256 GB
- OS Installation: ~80 GB
- RAM: 16 GB

**Question:** Can 80 GB fit into 16 GB?

**Answer:** NO! That's why:
> **Only the KERNEL part of OS loads into RAM, not the entire Operating System!**

### Kernel Loading Facts
- **First to load** during startup
- **Last to leave** during shutdown
- Manages all operations while computer is running

### Drive Letters Information
| Drive Letter | Reserved For |
|--------------|--------------|
| A: | Floppy Drive (still reserved) |
| B: | Floppy Drive (still reserved) |
| C: | Hard Disk (OS installation - default) |
| D:, E:, etc. | Additional partitions |

---

## 12. Shell - The Command Interpreter

### How Shell Works

```
USER (Any Language)
        ↓
   APPLICATION
        ↓
      SHELL ←──── Converts ANY language to MACHINE language
        ↓
     KERNEL ←──── Understands only MACHINE language
        ↓
       CPU ←──── Processes the input
        ↓
     KERNEL
        ↓
      SHELL ←──── Converts MACHINE language back to USER's language
        ↓
   APPLICATION
        ↓
USER (Gets output in their language)
```

### The Language Problem

**Users speak different languages:**
- Hindi
- English
- Chinese
- Japanese
- German
- And many more...

**Computer understands only ONE language:**
- Machine Language (Binary: 0s and 1s)

### Shell's Role
1. **Receives** input from user (in any language)
2. **Converts** it to machine language
3. **Sends** to kernel
4. **Receives** output from kernel (in machine language)
5. **Converts** back to user's language
6. **Displays** to user

### Definition
> **The Shell is the layer of programming that understands and executes the commands a user enters. In some systems, Shell is called Command Interpreter.**

---

## 13. Examples of Operating Systems

### Desktop/Laptop Operating Systems
- Microsoft Windows (Windows 10, 11)
- macOS (Apple)
- Linux (Ubuntu, Fedora, etc.)
- Unix
- Chrome OS

### Mobile Operating Systems
- Android (Google)
- iOS (Apple)
- HarmonyOS (Huawei)

### Server Operating Systems
- Windows Server
- Linux Server distributions
- Unix

---

## Quick Revision Points

### Must Remember!

1. **OS Definition:** Set of programs controlling application execution, intermediary between user and hardware

2. **OS is:** System Software example

3. **Kernel:** Heart/Core of OS

4. **Shell:** Command Interpreter

5. **Booting:** Loading OS from Hard Disk to RAM

6. **Only Kernel loads to RAM** - not entire OS

7. **Kernel is last to leave RAM** during shutdown

8. **Embedded Software:** For single-purpose devices, no updates needed

9. **Four Components:** Hardware → OS → Application Software → User

10. **OS is like Government:** Manages and regulates, doesn't produce

11. **A: and B: drives:** Reserved for Floppy (even today)

12. **C: drive:** Default for OS installation

---

## Glossary

| Term | Definition |
|------|------------|
| Operating System | Software managing hardware and providing environment for applications |
| Kernel | Core/Heart of OS that loads into RAM |
| Shell | Command Interpreter, translates languages |
| Booting | Process of loading OS from Hard Disk to RAM |
| BIOS | Basic Input/Output System in ROM |
| Bootstrap Loader | Program that initiates OS loading |
| Embedded Software | Fixed software for single-purpose devices |
| System Software | Software that interacts with hardware |
| Application Software | Software for specific user tasks |

---

## Next Lesson Preview
**Topic:** History of Operating System

---

*Notes prepared from Computer Foundation Batch - Operating System Lesson 1*
*Khan Global Studies*
