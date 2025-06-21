## Bandit Level 2 → Level 3: My Approach

### **Goal**

Find the password for the next level, stored in a file called `spaces in this filename` in the home directory.

### **My Steps**

1. **List files in the directory:**
   I used `ls` to check what files were present, and I noticed a file named `spaces in this filename`.

2. **Read a file with spaces in its name:**
   Since the filename contained spaces, I knew I needed to put quotes around the filename to read it properly.
   I ran:

   ```
   cat "spaces in this filename"
   ```

   This let the terminal treat the entire phrase as a single filename, rather than separate arguments.

3. **Retrieve the password:**
   The password was displayed in the terminal, allowing me to proceed to the next level.

**Reflection:**
This challenge taught me the importance of handling filenames with spaces in the Linux command line, and how quoting the filename lets me interact with it easily.




