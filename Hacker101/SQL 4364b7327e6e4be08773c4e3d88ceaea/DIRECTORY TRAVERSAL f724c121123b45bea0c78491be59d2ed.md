# DIRECTORY TRAVERSAL

# Directory Trivial

It’s a path injection attack which occurs when path is constructed unsanitized user input by manupulating the construction of path you are able to walk up through control the files where files are read from and written to.

## Mechanism

As May you know there are many OSes, in which two directory representation . and ..

. is the Current directory and .. is the parent directory so when you by combining these we can practically walk anywhere on the file system.

- URL – http://bad-site.com/get_upload.php?file=../../../../etc/passwd

In this URL we going to see the password file by the path injection.

> **This could reveal code, personal file, database file
>