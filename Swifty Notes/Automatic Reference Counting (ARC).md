# Automatic Reference Counting (ARC)



## How it works

- Keeping the count of strong references
- The instance is not deallocated until the last strong reference is broken

## Retain Cycle (Strong Reference Cycle)

- Problem: Memory Leak
- Cause: two strong references pointing to each other
- Solution:
  - Weak references
  - Unowned References
    - Alwasys refers to an instance that has not been deallocated
    - Runtime error occurs when access unowned reference after the instance has been deallocated
    - An unowned optional reference can be nil

## Types that are managed by ARC (Reference Type)

- Class 
- Closure

## Types that are NOT managed by ARC (Value Type)

- Basic types, like Bool, Int, etc.
- Struct
- Enum
- Tuple