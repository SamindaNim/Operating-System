## Steps to Open PuTTY and Connect to a Server

1. **Open PuTTY** – Search for **PuTTY** and open it.
2. **Enter Server Details** – Use IP address: `172.16.140.150`
3. **Connect** – Click **Open**.
4. **Login** – Type your **username** and **password** (`789*asd`).
5. **Access Server** – You are now connected!

---

## Linux Commands Learnt

### `pwd`
- Shows your **current directory**.
- Default: `/home/username`

### `ls`
- Lists files and directories.
- `ls -l` – Detailed list (permissions, owner, size)
- `ls -a` – Show hidden files
- `ls -ltr` – Long list, sorted by time (oldest first)

---

## File Creation in Linux

### `touch`
- Creates an empty file or updates timestamp.

```bash
touch abc.txt
```

### `vi`
- Opens a file for editing.

```bash
vi filename.txt
```

- Press `i` to insert text.
- Press `Esc`, then type `:wq` to save and exit.

**Example Data (xyz.txt):**
```
John 32 Engineer
Jane 22 Student
Bob 33 Doctor
Mary 25 Teacher
Alice 32 Nurse
```

---

## Viewing File Content

### `more`
- View file **one page at a time**.

```bash
more abc.txt
```

### `less`
- View file with **scrolling support**.

```bash
less abc.txt
```

---

## Creating a CSV File

```bash
vi pqr.csv
```

---

## Searching for Files

- **Find a file by name**:
```bash
find . -name "file.txt"
```

- **Find all directories**:
```bash
find . -type d
```

- **Find all CSV files**:
```bash
find . -name "*.csv"
```

---

## Count Number of Lines in a File

```bash
wc -l xyz.txt
```

---

## Retrieve Columns and Rows

### `cut`
- 2nd column:
```bash
cut -d ',' -f2 pqr.csv
```

- 1st and 3rd column:
```bash
cut -d ',' -f1,3 pqr.csv
```

### `awk`
- 1st column:
```bash
awk -F ',' '{print $1}' pqr.csv
```

---

## Head and Tail Commands

- First 5 lines:
```bash
head -n 5 pqr.csv
```

- Last 2 lines:
```bash
tail -n 2 pqr.csv
```

---

## Extracting/Appending from One File to Another

- Append 2nd column to new file:
```bash
cut -d ',' -f2 pqr.csv >> pqrNew.csv
```

- Append first 3 rows:
```bash
head -n 3 pqr.csv >> rows.csv
```

---

## File Permissions in Linux

### Types

- **Read (r)**: View content
- **Write (w)**: Edit content
- **Execute (x)**: Run file or enter folder

### Example: `-rwxr-xr--`

| Owner | Group | Others |
|-------|-------|--------|
| rwx   | r-x   | r--    |

### Numeric (Octal) Values

- **Read** = 4
- **Write** = 2
- **Execute** = 1

| Code | Meaning                               |
|------|----------------------------------------|
| 777  | Full permissions for all              |
| 755  | Owner full, group/others read & exec  |
| 644  | Owner read/write, others read         |
| 700  | Full for owner only                   |

---

## Windows Command Prompt – `ATTRIB` Command

- **Create files**: `abc.txt` and `xyz.txt`

### Hide a file
```cmd
ATTRIB +H abc.txt
```

### Unhide a file
```cmd
ATTRIB -H xyz.txt
```

### Make file read-only
```cmd
ATTRIB +R abc.txt
```

---
