# tree2dir
Facilitates accessing files in a tree structure from a single directory, especially when the files have identical names or when information on the location in the tree needs to be preserved. Useful in conjunction with rsync in order to only copy certain files from a server.

USAGE: tree2dir <path_list>

OUTPUT:  

         For each path in path list, generates a symbolic link to path in current directory.
         The symbolic link name is identical to path, with "/" replaced with "_".
         
         When using rsync subsequently: use the --copy-links option to instruct rsync to copy the files the symbolic links are
         pointing to rather than the symbolic links themselves.
        
AUTHOR:   Oren Civier 
       
EXAMPLES: 

1) tree2dir dira/1.txt dira/dirb/2.txt

        Will create two symbolic links in the current directory:
        dira_1.txt pointing to dira/1.txt
        dira_dirb_2.txt pointing to dira/dirb/2.txt

2) tree2dir $(find /dira -name 1.txt)

        Will create symbolic links in the current directory, to all the files named 1.txt in the tree below the directory /dira

3) tree2dir $(find /dira)

        Will create symbolic links in the current directory, to all the files in the tree below /dira
