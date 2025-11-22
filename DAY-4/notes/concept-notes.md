## 1. LINUX ARCHITECTURE

**1. Hardware**
- Physical core parets: CPU, RAM, DISK.

**2. Kernal**
- Core of LINUX.
- Controls hardware, memory, drives.

**3. System Libraries**
- Help programs talk with kernal.

**4. System Utilities**
- Basic commands and tools.
- Examples: ls, cp, mv.

**5. User Applications**
- Software that user runs.

---

## 2. INTERACTIVE SHELL

- Shell that takes commands from the user.
- You type commands --> shell executes.
- Show a prompt like like `$`
- Example: opening Terminal and typing `ls`

---

## 3. NON-INTERACTIVE SHELL

- Shell that runs commands automatically without user input.
- Used for scripts, cron jobs, startup tasks.
- Example: running bash `script.sh`.

---

## 4. SUBSHELL

- A child shell created by the main shell.
- It can run commands without affecting the parent shell.

**Example**

    pwd
    (cd /tmp)
    pwd  # still same directory

---