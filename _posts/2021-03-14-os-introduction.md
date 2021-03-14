---
title: OS - Introduction
layout: post
date: '2021-03-14 14:06:16 +0900'
categories:
- OS
---

# Virtualizing
## CPU
Virtualize CPU to handle multiple (process, thread, program)
## Memory
Allocation from heap
Use virtualized memory address (PID)
# Concurrency
# Persistence
Abstract externel device via file
Flush memory when program end

# ?Difference between
```
char *temp = "Hello, World!"; --> reference pointer where string "Hello, World!" located
char temp[] = "Hello, World!"; --> allocated in stack
```
# Summary
실행 파일에는 전역 변수 및 코드가 존재한다. 지역 변수를 실행 시에 스택에서 할당받는다.
전역 변수는 초기값이 주어지지 않으면 0 이나 NULL이다.
