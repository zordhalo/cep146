
# Lab 1: Computer Systems

## System Specification

| Component | Specification |
|---|---|
| Computer | MacBook Air (Mac16,12) |
| Processor | Apple M4, 10 cores: 4 performance cores and 6 efficiency cores |
| Memory | 16 GB unified memory; the Apple silicon system report does not identify it as DDR4 or DDR5 because it is integrated unified memory |
| Storage | Internal Apple SSD, approximately 256 GB capacity (245.11 GB usable APFS volume) |
| Operating system | macOS 26.6.2 (build 25G83), Darwin 25.6.0 |

## Analysis Answers

1. **How many tasks can the processor theoretically handle simultaneously?**
   The processor has 10 CPU cores, so theoretically it should be able to handle 10 processes running simultaniously.

2. **Is the storage primarily HDD or SSD, and what are the performance implications?**
   The internal storage is an SSD. No moving parts, way faster; can be used as a memory cache, won't get damaged by a drop and is lighter.

3. **How does the RAM amount compare to typical requirements for modern applications?**
   The computer has 16 GB of unified memory, which is more then the 8 gb suggested for a normal computer. Should be fine for regular browser use, visual studio, etc.

## Optional Feature Checklist

- [x] **Process management:** The system reported 673 processes, including `zsh`, `Superset`, `node`, `spotlightknowled`, and `PerfPowerService`. When I ran the check the the system was 80.56% idle.
- [x] **Memory management:** Total memory is 16 GB. The system reported 15 GB used, approximately 90 MB unused, and significant compressed memory. This demonstrates that macOS manages memory well.
- [x] **File system management:** The computer uses APFS. I created `Documents/OS_Lab_Test`; its filesystem creation time was 2026-09-09 21:28:45 EDT.
- [x] **Device management:** System Report said Apple M4 processor, internal Apple SSD, Bluetooth controller, network, and connected AirPods Pro as managed hardware devices.
- [x] **Security features:** Secure Virtual Memory and System Integrity Protection are enabled. Automatic macOS update checking is also turned on.
