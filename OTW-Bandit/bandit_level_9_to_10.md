## Bandit Level 9 → Level 10: My Approach

### **Goal**

Find the password for the next level, which is stored in the file `data.txt`, in one of the few human-readable strings, preceded by several ‘=’ characters.

---

### **My Steps**

1. **Check the file contents:**
   I started by running `cat data.txt`, but most of the content was unreadable binary data.

2. **Attempt to grep for clues:**
   I tried using `grep` directly to search for lines with `===`, `==`, and even `=`:

   ```
   grep === data.txt
   grep "==" data.txt
   grep "=" data.txt
   ```

   Each time, I got “binary file matches” but no readable output.

3. **Use regular expressions and further grep attempts:**
   I tried a regular expression to match lines starting with `=`, but still only got “binary file matches.”

4. **Switch to extracting readable strings:**
   I realized the file was binary, so I used the `strings` command to extract all human-readable text:

   ```
   strings data.txt
   ```

   Then I piped the output to `grep` to filter for lines with `=`:

   ```
   strings data.txt | grep "="
   ```

   This finally showed the readable lines with several `=` characters, including the one that contained the password.

---

**Reflection:**
This level showed me how to handle binary files on the command line and use tools like `strings` to extract useful text. It also reinforced the value of combining commands with pipes to efficiently find the exact information I needed.

---

*(Add your screenshot here for documentation!)*

