# CPP-BASICS
 
- **variables**
    ```cpp
    int x;
    x = 5
    ```
    this is a copy-assignment 
    ```cpp
    int x {5};
    ```
    this is a list initialization 
    ```cpp
    int a;         // default-initialization (no initializer)
    int b = 5;     // copy-initialization (initial value after equals sign)
    int c ( 6 );   // direct-initialization (initial value in parenthesis)
    // Modern initialization forms (preferred):
    int d { 7 };   // direct-list-initialization (initial value in braces)
    int e {};      // value-initialization (empty braces)
    ```
    **Copy initialization**: involves creating a temporary object and then copying it to the destination.
    **Direct Initialization**: more efficient initialization of complex objects.
    **List initialization**: disallows narrowing conversions, meaning it wouldnt allow int and double to get mixed up. 
    **Value initialization**: When a variable is initialized using an empty set of braces its a special form of list-initialization.
- **print statment**:
    ```cpp
    std::cout << "hello world";
    std::cout << 4;
    int x{5};
    std::cout << x;
    ```
    which pretty much means print "hello world", 5 and variable x = 5
    << -> is an inseration operator imagine it to be a conveyer belt sending suff to std::cout -> character output

    ```cpp
    std::cout << "Hi!" << std::endl; 
    ```
    endl -> end line and it will go to the next line after this

    in `std::count` there is a chance that data might get lost as it will get buffered and has a change to get flushed out. 

    endl is quite inefficient, just rather use `\n` instead like 

    ```cpp
    int x{ 5 };
    std::cout << "x is equal to: " << x << '\n'; // single quoted (by itself) (conventional)
    std::cout << "Yep." << "\n";                 // double quoted (by itself) (unconventional but okay)
    std::cout << "And that's all, folks!\n";     // between double quotes in existing text (conventional)
    return 0; 
    ```

    std::cin -> character input reads input from keyboard like how scanf works
    ```cpp 
    #include <iostream>  // for std::cout and std::cin
    int main()
    {
    std::cout << "Enter a number: "; // ask user for a number

    int x{};       // define variable x to hold user input (and value-initialize it)
    std::cin >> x; // get number from keyboard and store it in variable x

    std::cout << "You entered " << x << '\n';
    return 0;
    }
    ```
    you can input multiple values like `std::cin >> x >> y; `
    std::cin is also buffered
- **functions**: 
    Very similar to c, follows the pattern and same rules
    ```cpp
    returnType functionName() // This is the function header (tells the compiler about the existence of the function)
    {
    // This is the function body (tells the compiler what the function does)
    }
    ```





