# PHP File Handling Bug: Ignoring fclose() Return Value

This repository demonstrates a common, yet often overlooked, error in PHP file handling: ignoring the return value of the `fclose()` function.  While `fclose()` usually succeeds, it can fail (e.g., due to I/O errors), and ignoring the return value means these failures go undetected, potentially leading to resource leaks and data corruption.

The `bug.php` file shows the problematic code. The `bugSolution.php` provides the corrected code, which explicitly checks the return value of `fclose()` and handles any potential errors.