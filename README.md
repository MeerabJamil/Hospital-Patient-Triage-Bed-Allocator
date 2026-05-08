# Hospital Patient Triage & Bed Allocator

**Operating Systems Lab Semester Project**  
**CL2006 - Spring 2026**  
**FAST-NUCES Chiniot-Faisalabad Campus**

---

## 📋 Project Description

A comprehensive simulation of a hospital emergency room system that integrates core Operating Systems concepts including **Process Management**, **IPC**, **Thread Synchronization**, **CPU Scheduling**, and **Memory Management**.

The system handles patient triage, priority-based bed allocation (ICU, Isolation, General Ward) using **Best-Fit** algorithm, and manages concurrent patient treatment using processes and threads.

---

## ✨ Features

- Real-time patient triage via shell script
- Priority-based scheduling
- Best-Fit, First-Fit, and Worst-Fit memory allocation strategies
- Multi-threading (Receptionist, Scheduler, Nurse threads)
- Synchronization using Mutex, Condition Variables, and Semaphores
- Shared Memory for bed allocation
- Named Pipes (FIFO) for IPC
- Coalescing and Fragmentation reporting
- Clean startup and shutdown scripts

---

## 🛠️ OS Concepts Demonstrated

| OS Concept              | Implementation |
|------------------------|--------------|
| Process Management     | `fork()` + `exec()` for patient simulators |
| IPC                    | Named FIFO + Shared Memory (`shmget`) |
| Threads                | POSIX threads (Receptionist, Scheduler, 3 Nurse threads) |
| Synchronization        | Mutex, Condition Variables, Semaphores |
| Scheduling             | FCFS, SJF, Priority, Round Robin |
| Memory Management      | Best-Fit allocation + Coalescing + Fragmentation tracking |

---

🚀 Build & Run Instructions
Prerequisites

Linux Environment (Ubuntu recommended)
GCC compiler
make utility

1. Build the Project
Bashmake all

Run the Hospital System
Bash./scripts/start_hospital.sh

Add a Patient
Bash./scripts/triage.sh "Ali Khan" 45 7

Stop the System
Bash./scripts/stop_hospital.sh

Change Allocation Strategy
Bash./bin/admissions --strategy best     # best | first | worst

📁 Project Structure

src/ → All C source files
scripts/ → Shell scripts (triage.sh, start_hospital.sh, etc.)
logs/ → Generated logs (schedule_log.txt, memory_log.txt)


📊 Report & Demo

Final Report: report.pdf
Demo Video: demo_video.mp4

# First Fit
./bin/admissions --strategy first

# Worst Fit
./bin/admissions --strategy worst

**Group Members **

Member 1: Warisha Zia (F230534)
Member 2: Rabia Basri (F230588)
Member 3: Meerab Jamil (F230678)
