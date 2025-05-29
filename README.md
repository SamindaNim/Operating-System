##  Fibonacci Series

**File**: `fibonacci.sh`  
**Description**: Displays the first 10 numbers in the Fibonacci sequence.

```bash
# fibonacci.sh

a=0  # Initialize the first number in the Fibonacci sequence
b=1  # Initialize the second number

echo 'First 10 fibonacci numbers'  # Heading message

for((i=0;i<=10;i++))  # Loop 11 times (0 to 10)
do                    
  echo $a             # Print current number
  echo " "
  c=$(($a+$b))        # Next number = a + b
  a=$b                # Update a
  b=$c                # Update b
done
```

**Output:**
```
First 10 fibonacci numbers
0

1

1

2

3

5

8

13

21

34

55
```

---

## Factorial Calculation

**File**: `fact.sh`  
**Description**: Prompts the user to enter a number and calculates its factorial.

```bash
# fact.sh

echo 'Enter the number:'  # Prompt
read num                  # Read input
fact=1                    # Initialize factorial
for((i=1;i<=num;i++))
do
  fact=$(($fact*$i))      # fact = fact * i
done
echo "Factorial of number:$fact"  # Output result
```

**Example Output:**
```
Enter the number:
5
Factorial of number:120
```

---

## Multiples of 3 (1–50)

**File**: `mul.sh`  
**Description**: Prints all multiples of 3 between 1 and 50.

```bash
# mul.sh

num=50/3  # Divide 50 by 3 (not needed, see note below)

for((i=1;i<=16;i++))  # 16 multiples from 3*1 to 3*16 = 48
do
  mul=$((3*$i))
  echo $mul
done
```

**Output:**
```
3
6
9
12
15
18
21
24
27
30
33
36
39
42
45
48
```

---

## How to Run the Scripts

1. Open a terminal and create the script files:
```bash
touch fibonacci.sh
touch fact.sh
touch mul.sh
```

2. Edit the files using `vi` or any text editor:
```bash
vi fibonacci.sh
vi fact.sh
vi mul.sh
```

3. Give execution permission:
```bash
chmod 777 fibonacci.sh
chmod 777 fact.sh
chmod 777 mul.sh
```

4. Run the scripts:
```bash
./fibonacci.sh
./fact.sh
./mul.sh
```
