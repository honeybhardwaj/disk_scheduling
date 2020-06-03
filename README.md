# disk_scheduling

# 1.Introduction

Since the emergence of computers, hardware technology has been evolving at a
tremendous pace. This evolution includes storage technologies. The current trend in
storage technology is miniaturization for portability and increased storage capacity.
Due to the volatile characteristic of the CPU register, Cache, and Main Memory, the
use of secondary storage devices such as Disk came into existence.

In a movable-head disk, access may take the form of a write or a read operation
performed by the access arm, which holds the read/write head. Since the invention
of movable head disk, the Input and Output (I/O) performance has been improved
by implementing proper and intelligent scheduling of disk accesses. Disk scheduling
involves a careful examination of pending requests to determine the most efficient
way to service the requests. Some of Disk Scheduling algorithms are First Come
First Serve (FCFS), Shortest Seek Time First (SSTF), SCAN, LOOK, C-SCAN and
C-LOOK Scheduling algorithm.

# 2. Feasibility
The model which has been developed is programmed to schedule multiple
Input/output requests arriving for the disk and displays the sequence produced by
multiple Disk Scheduling algorithms such as First Come First Serve (FCFS),

Shortest Seek Time First (SSTF), SCAN, LOOK, Circular SCAN (C-SCAN) and C-
LOOK Scheduling algorithm.

The model does not actually perform the read operations from the disk. It only finds
the locations sequence to be traversed by using different algorithms.

Disk scheduling is done by operating systems to schedule I/O requests arriving for
disk. Disk scheduling is also known as I/O scheduling.
Problems solved by Disk scheduling:
• Multiple I/O requests may arrive by different processes and only one I/O
request can be served at a time by disk controller. Thus, other I/O requests
need to wait in waiting queue and need to be scheduled.
• Two or more requests may be far from each other so can result in greater disk
arm movement.
• Hard drives are one of the slowest parts of computer system and thus need to
be accessed in an efficient manner.

# 2.1 Alternative solutions
# 2.1.1 FCFS
FCFS is the simplest of all the Disk Scheduling Algorithms. In FCFS, the requests
are addressed in the order they arrive in the disk queue.
Advantages:
• Every request gets a fair chance
• No indefinite postponement
Disadvantages:
• Does not try to optimize seek time
• May not provide the best possible service



# 2.1.2 SSTF
In SSTF (Shortest Seek Time First), requests having shortest seek time are executed
first. So, the seek time of every request is calculated in advance in queue and then
they are scheduled according to their calculated seek time. As a result, the request
near the disk arm will get executed first. SSTF is certainly an improvement over
FCFS as it decreases the average response time and increases the throughput of
system.

Advantages:
• Average Response Time decreases
• Throughput increases
Disadvantages:
• Overhead to calculate seek time in advance
• Can cause Starvation for a request if it has higher seek time as compared to
incoming requests
• High variance of response time as SSTF favours only some requests

# 2.1.3 SCAN
In SCAN algorithm the disk arm moves into a particular direction and services the
requests coming in its path and after reaching the end of disk, it reverses its direction
and again services the request arriving in its path. So, this algorithm works like an
elevator and hence also known as elevator algorithm. As a result, the requests at the
midrange are serviced more and those arriving behind the disk arm will have to wait.

Advantages:
• High throughput
• Low variance of response time
• Average response time
Disadvantages:
• Long waiting time for requests for locations just visited by disk arm



# 2.1.4 C-SCAN
In SCAN algorithm, the disk arm again scans the path that has been scanned, after
reversing its direction. So, it may be possible that too many requests are waiting at
the other end or there may be zero or few requests pending at the scanned area.
These situations are avoided in CSAN algorithm in which the disk arm instead of
reversing its direction goes to the other end of the disk and starts servicing the
requests from there. So, the disk arm moves in a circular fashion and this algorithm
is also like SCAN algorithm and hence it is known as C-SCAN (Circular SCAN).
Advantages:
• Provides more uniform wait time compared to SCAN

# 2.1.5 LOOK: It is like the SCAN disk scheduling algorithm except the difference
that the disk arm despite going to the end of the disk goes only to the last request to
be serviced in front of the head and then reverses its direction from there only. Thus,
it prevents the extra delay which occurred due to unnecessary traversal to the end of
the disk.

# 2.1.6 C-LOOK: As LOOK is like SCAN algorithm, in similar way, C-LOOK is
like C-SCAN disk scheduling algorithm. In C-LOOK, the disk arm despite going to
the end goes only to the last request to be serviced in front of the head and then from
there goes to the other end’s last request. Thus, it also prevents the extra delay which
occurred due to unnecessary traversal to the end of the disk.
Each algorithm is unique. Overall Performance depends on number and type of
requests


# further details

the following project is command based disk scheduling simulation.
