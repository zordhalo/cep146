
# Lab 1
# Computer Systems In-Class Lab Exercises

## Exercise 1: System Hardware Detective (15-20 minutes)
**Format:** Solo or pairs  
**Objective:** Students will identify and analyze their computer's hardware components using built-in system tools.

### Completed System Specification Sheet

| Component | Specification |
|---|---|
| Computer | MacBook Air (Mac16,12) |
| Processor | Apple M4, 10 cores: 4 performance cores and 6 efficiency cores |
| Memory | 16 GB unified memory; the Apple silicon system report does not identify it as DDR4 or DDR5 because it is integrated unified memory |
| Storage | Internal Apple SSD, approximately 256 GB capacity (245.11 GB usable APFS volume) |
| Operating system | macOS 26.6.2 (build 25G83), Darwin 25.6.0 |

### Analysis Answers

1. **How many tasks can the processor theoretically handle simultaneously?**
   The processor has 10 CPU cores, so it can theoretically execute up to 10 hardware threads simultaneously when tasks can be distributed across all cores. Four are performance cores for demanding work and six are efficiency cores for lighter background work. The exact number of programs that can be open is not limited to 10 because the operating system rapidly schedules many processes across the cores.

2. **Is the storage primarily HDD or SSD, and what are the performance implications?**
   The internal storage is an SSD. Compared with an HDD, an SSD has no moving parts, much faster random access, quicker application and system startup, lower noise, and better resistance to physical shock. Its main trade-offs are that storage capacity can cost more and flash storage has a limited number of write cycles, although normal modern use manages this reliably.

3. **How does the RAM amount compare to typical requirements for modern applications?**
   The computer has 16 GB of unified memory, which is a solid amount for everyday applications, web browsing, programming, office work, and most student workloads. It meets or exceeds the common 8 GB baseline for modern applications. Very demanding video editing, 3D work, virtual machines, or large data projects may benefit from more memory. The system report showed about 15 GB in use and 90 MB unused during this check, but macOS was also compressing memory, so unused memory alone does not mean the computer has failed; memory pressure and responsiveness are better indicators.

### Optional Exercise 2: Observed Feature Checklist

- [x] **Process management:** The system reported 673 processes, including `zsh`, `Superset`, `node`, `spotlightknowled`, and `PerfPowerService`. At the instant of measurement, the sampled processes were using very little CPU; the system overall was 80.56% idle.
- [x] **Memory management:** Total memory is 16 GB. The system reported 15 GB used, approximately 90 MB unused, and significant compressed memory. This demonstrates that macOS is actively managing memory.
- [x] **File system management:** The computer uses APFS. I created `Documents/OS_Lab_Test`; its filesystem creation time was 2026-09-09 21:28:45 EDT.
- [x] **Device management:** System Report identified the Apple M4 processor, internal Apple SSD, Bluetooth controller, network adapters, and connected AirPods Pro as managed hardware devices. macOS device support includes the installed firmware and drivers needed for these devices.
- [x] **Security features:** Secure Virtual Memory and System Integrity Protection are enabled. Automatic macOS update checking is also turned on.

### Optional Challenge Answers

1. **Which process is using the most resources and why might that be?**
   The CPU snapshot did not show one process using a significant amount of CPU; the computer was 80.56% idle. The largest visible application process by memory was `2.1.263` at about 290 MB, but its CPU use was 0.0% at the time. Resource use changes continuously, so a process doing indexing, development work, or background maintenance could become the temporary leader.

2. **What would happen if the operating system did not manage memory automatically?**
   Programs would compete for the same physical memory without safe allocation or protection. They could overwrite one another's data, crash, or make the entire computer unresponsive. The operating system prevents this by allocating memory, reclaiming unused pages, compressing memory, and using virtual memory when necessary.

3. **How does the operating system protect against security threats?**
   macOS uses protections including System Integrity Protection, application permissions and sandboxing, signed software checks, encrypted and protected system data, automatic security updates, and built-in malware defenses. Secure Virtual Memory also helps protect memory contents when data is moved between RAM and storage.

### Instructions:
1. **Windows Users:** Open "System Information" (type `msinfo32` in Start menu)
   **Mac Users:** Hold Option key + Apple menu → "System Information"
   **Linux Users:** Open terminal and run `lscpu`, `lshw`, or `inxi -F`

2. **Find and record the following:**
   - Processor (CPU) brand, model, and number of cores
   - Total RAM amount and type (DDR4/DDR5)
   - Storage device type (HDD/SSD) and capacity
   - Operating System version

3. **Analysis Questions:**
   - Based on your CPU cores, how many tasks can your processor theoretically handle simultaneously?
   - Is your storage primarily HDD or SSD? What are the performance implications?
   - How does your RAM amount compare to typical requirements for modern applications?

### Deliverable:
Complete a simple system specification sheet and answer the analysis questions.

---

(Optional)

## Exercise 2: Operating System Feature Hunt (15-20 minutes)
**Format:** Solo or pairs  
**Objective:** Students will explore and identify key OS functions on their own devices.

### Mission:
Find real examples of the five key OS functions running on your computer right now.

### Tasks:

1. **Process Management:**
   - Open Task Manager (Windows), Activity Monitor (Mac), or System Monitor (Linux)
   - Identify 5 currently running processes
   - Find one process using the most CPU

2. **Memory Management:**
   - Check total RAM usage
   - Find which application is using the most memory
   - Identify available free memory

3. **File System Management:**
   - Navigate to your Documents folder
   - Create a new folder called "OS_Lab_Test"
   - Check the folder's properties/info to see creation date

4. **Device Management:**
   - Access Device Manager (Windows) or System Report (Mac)
   - Identify 3 different types of hardware devices listed
   - Find one device driver that's currently installed

5. **Security Features:**
   - Check if Windows Defender/antivirus is running
   - Verify if automatic updates are enabled
   - Look for any recent security scans

### Challenge Questions:
- Which process is using the most resources and why might that be?
- What would happen if your OS didn't manage memory automatically?
- How does your OS protect you from security threats?

### Deliverable:
Complete a checklist of found features and answer the challenge questions.

---
## Lab Rubric

**Total Points: 2 marks**

## Requirements for Completion:
* **Exercise 1 (Required):** Complete system specification sheet with all hardware components identified AND answer all three analysis questions with thoughtful responses
* **Exercise 2 (Optional):** If attempted, complete feature checklist for all 5 OS functions AND answer challenge questions

## Lab Rubric:

| Criteria | Poor - 0 mark | Fair - 1 mark | Good - 2 marks |
|---|---|---|---|
| Lab Completion | Missing system specification data OR analysis questions not attempted OR answers lack depth (single sentence, vague responses that don't address the questions) | Successfully identified most hardware components and completed system specification sheet, but analysis questions show minimal effort or understanding | Successfully completed full system specification sheet with accurate hardware identification AND provided thoughtful analysis answers that demonstrate understanding of hardware implications |
