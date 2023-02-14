


No, the rename 's/ /_/g' * command will only rename files in the current directory, not in any subdirectories. If you want to rename files in all subdirectories as well, you can use the -r or --recursive option with the rename command.

Here's how the command would look with the -r option:

    rename -r 's/ /_/g' *

This will recursively search for all files and directories under the current directory and rename all files with spaces replaced by underscores.

Note that the rename command with the -r option will rename all files in the current directory and its subdirectories, so make sure to double-check your files and back them up before running the command.
