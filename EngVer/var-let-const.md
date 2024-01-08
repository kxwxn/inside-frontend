# *var, let, and const*

##### var, let, and const are all variable declaration keywords, but each has its own characteristics.

- var is limited to the scope of the function in which it is declared. In addition, variables declared with var can be reassigned. Hoisting initializes the variable at the same time, so it is initialized to undefined at first and then assigned a value at the declaration location of the function.

- let is limited to the scope of the block in which it is declared. In addition, variables declared with let can be reassigned. Hoisting goes into the Temporal dead zone (not initialized) and cannot access the let variable before it is initialized.


- const is the same as the part explained in let above. However, const must also be assigned a value at the time of declaration. If not, an error will occur when it is initialized to initialize it. In addition, if the value assigned to const is not a "string" or a number, but an object, the properties within the object can be changed after the declaration. However, it is not possible to reassign to another type. If you do not want to change the properties, you can use the Object.freeze method to make the properties completely unchangeable. In addition, an empty array can also be assigned at the time of declaration, and it is possible to add values to the array later.


Here is a more detailed translation of some of the key terms:

- Hoisting: The process of moving the declaration of a variable or function to the top of the scope in which it is declared.
- Temporal dead zone: The period of time between the declaration of a variable with let or const and the point at which it is initialized. During this period, the variable cannot be accessed.
- Object.freeze: A method that can be used to prevent changes to the properties of an object.
