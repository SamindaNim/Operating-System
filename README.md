### 1) Find the row of data which has the word "Engineering"
**Command:**
```bash
grep "Engineering" data.csv
```
**Output:**
```
102,Bob,25,50000,Engineering
105,Eve,28,60000,Engineering
108,Hank,32,68000,Engineering
```
**Explanation:**
- `grep`: Searches for patterns in a file.
- `"Engineering"`: The keyword to search.
- `data.csv`: The file to search in.

---

### 2) Find the number of columns in the first row
**Command:**
```bash
awk -F, '{print NF; exit}' data.csv
```
**Output:**
```
5
```
**Explanation:**
- `-F,`: Sets comma as the field separator.
- `NF`: Number of fields (columns).
- `exit`: Stops after the first line.

---

### 3) Find the number of columns in each row
**Command:**
```bash
awk -F ',' '{print NF}' data.csv
```
**Output:**
```
5
5
5
5
5
5
5
5
5
5
5
```
**Explanation:**
- Prints number of columns in each row.

---

### 4) Sort CSV by Salary in Reverse Order (Descending)
**Command:**
```bash
sort -t',' -k4,4r data.csv
```
**Explanation:**
- `-t','`: Sets comma as delimiter.
- `-k4,4r`: Sort by 4th column (Salary) in reverse order.

---

### 5) Sort CSV by Salary in Ascending Order (Numerical)
**Command:**
```bash
sort -t',' -k4,4n data.csv
```
**Explanation:**
- `-n`: Sorts numerically (ascending).

---

### 6) Lexicographical Reverse Sorting by Salary
**Command:**
```bash
sort -t',' -k4,4 -r data.csv
```
**Explanation:**
- Without `-n`, sorting is alphabetical, not numeric.

---

### 7) Reverse Numeric Sorting by Salary
**Command:**
```bash
sort -t',' -k4,4 -n -r data.csv
```
**Explanation:**
- `-n`: Numeric sort.
- `-r`: Reverse order.
- Header appears last due to text sorting.

---

### 8) Multi-Level Reverse Sorting: Department then Name
**Command:**
```bash
sort -t',' -k5,5 -k2,2 -r data.csv
```
**Explanation:**
- First sort by Department (column 5).
- Then sort by Name (column 2).
- `-r`: Reverse order for both levels.

---
