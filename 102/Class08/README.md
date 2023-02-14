## Class 8 Reading Notes

### Operators and Loops
_______
At a high level, an __expression__ is a valid unit of code that resolves to a value. There are two types of expressions: those that have side effects (such as assigning values) and those that purely evaluate.  
- The expression ```x = 7``` is an example of the first type. This expression uses the ```=``` _operator_ to assign the value seven to the variable ```x```. The expression itself evaluates to ```7```
- all complex expressions are joined by operators
- Operators join operands either formed by higher-precedence operators or one of the basic expressions
- The _precedence of operators_ determines the order they are applied when evaluating an expression

```
    const x = 1 + 2 * 3;
    const y = 2 * 3 + 1; 
```

- in the above example both expressions would result in 7 because ```*``` has precedence over ```+``` despite ```*``` and ```+``` coming in different orders; the ```*```-joined expression will always be evaluated first.  
        - [Here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence#table) is a table of operator precedence and caveats  
- __Binary Operators__ require two operands; one before and one after the operator i.e, ```x * y```. All binary operators in JavaScript are infix
-__Unary Operators__ require a single operand, either before (prefix) or after (postfix) the operator; ```!``` and ```typeof``` are examples of prefix operators while ```++``` and ```--``` are the __*only*__ postfix operators in JavaScript
- __Assignment Operators__ assign a value to its left operand based on the value of its right operand.
    - If an expression evaluates to an object, then the left-hand side of an assignment expression may make assignments to properties of that expression
    - If an expression does not evaluate to an object, then assignments to properties of that expression do not assign
    - It is an error to assign values to unmodifiable properties or to properties of an expression without properties (null or undefined)
    - Assignments can be used within a variable declaration (i.e., with ```const```, ```let```, or ```var```) or as standalone statements
    - By chaining or nesting an assignment expression, its result can itself be assigned to another variable. It can be logged, it can be put inside an array literal or function call, and so on
        - That means that x = f() evaluates into whatever f()'s result is, x += f() evaluates into the resulting sum x + f(), x **= f() evaluates into the resulting power x ** y, and so on.
        - In the case of logical assignments, x &&= f(), x ||= f(), and x ??= f(), the return value is that of the logical operation without the assignment, so x && f(), x || f(), and x ?? f(), respectively.
        - When chaining expressions without parentheses or other grouping operators like array literals, the assignment expressions are grouped right to left, but evaluated left to right
        - for all assignment operators other than = itself, the resulting values are always based on the operands' values before the operation.
        - Chaining assignments are strongly [discouraged](https://github.com/airbnb/javascript/blob/master/README.md#variables--no-chain-assignment)
-__Comparison operators__ compare its operands and return a logical value based on wheter the comparison is true.
    - operands can be numerical, string, logical, or object values. If operands are not the same type, JavaScript attempts to convert them to an appropriate type--usually to a numerical value--for the comparison.
    - [Here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#comparison_operators) is a table of comparison operators
- __Loops__ repeat an action some number of times. various loop mechanisms offer different ways to determine the start and end points of the loop
    - A ```for``` loop repeats until a specified condition evaluates to false.
    - When a ```for``` loop executes, the following occurs:
    ``` 
        for (initialization; condition; afterthought)
            statement  
    ```
    
    - The initialzing expression is executed; usually initializes one or more loop counters (syntax allows an expression of any degree of complexity). This expression can also declare variables.
    - The condition expression is evaluated. If the value of condition is true, the loop statements execute. Otherwise, the for loop terminates. (If the condition expression is omitted entirely, the condition is assumed to be true.)
    - The statement executes. To execute multiple statements, use a block statement ({ }) to group those statements.
    - If present, the update expression ```afterthought`` is executed.
    - Control returns to Step 2.