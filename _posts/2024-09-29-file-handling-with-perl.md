---
layout: post
title: "Handling file with Perl"
date: 2024-09-29
category: perl
permalink: /perl/:title
---

File handling is a crucial aspect of programming, allowing you to read from and write to files, manipulate file data, and manage file operations. In this tutorial, we'll cover the basics of file handling in Perl, complete with examples and explanations.

### 1. Opening a File

In Perl, you can open a file using the `open` function. The basic syntax is:

```perl
open(FILEHANDLE, MODE, 'filename');
```

- **FILEHANDLE**: A user-defined name for the file.
- **MODE**: The mode in which to open the file (`<` for reading, `>` for writing, `>>` for appending).
- **'filename'**: The name of the file to be opened.

#### Example: Opening a File for Reading

```perl
open(my $fh, '<', 'input.txt') or die "Cannot open input.txt: $!";
```

### 2. Reading from a File

Once the file is opened in read mode, you can read its contents using several methods.

#### Read Line by Line

```perl
while (my $line = <$fh>) {
    print $line;
}
```

#### Read All at Once

```perl
my @lines = <$fh>;
print @lines;
```

### 3. Writing to a File

To write to a file, you need to open it in write mode. This will create a new file or overwrite an existing one.

#### Example: Writing to a File

```perl
open(my $fh, '>', 'output.txt') or die "Cannot open output.txt: $!";
print $fh "Hello, World!\n";
print $fh "This is a test.\n";
```

### 4. Appending to a File

If you want to add data to an existing file without overwriting it, use append mode (`>>`).

#### Example: Appending to a File

```perl
open(my $fh, '>>', 'output.txt') or die "Cannot open output.txt: $!";
print $fh "Appending a new line.\n";
```

### 5. Closing a File

After you're done with file operations, it's essential to close the file to free up system resources.

#### Example: Closing a File

```perl
close($fh) or die "Cannot close filehandle: $!";
```

### 6. Error Handling

Using `or die` after `open` is a common practice in Perl for error handling. You can also use `warn` for warnings.

#### Example: Error Handling

```perl
open(my $fh, '<', 'nonexistent.txt') or die "Error: $!";
```

### 7. Example: Reading and Writing

Here’s a complete example that demonstrates reading from one file and writing to another.

```perl
# Open input file for reading
open(my $in, '<', 'input.txt') or die "Cannot open input.txt: $!";

# Open output file for writing
open(my $out, '>', 'output.txt') or die "Cannot open output.txt: $!";

# Read from input and write to output
while (my $line = <$in>) {
    print $out $line;
}

# Close both files
close($in) or die "Cannot close input file: $!";
close($out) or die "Cannot close output file: $!";
```

### Conclusion

File handling in Perl is straightforward and powerful. By mastering these basic operations—opening, reading, writing, appending, and closing files—you can handle a wide range of data manipulation tasks. Experiment with these examples to get a solid grasp of file handling in your Perl scripts!
