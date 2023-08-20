# MiniMemAlloc
This project employs a memory allocation strategy where memory is allocated in multiples of 2. Additionally, it utilizes a technique to minimize memory wastage by breaking down a block into two pieces if the allocated memory size is smaller than the block size. If both pieces of the broken block are deallocated, they are merged back together to optimize memory usage.

Here's how the project incorporates these techniques:

Memory Allocation in Powers of 2:
The splitmem() function splits the available memory into blocks, each with a size that is a power of 2. This approach ensures efficient memory allocation by providing a range of block sizes, making it easier to find a suitable block for a requested memory size.

Minimizing Memory Wastage: 
When a block is allocated, the program checks if there is unused space within the block. If the allocated memory size is smaller than the block size, the block is divided into two parts: one for the allocated memory and another for the remaining unused space. This technique minimizes memory wastage by using the available space effectively.

Block Merging:
When deallocating memory, the program checks adjacent blocks. If two adjacent blocks are both deallocated and have the same size, they are merged back together into a single larger block. This merging process optimizes memory usage by reducing fragmentation and maximizing the availability of larger memory blocks for future allocations.

These techniques collectively enhance memory allocation efficiency and minimize memory fragmentation, resulting in more effective utilization of available memory resources.

This project consists of a memory allocation and deallocation system demonstrated through three different scenarios:

All_del.cpp: This component showcases memory allocation and deallocation within the program itself. Users can allocate memory with specified sizes and process IDs, and the program manages memory allocation and deallocation.

Pocess.cpp: This part demonstrates the allocation of memory when creating a new process using the fork system call. It measures the memory usage of the parent process and records the time taken for the child process to complete its execution.

file.cpp: This section involves allocating memory based on the size of a specified file. It calculates the file size, generates a random process ID, and then allocates memory accordingly.

Overall, this project provides a practical understanding of memory allocation and deallocation in different scenarios, highlighting how processes and file sizes impact memory usage.
