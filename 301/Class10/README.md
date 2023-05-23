# In memory storage

## Understanding the JavaScript Call Stack

1. What is a ‘call’?
    - In the context of the article, a 'call' refers to the invocation of a function. When a function is called, it is pushed onto the call stack.
2. How many ‘calls’ can happen at once?
    - The call stack in JavaScript is single-threaded, which means only one function call can happen at a time. JavaScript executes function calls synchronously, one after another, from top to bottom on the call stack.
3. What does LIFO mean?
    - LIFO stands for Last In, First Out. In the context of the call stack, it means that the last function that is pushed onto the stack is the first one to be popped off and executed when it reaches the top of the stack. The call stack operates like a stack data structure, where the most recently added function is the next one to be processed.
4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
    - 
5. What causes a Stack Overflow?
    - A stack overflow occurs when there is a recursive function (a function that calls itself) without a proper exit condition.

## JavaScript error messages

1. What is a ‘reference error’?
    - An error that occurs when you try to use a variable that has not been declared or is not accessible in the current scope.
2. What is a ‘syntax error’?
    - An error that happens when there is a mistake in the syntax of your code that prevents it from being parsed correctly. It could be an invalid object in JSON parsing or a trailing comma in a function call.
3. What is a ‘range error’?
    - A error that occurs when you manipulate an object with a length property and provide an invalid length value. For example, trying to set a negative length for an array.
4. What is a ‘type error’?
    - An error that happens when you try to access or use a value that is of an incompatible type. For instance, accessing a property of an undefined variable or trying to perform an operation on incompatible data types.
5. What is a breakpoint?
    - A 'breakpoint' is a point in your code where the execution will pause, allowing you to inspect the program state and variables at that particular moment. It is useful for debugging and understanding how your code behaves.
6. What does the word ‘debugger’ do in your code?
    - The word 'debugger' is a statement you can include in your code to create a breakpoint at that specific line. When the code is executed, it will pause at the debugger statement, allowing you to examine the program state and debug any issues.