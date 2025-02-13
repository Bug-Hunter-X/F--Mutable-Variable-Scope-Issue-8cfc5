# F# Mutable Variable Scope Issue

This example demonstrates a common issue in F# related to mutable variables and function scope.  When mutable variables are passed to a function, changes made inside the function do not affect the original variables outside its scope unless they are passed by reference (using `byref`).

The provided `bug.fs` file contains code that attempts to swap two mutable variables within a function. However, due to the scope issue, the values of `x` and `y` outside the `swap` function remain unchanged. The `bugSolution.fs` file showcases a corrected version that utilizes the `byref` keyword to achieve the intended effect.