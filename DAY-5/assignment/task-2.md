# TASK-2

![task-2](../images/task-2.png)

---

    #!/bin/bash

    # Get private IP
    private_ip=$(hostname -I | awk '{print $1}')

    # Get public IP
    public_ip=$(curl -s ifconfig.me)

    echo "------ SERVER IP DETAILS ------"
    echo "Private IP: $private_ip"
    echo "Public IP:  $public_ip"

---

### QUICK SUMMARY TABLE

1. hostname -I         --> show private IP addresses
2. awk '{print $1}'    --> pick the first private IP
3. curl                --> get data from the internet (download info from a website)
4. curl -s ifconfig.me --> show public IP address (silent mode, no extra output)
5. variable=$(command) --> store command output in a variable
6. $variable           --> print stored value

---