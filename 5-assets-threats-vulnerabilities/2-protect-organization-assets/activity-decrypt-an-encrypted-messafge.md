# Decrypt an encrypted message

## Activity Overview
In this lab activity, you’ll be guided through some basic cryptographic activities using Linux commands to decrypt files and reveal hidden messages.

### Scenario
You work for an educational technology company that developed an application to help teachers automatically grade assignments. The application handles a wide range of data that it collects from academic institutions, instructors, parents, and students.

Your team was alerted to a data leak of internal business plans on social media. An investigation by the team discovered that an employee accidentally shared those confidential documents with an external business partner. An audit into the leak is underway to determine how similar incidents can be avoided.

### Steps to decrypt messages

#### Task 1. Read the contents of a file
1. **List the files in the current working directory.**
   ```bash
   ls /home/analyst

Output:

```
Copy code
Q1.encrypted  README.txt caesar
```

1. Read the contents of the README.txt file.

   ```
   bash
   Copy code
   cat README.txt
   ```

   Output:

   ```
   css
   Copy code
   Hello,
   All of your data has been encrypted. To recover your data, you will need to solve a cipher. To get started look for a hidden file in the caesar subdirectory.
   ```

#### Task 2. Find a hidden file

1. **Change to the caesar subdirectory.**

   ```
   bash
   Copy code
   cd caesar
   ```

2. **List all files, including hidden files.**

   ```
   bash
   Copy code
   ls -a
   ```

   Output:

   ```
   Copy code
   .  ..  .leftShift3
   ```

3. **Read the contents of the .leftShift3 file.**

   ```
   bash
   Copy code
   cat .leftShift3
   ```

   Output (encrypted message).

4. **Decrypt the Caesar cipher in the .leftShift3 file.**

   ```
   bash
   Copy code
   cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"
   ```

   Output:

   ```
   css
   Copy code
   In order to recover your files you will need to enter the following command:
   
   openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
   ```

5. **Return to your home directory.**

   ```
   bash
   Copy code
   cd ~
   ```

#### Task 3. Decrypt a file

1. **Use the command revealed in .leftshift3 to decrypt the encrypted file.**

   ```
   bash
   Copy code
   openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute
   ```

2. **List the contents of your current working directory.**

   ```
   bash
   Copy code
   ls
   ```

   Output:

   ```
   Copy code
   Q1.encrypted  Q1.recovered  README.txt  caesar
   ```

3. **Read the contents of the Q1.recovered file.**

   ```
   bash
   Copy code
   cat Q1.recovered
   ```

   Output:

   ```
   arduino
   Copy code
   If you are able to read this, then you have successfully decrypted the classic cipher text. You recovered the encryption key that was used to encrypt this file. Great work!
   ```

## Conclusion

Great work! You now have practical experience in using basic Linux Bash shell commands to:

- List hidden files
- Decrypt a Caesar cipher
- Decrypt an encrypted file