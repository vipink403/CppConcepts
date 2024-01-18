# Type casting:

## Why casting? 
Casts are used to convert the type of an object, expression, function argument, or return value to that of another type.


<details>
  <summary>C-Style casting (Very Bad Idea)</summary>

1. Casting is performed when a value (variable) of one type is used in place of some other type.

   ```c++
   int i = 3;
   double d = 2.5

   double result = d / i; // i is cast to double and then used
   ```
    
</details>


## (Silent)Implicit conversions:
The standard C++ conversions and user-defined conversions.

## Explicit Conversions:
Type is needed for an expression that cannot be obtained through an implicit conversion more than one standard conversion creates an ambiguous situation.

## To perform a type-cast, the compiler:
a)	May Allocate temporary storage if required.

b)	Initialize temporary with value being cast.

```c++
double f(int i, int j) { return (double) i / j; }
```

```c++
// Compiler generates the above code snippet as below:
double f(int i, int j)
{
    double temp_i = i, temp_j = j; // conversion in temporary
    return temp_i / temp_j;
}
```

In the above code, since the numerator (i) is explicitly type casted to double and denominator (j) is int, compiler will implicitly typecast j to double and will perform division. 
