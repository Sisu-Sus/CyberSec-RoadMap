# Operating Systems

## Roadmap.sh Summary:
Operating Systems (OS) are software that manage computer hardware and provide a platform for applications to run. They hand essential functions such as managing memory, processing tasks, controlling input and output devices, and facilitating file management. Key examples include Windows, macOS, Linus, and Unix. Each operating system offers different features and interfaces, tailored to specific user needs or system reuirements, from desktop computing to server management and embedded systems.

I would like to add that if you are trying a new Linux distro, I chose to go with Debian as my first choice. They have  really nice write ups for the entire system and if you are willing to put the time in, you too can evolve backwards into a CLI monkey like me. One bonus of starting with a raw Debian setup -- Debian is the base Distro for many others such as Ubuntu and Hackermans favorite, Kali Linux.

### Resource
[https://en.wikipedia.org/wiki/Operating_system](https://en.wikipedia.org/wiki/Operating_system)

### Types of Operating Systems
- Multicomputer Operating Systems: With multiprocessors multiple CPUs share memory. A multicomputer or cluster computer has multiple CPUs, each of which has its own memory. Multicomputers were developed because large mulltiprocessors are difficult to engineer and prohibitively expensive; they are universal in cloud computing because of the size of the machine needed. The different CPUs often need to send and receive messages to each other; to ensure good performance, the operating systems for these machines need to minimize this copying of packets. Newer systems are often multiqueue--seperating groups of users into seperate queues--to reduce the need for packet copying and support more concurrent users. Another techinique is remote direct memory access, which enables each CPU to access memory belonding to other CPUs. Multicomputer operating systems often support remote procedure calls where a CPU can call a procedure on another CPU, or distributed shared memory, in which the operating system uses virtualization to generate shared memory that does not physically exist.

- Distributed Systems: A distributed system is a group of distinct, networked computers--each of which might have their own operating system and filesystem. Unlike multicomputers, they may be dispersed anywhere in the world. Middlewarem an additional software layer between the operating system and applications, is often used to improve consistency. Although it functions simlarly to an operating system it is not a true operating system.

- Embedded: Embedded operating systems are designed to be used in embedded computer systems, whether they are IoT objects or not connected to a network. Embedded systems include many household appliances. The distuinguishing factor is that they do no not load user-installed software. Consqequently, they do no not need protection between different applications, enabling simpler designs. Very small operating systems might run in less than 10 kilobytes, and the smallest are for smart cards. Examples include Embedded Linux, QNX, VxWorks, and the extra-small systems RIOT and TinyOS.

- Real-time: A real-time operating system is an operating system that guarantees to process events or data by or at a specific moment in time. hard real-time systems require exact timing and are common in manufacturing, avionics, military and other similar uses. With soft real-time systems, the occasional missed event is acceptable; this category often includes audio or multimedia systems, as well as smartphones. In order for hard real-time systems by sufficiently exact in their timing, often they are just library with no protection between applications, such as eCos.

- Hypervisor: A hypervisor is an operating system that runs a virtual machine. The virtual machine is unaware that it is an application an operates as if it had its own hardware. Virtual machines can be paused, saved, and resumed, making them useful for operating systems research, development, and debugging. They also enhance portability by enabling applications to be run on a computer even if they are not compatible with the base operating system.

- Library: A library operating system (libOS) is one in which the services that a typical operating system provides, such as networking, are provided in the form of librairies and composed with a single application and configuraion code to construct a unikernel: a specialized (only the absolute necessary pieces of code are extracted from librairies and bound together), single address space, machine image that can be deployed to cloud or embedded environments.

The operating system code and application code are note xecuted in seperated protection domains (there is only a single application running, at least conceptually, so there is no need to prevent intereference between applications) and OS services are accessed via simple library calls (potentially inlining them based on compiler thresholds), without the usual overhead of context switches, in a way similarly to embedded and real-time OSes. note that this overhead is not negligible: to the direct cost of mode switching it's necessary to add the indirect pollution of important processor structures (like CPU caches, the instruction pipelines, and so on) which affects bother user-mode and kernel-mode performance.

### Next Step
- [Windows]
- [Index](https://github.com/Sisu-Sus/CyberSec-RoadMap/blob/main/index.md)
