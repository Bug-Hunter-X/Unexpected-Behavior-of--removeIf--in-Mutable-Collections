# Kotlin `removeIf` Function Gotcha

This repository demonstrates an unexpected behavior of the `removeIf` function in Kotlin's mutable collections (Lists and Sets).

The issue is that `removeIf` modifies the original collection directly, rather than returning a new collection. This can lead to unexpected side effects if not handled carefully.

**File: `bug.kt`**: This file shows the problematic behavior. The `removeIf` function alters the original list and set.

**File: `bugSolution.kt`**: This file offers an alternative approach to ensure predictable behavior.

**How to reproduce**: Run the `bug.kt` file. Observe that the `list` and `set` are directly modified after the `removeIf` call.

**Solution**: Use filter and toMutableList() or toMutableSet() for creating a new list or set with the desired elements.