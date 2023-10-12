# Let's Mastering Linux Permissions and chmod - Your guide to complete control over file access in Linux.

<p align="center">
   <img src="https://github.com/bhavesh-pardhi/Chmod-Mastery/blob/main/image/chmod-linux-example-4.png"alt="Chmod">
</p>


> In Linux, file and directory permissions are essential for controlling who can access, modify, or execute files and directories. Permissions are represented by a 10-character string, such as "drwxr-xr-x" for a directory or "-rw-r--r--" for a file. Let's break down what each character in the string represents:


1. The first character indicates the file type:
   - "d" for directories
   - "-" for regular files
   - "l" for symbolic links


2. The next nine characters are divided into three groups of three:
   - The first group (characters 2-4) represents the owner's permissions.
   - The second group (characters 5-7) represents the group's permissions.
   - The third group (characters 8-10) represents everyone else's (others) permissions.


Each group of three characters represents the permissions in the following order:


- *"r" (read): If this permission is set, the file or directory can be read.*
- *"w" (write): If this permission is set, the file or directory can be modified.*
- *"x" (execute): If this permission is set, the file (for directories) can be entered or executed.*


To change these permissions, you can use the "chmod" command. For example:


- To give read, write, and execute permissions to the owner of a file:
  ```
  chmod u+rwx filename
  ```

- To give read and execute permissions to the group:
  ```
  chmod g+rx filename
  ```

- To remove write permission from others:
  ```
  chmod o-w filename
  ```

# ▪️ You can also use numeric values to represent permissions:


**Certainly! In Linux, file and directory permissions can be represented using numeric values, which are a more compact way of specifying permissions compared to the symbolic representation (like "rwx" for read, write, and execute). Numeric values are calculated based on a combination of the three basic permissions: read, write, and execute.**


Here's how you can calculate numeric values for permissions:


*1. Read (r) permission is represented by the value `4`.*
*2. Write (w) permission is represented by the value `2`.*
*3. Execute (x) permission is represented by the value `1`.*


To assign permissions using numeric values, you need to add up these values based on the permissions you want to grant. For example:


- To give read and write permissions to the owner and read permission to the group and others, you would calculate it as:
  - Owner (read + write) = 4 + 2 = 6
  - Group (read) = 4
  - Others (read) = 4


You would then use these values with the "chmod" command like this:

```
chmod 644 filename
```

Here's what each digit in "644" means:


- The first digit (6) represents the owner's permissions (read + write).
- The second digit (4) represents the group's permissions (read).
- The third digit (4) represents others' permissions (read).


# ▪️ explanations and examples for the owner, group, and others:


1. `7` (Owner: Read, Write, Execute; Group: Read, Write, Execute; Others: Read, Write, Execute)
   - Example: `chmod 777 filename`
   - Explanation: This grants full permissions to the owner, group, and others, allowing them to read, write, and execute the file or directory.


2. `6` (Owner: Read, Write; Group: Read, Write; Others: Read)
   - Example: `chmod 664 filename`
   - Explanation: The owner and group have read and write permissions, while others have only read permission.


3. `5` (Owner: Read, Execute; Group: Read, Execute; Others: Read, Execute)
   - Example: `chmod 555 filename`
   - Explanation: The owner, group, and others can read and execute the file or directory, but they cannot modify it.


4. `4` (Owner: Read; Group: Read; Others: Read)
   - Example: `chmod 444 filename`
   - Explanation: All users can only read the file or directory, and they cannot modify or execute it.


5. `3` (Owner: Write, Execute; Group: Write, Execute; Others: Write)
   - Example: `chmod 333 filename`
   - Explanation: All users can write and execute the file or directory, but they cannot read it.


6. `2` (Owner: Write; Group: Write; Others: Write)
   - Example: `chmod 222 filename`
   - Explanation: All users can write the file or directory, but they cannot read or execute it.


7. `1` (Owner: Execute; Group: Execute; Others: Execute)
   - Example: `chmod 111 filename`
   - Explanation: All users can execute the file or directory, but they cannot read or write it.


8. `0` (Owner: No permissions; Group: No permissions; Others: No permissions)
   - Example: `chmod 000 filename`
   - Explanation: No one has any permissions, effectively locking the file or directory.


***The numeric representation is concise and can be useful for scripting and automation. Just remember the values for the basic permissions: 4 for read, 2 for write, and 1 for execute, and then add them together as needed for the owner, group, and others.***


# ▪️ Conclusion:

***Thank you for being part of our wonderful community. Together, we can achieve great things!***

# ▪️ Follow Author

[![Twitter](https://img.shields.io/twitter/url?label=Twitter&logo=twitter&style=social&url=https%3A%2F%2Ftwitter.com%2FYourTwitterHandle)](https://twitter.com/Bhavesh_Pardhi_)
[![LinkedIn](https://img.shields.io/badge/LinkedIn--blue?style=social&logo=linkedin)](https://www.linkedin.com/in/bhavesh-pardhi-)
[![GitHub](https://img.shields.io/badge/GitHub--black?style=social&logo=github)](https://github.com/bhavesh-pardhi)
[![Snapchat](https://img.shields.io/badge/Snapchat--yellow?style=social&logo=snapchat)](https://www.snapchat.com/add/bhaveshpardhi0)
[![Instagram](https://img.shields.io/badge/Instagram--purple?style=social&logo=instagram)](https://www.instagram.com/bhavesh_pardhi_)
[![HackerOne](https://img.shields.io/badge/HackerOne--red?style=social&logo=hackerone)](https://hackerone.com/bhavesh_cxs)


- ***If you find value in these free wordlists and tools, consider showing your appreciation by buying me a coffee. Your support helps keep this project going and enables the continuous improvement of these resources.***

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
