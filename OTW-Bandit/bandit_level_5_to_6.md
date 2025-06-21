


## Bandit Level 5 → Level 6: My Approach

### **Goal**

Find the password for the next level, which is hidden somewhere under the `inhere` directory and has these properties:

* Human-readable
* 1033 bytes in size
* Not executable

---

### **My Steps**

1. **Search recursively:**
   I used the `find` command to look through all files under the `inhere` directory, including subdirectories.

2. **Filter by size and permissions:**
   To match the required properties, I ran:

   ```
   find inhere/ -type f -size 1033c ! -executable
   ```

   This command finds all regular files (`-type f`) that are exactly 1033 bytes (`-size 1033c`) and are **not executable** (`! -executable`).

3. **Check the result:**
   The command returned the path to the file:
   `inhere/maybehere07/.file2`

4. **Read the password:**
   I used `cat inhere/maybehere07/.file2` to display the contents of the file and get the password for the next level.

---

**Reflection:**
This level was a great exercise in using the `find` command with multiple conditions, and it really showed how powerful Linux commands can be for searching through directories with specific requirements.

---


