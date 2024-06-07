This repository contains notes and resources for learning CUDA.

### Course Overview
Resources : [CUDA Tutorial Series](https://www.youtube.com/playlist?list=PLBQlPZZ80yqRVrt99CsmYY77MLaenKVa8)

### Contents

#### Introduction to GPUs
- **Difference between CPUs and GPUs**
- **GPU Architecture and Components**
- **Step-by-step SM (Streaming Multiprocessor) Functionality**

#### CPU vs GPU
- **Introduction to GPU Architecture**
  - **Can we write code and run it on GPU?**
    - Answer: Yes, but it requires CUDA for NVIDIA GPUs or OpenCL for others.

  - **Comparison of CPUs and GPUs**:
    | Feature               | CPU                        | GPU                                    |
    |-----------------------|----------------------------|----------------------------------------|
    | Purpose               | General-purpose computing  | Graphics rendering, parallel tasks     |
    | Cores (ALU)           | Fewer (up to 32 cores)     | Many (hundreds to thousands)           |
    | Architecture          | Sequential processing      | Parallel processing                    |
    | Clock Speed           | Higher (GHz range)         | Lower, but more cores                  |
    | Cache                 | Larger caches              | Smaller caches per core                |
    | Memory                | System RAM and caches      | Dedicated VRAM                         |
    | Floating Point        | Supports single and double | Optimized for single precision         |
    | Power Consumption     | Higher                     | Efficient for parallel tasks           |
    | Special Features      | General computing optimizations | Graphics rendering specializations |




- **CPU ALU vs GPU Core**
  - **CPU ALU**: More powerful, higher frequencies (3-4 GHz).
  - **GPU Core**: Optimized for parallel processing, lower frequencies (765-1200 MHz).

- **Performance Impact**
  - **Sequential Execution**: Instructions processed step-by-step.
  - **Parallel Execution**: Independent instructions executed simultaneously.

- **CPU and GPU Coexistence**
  - **Motherboard**: Central hub connecting CPU, GPU, and other components.

#### Motherboard Components
- **CPU Socket**
- **Chipset**
- **RAM Slots**
- **PCI Slots**
- **SATA Connectors**
- **USB Headers**
- **CMOS Battery**
- **BIOS Chip**
- **Power Connectors**
- **Front Panel Connectors**
- **Cooling System Connectors**
- **M.2 Slots**
- **Ethernet Port**
- **Audio Ports**
- **VRM (Voltage Regulator Module)**
- **Debug LEDs/Display**
- **Thunderbolt Header**
- **Wi-Fi/Bluetooth Module**
- **Internal Headers**

#### NVIDIA GPU Components
- **SM (Streaming Multiprocessor)**: Manages parallel tasks, contains multiple CUDA cores.
- **L2 Cache Memory**: Stores recently accessed data for faster retrieval.
- **Device Global Memory**: Main memory for data storage, accessible by all cores and SMs.
- **Scheduler**: Decides which tasks (kernels) to execute next.
- **Dispatcher**: Sends tasks to SMs for execution.

#### SM (Streaming Multiprocessor) Functionality
- **Instruction Fetch**
- **Thread Assignment**
- **Thread Scheduling**
- **Instruction Decode and Issue**
- **Parallel Execution**
- **Data Access**
- **Execution Completion**
- **Warp Synchronization (if needed)**
- **Result Accumulation**
- **Completion and Result Return**

#### Example Kernel Execution
- **Calculating the square of a number**
  - Organize threads into warps.
  - Assign tasks to CUDA cores.
  - Execute instructions in parallel.
  - Store results in shared memory.
  - Return results to GPU memory.

#### NVIDIA GPU Architectures and Generations
- **GPU Architecture**: Design and organization of GPU components and functionality.

### Further Learning
Stay tuned for more updates and detailed explanations as we progress through the course. Happy learning!
