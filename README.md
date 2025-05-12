# TAB-SEPARATED FILES IN LINUX  

---

## 01. Creating a TSV File

**Command:**
```bash
vi abc.tsv
```

**Steps:**
1. Type `vi abc.tsv` to open the editor.
2. Press `i` to enter insert mode.
3. Enter the following sample data (separate using TAB):

```
11	22	44	55  
88	99	77	55  
22	66	00	33  
11	22	77	88
```

4. Press `Esc`, type `:wq`, and hit `Enter` to save and exit.

---

## 02. Extracting Columns from a TSV File

### Extract Column 1 using `cut`
```bash
cut -d $'	' -f1 abc.tsv
```

- `cut`: Extracts specific fields.
- `-d $'	'`: Specifies TAB as the delimiter.
- `-f1`: Extracts the first column.

**Output:**
```
11  
88  
22  
11
```

### Extract Column 3 using `awk`
```bash
awk '{print $3}' abc.tsv
```

- `$3`: Refers to the 3rd column.

**Output:**
```
44  
77  
00  
77
```

---

## 03. Displaying Rows from a TSV File

### Display the First 2 Rows
```bash
head -n 2 abc.tsv
```

**Output:**
```
11	22	44	55  
88	99	77	55
```

### Display the Last 2 Rows
```bash
tail -n 2 abc.tsv
```

**Output:**
```
22	66	00	33  
11	22	77	88
```

### Display the 4th Row
```bash
head -n 4 abc.tsv | tail -n 1
```

**Output:**
```
11	22	77	88
```

---

## 04. Display Entire Content of the TSV File
```bash
awk '{print}' abc.tsv
```

**Output:**
```
11	22	44	55  
88	99	77	55  
22	66	00	33  
11	22	77	88
```

---

## 05. File Structure Information

### Display Number of Fields (Columns)
```bash
awk '{print NF; exit}' abc.tsv
```

**Output:**
```
4
```

### Count Fields Using `awk` with TAB Separator
```bash
awk -F '\t' '{print NF; exit}' abc.tsv
```

**Output:**
```
4
```

### Retrieve the Number of Lines
```bash
wc -l abc.tsv
```

**Output:**
```
4 abc.tsv
```

---

## 06. Searching Specific Content

### Display Lines Containing `88` from First 5 Lines
```bash
head -n 5 abc.tsv | grep '88'
```

**Output:**
```
88	99	77	55  
11	22	77	88
```

---
