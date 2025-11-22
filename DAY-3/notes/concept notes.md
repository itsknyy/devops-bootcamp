# Linux Permissions 

## 1. Default Linux Permissions.

When a new **file** or **folder** is created, Linux assigns default permissions before `unmask` subtracts them.

**Default (before unmask)**

- Files: 666 --> rw-rw-rw
    - no execute`(x)`by default for safety.
- Directories: 777 --> rwxrwxrwx

**Why?**

- Files need read and write by default.
- Directories need execute (x) to allow entering.

---

## 2. unmask

`unmask` defines which permission to remove from the default.

**Formula**

    Final Permission = Default Permission − umask

**Example**

- Default file: 666
- umask       : 022
- Result      : 644 --> rw-r--r--

---

## 3. SUID (Set User ID)

SUID allow a file to run **with the file owner's permissions** instead of users.

**Symbol**

    s at the user(owner) position  (e.g., rwsr-xr-x)

    NOTE: Numeric value: 4XXX

**Set SUID**

    chmod u+s filename

---

## 4. SGID (Set Group ID)

SGID makes **files or folders** run or behave with the **group’s permissions**, not the user’s own permissions.

**Symbol**

    s in the group permission position (e.g., rwxr-sr-x)
    
    NOTE: Numeric value: 2XXX

**Set SGID**

    chmod g+s filename

---

## 5. Sticky Bit

Prevents users from deleting other user's file inside shared directory.

**Symbol**

    t in others permission (e.g., rwxrwxrwt)

    NOTE: Numeric value: 1XXX
    t = sticky + executable
    T = sticky + no executable

**Set SGID**

    chmod +t directory

---

