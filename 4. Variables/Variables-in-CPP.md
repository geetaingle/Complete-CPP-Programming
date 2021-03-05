# Variables in C++

A variable is a name given to a memory location


#### - Variable declaration:
It refers to the part where a variable is first declared or introduced before its first use.

#### - Variable definition:
It is a part where the variable is assigned a memory location and a value

There are three types of variables based on the scope of variables in C++:

1. Local Variables 
2. Instance Variables 
3. Static Variables


## Local Variables

A variable defined within a block or method or constructor is called local variable

- These variable are created when the block in entered or the function is called and destroyed after exiting from the block or when the call returns from the function.
- The scope of these variables exists only within the block in which the variable is declared. i.e. we can access these variable only within that block.


## Instance Variables

Instance variables are non-static variables and are declared in a class outside any method, constructor or block.

- These variables are created when an object of the class is created and destroyed when the object is destroyed
- Unlike local variables, we may use access specifiers for instance variables. If we do not specify any access specifier then the default access specifier will be used.
- Initilisation of Instance Variable is not Mandatory.
- Instance Variable can be accessed only by creating objects.

## Static Variables

- static variables are declared using the static keyword within a class
- we can only have one copy of a static variable per class irrespective of how many objects we create.
- created at the start of program execution and destroyed automatically when execution ends
- Initialization of Static Variable is not Mandatory. Its default value is 0
- If we access the static variable like Instance variable (through an object), the compiler will show the warning message and it won’t halt the program. The compiler will replace the object name to class name automatically.
- If we access the static variable without the class name, Compiler will automatically append the class name.

        #include <iostream> 
        using namespace std; 

        class Marks { 

        public: 
            // This is a class variable
            
            static int studentNumber; 

            // These variables are instance variables. 
            // These variables are in a class and are not inside any function 
            
            int engMarks; 

        public: 
            Marks() 
            { 
                // Modify the class variable 
                ++studentNumber; 
            }; 
        }; 

        // Setting the class variable of Marks 
        
        int Marks::studentNumber = 0; 
        
        int main() 
        { 

            // first object 
            Marks obj1; 
            obj1.engMarks = 50; 

            // second object 
            Marks obj2; 
            obj2.engMarks = 80;  

            // displaying marks for first object 
            cout << "Marks for first object:\n"; 
            cout << Marks::studentNumber << endl; 
            cout << obj1.engMarks << endl;  

            // displaying marks for second object 
            cout << "Marks for second object:\n"; 
            cout << Marks::studentNumber << endl; 
            cout << obj2.engMarks << endl; 
        } 
