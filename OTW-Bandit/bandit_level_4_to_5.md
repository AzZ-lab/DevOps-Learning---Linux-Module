
## Bandit Level 4 → Level 5: My Approach

### **Goal**

Find the password for the next level, which is stored in the only human-readable file in the `inhere` directory.

### **My Steps**

1. **Explore the directory:**
   I navigated into the `inhere` directory using `cd inhere` and ran `ls` to see the files. There were several files with names like `file00`, `file01`, etc.

2. **Identify readable files:**
   I wanted to find out which file was human-readable, so I used the `file` command on all the files:

   ```
   file ./*
   ```

   This command shows the type of each file. Most files were listed as `data`, but one of them, `./file07`, was identified as `ASCII text`.

3. **Read the password:**
   I used `cat ./file07` to print the contents of the readable file, and the password for the next level was revealed.



**Reflection:**
This level taught me how to quickly distinguish human-readable files from binary files using the `file` command—a useful technique when working with lots of unknown files in a directory.






