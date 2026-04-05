# Day 05 - [Archiving & Compression in Linux (tar, gzip, zip, xz]

## Objective

The goal for today is to understand how Linux handles file archiving and compression for storage, transfer, and system efficiency.

By the end of today, I should be able to:

Understand the concept of archiving vs compression
Use tar to create, extract, and manage archives
Apply compression using gzip, bzip2, and xz
Understand and use zip and unzip
Identify when to use each compression tool in real-world scenarios

---

## What I Learned

- Archiving vs Compression:
    - Archiving → Combining multiple files into one (.tar)
    - Compression → Reducing file size (.gz, .bz2, .xz, .zip)
- tar (Tape Archive):
    -Used to bundle files and directories
    - Preserves file structure and permissions

`tar -cvf archive.tar files/ `

- Extract archive:

`tar -xvf archive.tar`

- Common options:

-c → create archive
-x → extract archive
-v → verbose output
-f → file name

### Compression with tar
- Gzip compression:
    - tar -cvzf archive.tar.gz files/
    - tar -xvzf archive.tar.gz
- Bzip2 compression:

    - tar -cvjf archive.tar.tbz files/
    - tar -xvjf archive.tar.tbz

- xz
    - High compression efficiency (slower but smaller size):
        - xz file.txt
    - Decompress:
        - xz -d file.txt.xz
    - Keep original:
        - xz -k file.txt
- zip and unzip
    - Compress files:
        - zip archive.zip file1 file2
    - Compress directory:
        - zip -r archive.zip folder/
    - Extract:
- unzip archive.zip

- Wildcards in Archiving
    - * → matches multiple characters
    - ? → matches a single character

- Example:

`tar -cvf archive.tar *.txt`
---

## What I Practiced

- Created archive files:
`tar -cvf project.tar project/`

- Extracted archives:
`tar -xvf project.tar`

- Created compressed archives:
`tar -cvzf project.tar.gz project/`

`tar -cvjf project.tar.tbz project/`

- Compressed files using gzip:
`gzip file.txt`

`gzip -k file.txt`

- Compressed files using xz:
`xz file.txt`

- Used zip for multi-file compression:

`zip -r project.zip project/`

- Extracted zip archives:
`unzip project.zip`

## Challenges Faced

- Choosing the appropriate compression tool based on use case

---

## Key Takeaways

- tar is primarily for archiving, while tools like gzip, bzip2, and xz handle compression

- Combining tar with compression (.tar.gz, .tar.xz) is a standard practice in Linux

- gzip is fast and commonly used, while xz provides better compression ratios

- zip is cross-platform and ideal for sharing files across different operating systems

- Efficient file management is critical in real-world environments such as backups, logging, and data transfer


---

## Resources

- https://www.geeksforgeeks.org/linux-unix/tar-command-linux/
- https://www.geeksforgeeks.org/linux-unix/gzip-command-linux/
- https://www.geeksforgeeks.org/linux-unix/zip-command-linux/

---

## Output

- Commands Executed

`tar` → archive and extract files

`gzip` → compress files

`bzip2` → high compression

`xz` → maximum compression

`zip / unzip` → cross-platform compression
