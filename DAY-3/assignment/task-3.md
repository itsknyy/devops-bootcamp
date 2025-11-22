# Apply Correct Permissoions

![task-3](../images/task-3.png)

---

![task-3a](../images/task-3a.png)

    ls -ld source/ =  Shows detailed info (permissions, owner, group) of the source directory only.

    chown :devteam /var/www/project/source/ = 
    - chown    -> change ownership
    - :devteam -> change only the group to devteam (owner stays the same)
    - Makes devteam the group owner of the folder.

    chmod 2770 source/ = gives full access to owner + group, no access to others, and enables setgid (new files inherit the devteam group).

---

![task-3b](../images/task-3b.png)

    nano /etc/bashrc

    groups $USER | grep -q devteam = 
    This checks if the current user is a member of the devteam group.

    umask 002
    If the user is in devteam, this sets default permissions so new files and folders are group-writable.
    - Directories → rwxrwxr-x
    - Files → rw-rw-r--

---

![task-3c](../images/task-3c.png)

    chmod 3770 logs/ =  sets the following permissions:
    - 3 = SUID + sticky bit
    - 7 = full access for owner
    - 7 = full access for group
    - 0 = no access for others

    ls -ld logs/ = shows the updated permission of logs

    t = Sticky bit + others can enter the directory (x present)
    T = Sticky bit + others cannot enter the directory (x not present)

---

![task-3d](../images/task-3d.png)

    chmod 4750 deploy.sh = 
    - 4 = SUID (script runs with the owner's permissions)
    - 7 = owner has full access
    - 5 = group has read + execute
    - 0 = others have no access

---

![task-3e](../images/task-3e.png)

    chmod 2770 shared/ = 
    - 2 = setgid (new files inherit the group devteam)
    - 7 = owner has full access
    - 7 = group has read + execute
    - 0 = others have no access

---