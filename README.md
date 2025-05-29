#  Basic C Programs – Compilation & Execution

A collection of beginner-friendly C programs demonstrating basic syntax, data types, input/output, and variable usage.

---

## 1) Print Hello World

```c
#include<stdio.h>
int main() 
{
    printf("Hello World!");
    return 0;
}
```

**Execution:**
```bash
touch Hello.c
vi Hello.c
gcc Hello.c -o Hello
./Hello
# Output: Hello World!
```

---

## 2) Integer Data Type

```c
#include<stdio.h>
int main()
{
    int age=10;
    printf("%d", age);
    printf("size: %zu", sizeof(age));
    return 0;
}
```

**Execution:**
```bash
touch DataType.c
vi DataType.c
gcc DataType.c -o DataType
./DataType
# Output: 10size: 4
```

---

## 3) Character (`char`)

```c
#include<stdio.h>
int main()
{
    char character='z';
    printf("%c", character);    
    printf("\n%d", character);
    return 0;
}
```

**Execution:**
```bash
touch char.c
vi char.c
gcc char.c -o char
./char
# Output:
# z
# 122
```

---

## 4) Double Data Type

```c
#include<stdio.h>
int main()
{
    double number=12.45;
    printf("%lf", number);    
    return 0;
}
```

**Execution:**
```bash
touch double.c
vi double.c
gcc double.c -o double
./double
# Output: 12.450000
```

---

## 5) Float Data Type

```c
#include<stdio.h>
int main()
{
    float number=10.9f;
    printf("%f", number);    
    printf("\n%.1f", number);
    return 0;
}
```

**Execution:**
```bash
touch float.c
vi float.c
gcc float.c -o float
./float
# Output:
# 10.900000
# 10.9
```

---

## 6) Integer Variable

```c
#include<stdio.h>
int main()
{
    int age=25;
    printf("%d", age);
    return 0;
}
```

**Execution:**
```bash
touch variables.c
vi variables.c
gcc variables.c -o variables
./variables
# Output: 25
```

---

## 7) Variable Copy Example

```c
#include<stdio.h>
int main()
{
    int first_number = 25;
    printf("First Number:%d", first_number);
    
    int second_number = first_number;
    printf("Second Number:%d", second_number);
    return 0;
}
```

**Execution:**
```bash
touch variable01.c
vi variable01.c
gcc variable01.c -o variable01
./variable01
# Output: First Number:25Second Number:25
```

---

