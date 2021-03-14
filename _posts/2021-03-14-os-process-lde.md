---
title: OS - Process, LDE
layout: post
---

## Process API

- Running file should be on main memory
- CPU virtualization --> C - divide time sharing (process)
- machine state
- address space (cf) not physical memory space

#### Process States
  * Running
  * Ready
  * Blocked
  * Status stored in PCB (Process Control Block)
  
#### System Call
  - Create
  - Destory
  - Wait
  - Misc Control 


#### Fork
copy all status from parent process
only way to create process
return exit status when child process is done

#### Exec
Usually exetute after fork
play roles of loading
use when process whole other work (not condition)
cannot go back


## Mechanism: Limited Direct Execution
- 운영체제가 CPU를 control할 수 없을 때가 있다 --> time sharing X
- User mode
- Kernel Mode
	- Handle Interrpt via handler
	- Handle System Call (User using kernel mode)
	- I / O
 - Trap
   - 프로그램 카운터가 미리 약손된 지점으로 바뀜 (Trap Handler)
   - User mode --> Kernel Mode
   - 원인
     - Exception
       - internal error (zero division, page fault..)
     - Interrupt
       - external interrupt
       - tell who cause interrupt
       - IRET (return from interrupt)
       - timer interrupt
         - context switching (PCB)
     - System Call
       - fetch -> decode -> exec
       - trap handler judge why trap occur
