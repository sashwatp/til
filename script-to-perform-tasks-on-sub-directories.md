There are multiple times when you want to perform some action on a list of files or sub-directories. Following command line and scripts can help you perform such tasks. 


#### Command line
You can directly run the following command in a bash shell.

```bash
for i in ./*/ ; do (<perform tasks>) ; done ;
```

#### bash script executable 
OR you can write a script that can be used in future as well.

```bash
#!/bin/bash

# Iterate through all the files and directories in the current directory
for item in ./*/
do
     
     # Check if the $item is a NOT directory. 
     #     1. Remove '!' if you want to do a positive test. 
     #     2. Replace '-d' with '-f' if you want to check for file. 
     if test ! -d "$item"
     then
         echo "$item is a directory"
         
         printf "%s is a directory. Present directory: %s" "$item" "$PWD"
         
         
         # PERFORM TASK or RUN A SCRIPT
         git config user.email
         
     fi  # End of if block
     
done   # End of for block
```

