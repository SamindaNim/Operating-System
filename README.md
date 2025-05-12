## 1. Get the Calendar and Current Day

### Command:
```bash
cal
date +%d
```

### Output:
```
$ cal
     April 2025
Su Mo Tu We Th Fr Sa
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
20 21 22 23 24 25 26
27 28 29 30

$ date +%d
06
```

### Explanation:
- `cal`: Displays the calendar of the current month.
- `date +%d`: Displays the **day of the month** (01 to 31) using the format `+%d`.

---

## 2. Get Student Name and Marks, Then Calculate Total and Average

### Command:
```bash
echo Enter the name:
read name
echo Enter the mark for subject1:
read mark1
echo Enter the mark for subject2:
read mark2
echo Enter the mark for subject3:
read mark3
total=$(($mark1 + $mark2 + $mark3))
average=$(($total / 3))
echo Total: $total
echo Average: $average
```

### Output:
```
Enter the name:
zaheeda
Enter the mark for subject1:
3
Enter the mark for subject2:
4
Enter the mark for subject3:
5
Total: 12
Average: 4
```

### Explanation:
- A new file `ghi.sh` was created and saved.
- Given execute permission using `chmod 777 ghi.sh`.
- Script prompts for name and marks, calculates total and average, and displays them.

---

## 3. Create Calculator with Arithmetic Operations

### Command:
```bash
echo Enter the first number:
read num1
echo Enter the second number:
read num2
sum=$(($num1 + $num2))
sub=$(($num1 - $num2))
div=$(($num1 / $num2))
mul=$(($num1 * $num2))
echo Summation: $sum
echo Subtraction: $sub
echo Division: $div
echo Multiplication: $mul
```

### Output:
```
Enter the first number:
45
Enter the second number:
4
Summation: 49
Subtraction: 41
Division: 11
Multiplication: 180
```

### Explanation:
- File `prgrm4.sh` was created, saved, and made executable.
- Script performs addition, subtraction, division, and multiplication.

---

## 4. Get Day Name Based on User Input (1–7)

### Command:
```bash
echo Enter the number:
read num
if [ "$num" -lt 8 ]; then
  if [ "$num" -eq 1 ]; then echo "Monday"
  elif [ "$num" -eq 2 ]; then echo "Tuesday"
  elif [ "$num" -eq 3 ]; then echo "Wednesday"
  elif [ "$num" -eq 4 ]; then echo "Thursday"
  elif [ "$num" -eq 5 ]; then echo "Friday"
  elif [ "$num" -eq 6 ]; then echo "Saturday"
  elif [ "$num" -eq 7 ]; then echo "Sunday"
  fi
else
  echo "Invalid Number"
fi
```

### Output:
```
Enter the number:
3
Wednesday
```

### Explanation:
- File `prgrm5.sh` created and executed.
- Displays weekday name for numbers 1–7, or "Invalid Number" otherwise.

---

## 5. Verify Whether Username is Correct

### Command:
```bash
echo Enter username:
read name
username=$(whoami)
if [ "$name" = "$username" ]; then
  echo username is correct
else
  echo username is incorrect
fi
```

### Output:
```
Enter username:
skyline
username is correct
```

### Explanation:
- File `prgrm6.sh` created and made executable.
- Uses `whoami` to compare input with actual username.

---

## 6. Compare Two Numbers

### Command:
```bash
echo Enter two numbers:
read num1 num2
if [ "$num1" -gt "$num2" ]; then
  echo $num1 is greater than $num2
elif [ "$num1" -eq "$num2" ]; then
  echo $num1 is equal to $num2
else
  echo $num1 is less than $num2
fi
```

### Output:
```
Enter two numbers:
10 5
10 is greater than 5
```

### Explanation:
- Script reads two numbers and compares them using conditional checks: `-gt`, `-eq`, and else.

---

## 7. Create Simple Calculator Using `expr` Command

### Command:
```bash
echo Enter the first number:
read num1
echo Enter the second number:
read num2
sum=$(expr $num1 + $num2)
sub=$(expr $num1 - $num2)
div=$(expr $num1 / $num2)
mul=$(expr $num1 \* $num2)
echo Summation: $sum
echo Subtraction: $sub
echo Division: $div
echo Multiplication: $mul
```

### Output:
```
Enter the first number:
10
Enter the second number:
5
Summation: 15
Subtraction: 5
Division: 2
Multiplication: 50
```

### Explanation:
- File `calc2.sh` created, saved, and made executable.
- Uses `expr` for arithmetic; multiplication uses `\*` to avoid shell interpretation.
