# Elixir Enum.each Modification Bug
This example demonstrates a common mistake when trying to modify a list while iterating over it using Enum.each in Elixir.  The code attempts to remove the element '3' from the list, but due to the immutability of Elixir data structures, this does not work as expected. The original list remains unchanged.

## Bug Description
The code iterates through a list and attempts to remove an element if it matches a certain condition. However, since lists are immutable in Elixir, attempting to reassign `list` within the `Enum.each` function does not modify the original list. The modification is local to the anonymous function's scope.

## Solution
The correct approach involves creating a new list without the unwanted element.  This can be achieved using list comprehension or Enum.filter.