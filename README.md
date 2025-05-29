## (01) Multiplication Table Generator

**Filename:** `multable.sh`  
**Description:** Prints the multiplication table (up to 12) for a number provided by the user.

```bash
echo 'Enter the number that you want to get multiplication table:'
read num

for ((i=1; i<=12; i++))
do
  mul=$(($num * $i))
  echo "$num x $i = $mul"
done
```

### Run Instructions:
```bash
chmod 777 multable.sh
./multable.sh
```

### Example Output:
```
Enter the number that you want to get multiplication table:
5
5 x 1 = 5
5 x 2 = 10
...
5 x 12 = 60
```

---

##  (02) Star Patterns

**Filename:** `starpattern.sh`

---

### (I) Diamond Star Pattern

```bash
rows=5

# Top Half
for ((i=1; i<=rows; i++))
do
  for ((j=i; j<rows; j++)) 
  do 
    echo -n " " 
  done
  for ((k=1; k<=2*i-1; k++)) 
  do 
    echo -n "*" 
  done
  echo
done

# Bottom Half
for ((i=rows-1; i>=1; i--))
do
  for ((j=rows; j>i; j--)) 
  do 
    echo -n " " 
  done
  for ((k=1; k<=2*i-1; k++)) 
  do 
    echo -n "*" 
  done
  echo
done
```

#### Output:
```
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *
```

---

### (II) Hollow Square Pattern

```bash
rows=5

for ((i=1; i<=rows; i++))
do
  for ((j=1; j<=rows; j++))
  do
    if [[ $i -eq 1 || $i -eq $rows || $j -eq 1 || $j -eq $rows ]]
    then
      echo -n "*"
    else
      echo -n " "
    fi
  done
  echo
done
```

#### Output:
```
*****
*   *
*   *
*   *
*****
```

---

## (03) Fibonacci Series (First 10 Terms and Sum)

**Filename:** `fibonacci.sh`  
**Description:** Displays the first 10 Fibonacci numbers and their summation.

```bash
a=0
b=1
sum=0

echo 'First 10 Fibonacci numbers'

for ((i=1; i<=10; i++))
do
  echo $a
  sum=$((sum + a))
  c=$((a + b))
  a=$b
  b=$c
done

echo "Summation: $sum"
```

### Output:
```
First 10 Fibonacci numbers
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
Summation: 88
```

---

##  (04) Sum of Prime Numbers from 1 to 100

**Filename:** `prime_sum.sh`  
**Description:** Calculates and prints the sum of all prime numbers between 1 and 100.

```bash
sum=0

for (( num=2; num<=100; num++ ))
do
    is_prime=1
    for (( i=2; i*i<=num; i++ ))
    do
        if (( num % i == 0 ))
        then
            is_prime=0
            break
        fi
    done

    if (( is_prime == 1 ))
    then
        sum=$((sum + num))
    fi
done

echo "Sum of prime numbers between 1 and 100 is: $sum"
```

###  Output:
```
Sum of prime numbers between 1 and 100 is: 1060
```


