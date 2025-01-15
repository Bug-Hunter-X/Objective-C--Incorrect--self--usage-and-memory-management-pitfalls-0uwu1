# Objective-C: Incorrect 'self' Usage and Memory Management Pitfalls

This repository demonstrates a common and subtle error in Objective-C programming: incorrect usage of `self` within methods, specifically focusing on the potential for infinite recursion and memory management problems.

## The Bug

The `bug.m` file showcases an example where incorrect usage of `self` inside a setter method leads to an infinite recursive call, resulting in a stack overflow.

The other example in `bug.m` demonstrates a potential memory leak caused by improper memory management and retain cycles.

## The Solution

The `bugSolution.m` file corrects both scenarios.  The infinite recursion issue is resolved by directly assigning the value to the property, thereby avoiding the unintended recursive call.  The memory management issue is addressed by carefully managing object ownership using `weak` references where appropriate, preventing retain cycles.