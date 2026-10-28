# First Web Page Deployed

**Student:** Mateo Daniel Ortuño Ovando  
**Environment:** Ubuntu Server running in VirtualBox  
**Date:** [22 Oct 2026]

---

## Step 1. Check Apache Web Server Status
The Apache server is running and configured on a custom port for this exercise. Checking the listening sockets with the command `sudo netstat -tulpn | grep apache2`, We obtain the following result:

```text
tcp6       0      0 :::8777                 :::*                    LISTEN      1039/apache2
```

* **Note about the port:** As seen in the terminal output, the Apache server on this virtual machine uses port **8777** instead of the default port 80.


---

## Step 2. Directory and File Information (`/var/www/html`)

When listing the contents of the directory `/var/www/html` with comand
 `ls -la /var/www/html`, The available web files are identified.

### Answers to the questions regarding `index.html`:

* **Who is the owner of this file?**  
  The owner is **root**.
* **What is the group?**  
  The group is **root**.
* **What permissions does it have?**  
  It has **`-rw-r--r--`** (Read and write for the owner, read-only for the group and others).
* **What is the size?**  
  The size is **358 bytes**.
* **What is the update date/time for this file?**  
  It was last updated on **Oct 22 08:11**.

---

## Step 3. Verification and Local Testing
To verify the site's functionality internally within the server, the test command was executed pointing to the configured port:


```bash
curl localhost:8777
```

The server responded correctly, returning the custom web page structure.


---

## Step 4. Web Browser Screenshot

To fulfill the final requirement of the practice, the web page was accessed from the host system's browser (Windows) using the Ubuntu server's IP address along with port **8777**:


`http://http://192.168.1.211/:8777`.

<img width="1430" height="377" alt="Image" src="https://github.com/user-attachments/assets/d423cca4-b440-41b6-b9dc-2db9a0019c86"/>

@COMAND TEST
<img width="851" height="785" alt="Image" src="https://github.com/user-attachments/assets/aa54cb98-9279-4bde-84d2-abd37275c790"/>
