# Create Hash Values

## Activity Overview
As a security analyst, implementing security controls to protect organizations against threats is crucial. Hashing is one such control. A hash function produces a unique code that can't be decrypted, allowing you to check if a file has been modified. This lab will guide you through creating hash values for two files and comparing them using Linux commands.

## Scenario
In this scenario, you need to investigate whether two files are identical or different. You will display the contents of two files, generate hashes for each, and compare them to determine any differences.

## Task 1: Generate Hashes for Files

### Step 1: List Directory Contents
Use the `ls` command to list the contents of the directory.
```sh
ls
```

You should see two files: `file1.txt` and `file2.txt`.

### Step 2: Display File Contents

Use the `cat` command to display the contents of each file.

```
sh
Copy code
cat file1.txt
cat file2.txt
```

Review the output:

```
plaintext
Copy code
analyst@4fb6d613b6b0:-$ cat file1.txt
X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*
analyst@4fb6d613b6b0:-$ cat file2.txt
X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*
```

**Question:** Do the contents of the two files appear identical when you use the `cat` command?

**Answer:** Yes. The contents appear identical.

### Step 3: Generate Hashes

Use the `sha256sum` command to generate the hash of each file.

```
sh
Copy code
sha256sum file1.txt
sha256sum file2.txt
```

Review the generated hashes:

```
plaintext
Copy code
analyst@4fb6d613b6b0:-$ sha256sum file1.txt
131f95c51cc819465fa1797f6ccacf9d494aaaff46fa3eac73ae63ffbdfd8267  file1.txt
analyst@4fb6d613b6b0:-$ sha256sum file2.txt
2558ba9a4cad1e69804ce03aa2a029526179a91a5e38cb723320e83af9ca017b  file2.txt
```

**Question:** Do both files produce the same generated hash value?

**Answer:** No. The generated hash values are different, indicating the file contents are not identical.

## Task 2: Compare Hashes

### Step 1: Write Hashes to Files

Use the `sha256sum` command to generate the hash for each file and send the output to new files.

```
sh
Copy code
sha256sum file1.txt >> file1hash
sha256sum file2.txt >> file2hash
```

### Step 2: Display Hash Values

Use the `cat` command to display the hash values in the `file1hash` and `file2hash` files.

```
sh
Copy code
cat file1hash
cat file2hash
```

Inspect the output and note the differences.

### Step 3: Compare Hashes

Use the `cmp` command to compare the two hash files byte by byte.

```
sh
Copy code
cmp file1hash file2hash
```

Review the output:

```
plaintext
Copy code
analyst@4fb6d613b6b0:-$ cmp file1hash file2hash
file1hash file2hash differ: char 1, line 1
```

**Question:** Based on the hash values, is `file1.txt` different from `file2.txt`?

**Answer:** Yes, the contents of the two files are different because the hash values are different.

## Conclusion

Great work! You have practiced how to:

- Compute hashes using `sha256sum`
- Display hashes using the `cat` command
- Compare hashes using the `cmp` command

These skills are valuable for validating data integrity and contributing to your organization’s security.