
Testing Change



## Memory Mapped Arrays:

- **Virtual Memory and Paging:** Modern operating systems use virtual memory. This means that programs don't directly access physical RAM; instead, they operate on a virtual address space. The OS then maps these virtual addresses to physical RAM addresses. If a program tries to access data that isn't currently in physical RAM, the OS will load that "page" of data from disk into RAM (this is called a "page fault").
    
- **Memory Mapping a File:** When you memory-map a file, you're essentially telling the operating system: "Hey, take this file on disk, and make it look like a part of my program's memory." The OS sets up this mapping, but it doesn't necessarily load the entire file into RAM immediately.
    
- **On-Demand Loading (Lazy Loading):** The beauty of memory-mapped arrays is that data is loaded **on demand**. When your program tries to access a specific part of the memory-mapped array (which corresponds to a specific part of the file), the operating system will fetch only that required portion (a "page") from the disk into RAM. If you don't access a certain part of the file, it never needs to be loaded into memory

```
np.memmap('X.dat', dtype='float32', mode='w+', shape=X_shape)
```

