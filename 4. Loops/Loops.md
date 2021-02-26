# Loops in C++

Repeatedly execute a block of statements

### for() loop:

Syntax:

    for (initialization expr; test expr; update expr)
    {    
         // body of the loop
         // statements we want to execute
    }
    
### While Loop:

Syntax:

    initialization expression;
    while (test_expression)
    {
       // statements

      update_expression;
    }
    
### do while loop:

Syntax:

    initialization expression;
    do
    {
       // statements

       update_expression;
    } while (test_expression);
    
## Important Points:

- Use for loop when number of iterations is known beforehand, i.e. the number of times the loop body is needed to be executed is known.
- Use while loops where exact number of iterations is not known but the loop termination condition is known.
- Use do while loop if the code needs to be executed at least once like in Menu driven programs
