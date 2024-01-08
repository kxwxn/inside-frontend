# *Block scope & Function scope differences*

- Block scope is basically anything enclosed in curly braces ({}). This includes conditional statements (if, else if, else), loops (for, while, do-while), functions (function, =>{}), object literals, classes, and try-catch blocks. Block scope is also related to the keywords let and const, which are good ways to solve the scope issues that were previously caused by the var keyword. This is because var is a function scope, so variables declared with var in nested blocks within a function will be hoisted by the function that encloses the block, which can cause problems when the variable is referenced or called.

- Function scope refers to the scope of only the function, without regard to other blocks. However, variables declared with var have a function scope, which, as mentioned earlier, can affect other blocks. For this reason, it is not recommended to declare variables with var.
