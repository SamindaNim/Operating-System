# Palindrome Checker in Shell Script

This script checks whether a given word is a **palindrome** (a word that reads the same forwards and backwards).

---

## Script: `palindrome.sh`

```bash
echo "Enter the word: "
read word

reverse=$(echo "$word" | rev)

if [ "$word" == "$reverse" ]; then
    echo "It's a Palindrome."
else
    echo "Not a Palindrome."
fi
```

---

## Run Instructions

```bash
touch palindrome.sh       # Create the script file
vi palindrome.sh          # Paste the code inside
chmod 777 palindrome.sh   # Give execute permission
./palindrome.sh           # Run the script
```

---

## Example Output

```
[saminda@Saminda-PC ~]$ ./palindrome.sh
Enter the word:
amma
It's a Palindrome.
```

---

> A **palindrome** is a word or phrase that reads the same forward and backward, like `madam`, `racecar`, or `level`.

