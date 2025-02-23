# F# Mutable Variable Swap Bug

This example demonstrates a common issue with mutable variables in F# when attempting to swap their values using a function.  The unexpected behavior arises from the fact that mutable variables in F# are passed by reference, leading to in-place modification of the original variables rather than a value swap.

**Bug:** The `swap` function doesn't swap the values as one might expect, instead modifying the original variables directly. 

**Solution:**  The solution involves creating a new tuple containing the swapped values, which avoids modifying the original variables.  Alternatively, you could use immutability which is typically preferred in F#.