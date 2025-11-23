# Task

![task-1](../images/task)

---

![image-1](../images/image-1 [PID])

`top=$( ... )`
- Creates a variable named top
- Stores the output of the command inside $( )

`ps -eo pid,comm,%cpu`
Displays running processes.

|Option |Meaning                         |
|-------|--------------------------------|
|-e	    | list all processes             |
|-o	    | choose specific output format  |
|pid	| process ID                     |
|comm	| command/process name           |
|%cpu	| CPU usage                      |

`--sort=-%cpu`
- Sort results by CPU usage
- (-) means descending order
- The most CPU-consuming process appears first (after header)

`| awk 'NR==2 {print $1, $2, $3}`
- NR==2 → look at line 2
- $1 → first column (205)
- $2 → second column (snapd)
- $3 → third column

**awk is a command-line tool used to read text, split it into columns, and process it.**

---
