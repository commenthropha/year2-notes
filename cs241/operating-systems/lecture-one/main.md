# Introduction to Operating Systems
## What is an operating system?
### Definition
Broadly: a software acting as an intermediary between the user of a device and the hardware of the device
## Purpose of the OS
The OS is responsible for allocating [[Computer Resources]] to user *processes* and **control their execution**. (note the distinction between [[Program vs Process]])

The goal of the operating system at all times is to **avoid failures and errors**.
## Operating System Structure

![[Pasted image 20231002112438.png]]
## Roles of the OS
- [[Program Execution]]
- [[IO Operations]]
- [[File System Management]]
- [[Communications]]
- [[Error Handling]]
- [[Resource Allocation]]
- [[Accounting]]
- [[Protection and Security]]
# Kernel
A significant part of an operating system is the [[Kernel]]
## Kernel Space vs User Space
**Kernel space** is the part of memory where the kernel executes.

**User space** is the section of memory where user processes run.

Kernel space is kept protected from the user space, however it can be accessed through [[System Calls]]
### How to distinguish between the two?
We are able to distinguish between OS operations and user operations using [[Dual Mode Operation]]
















