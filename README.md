# tree2dir
Facilitates accessing files in a tree structure from a single directory, especially when the files have identical names or when information on the location in the tree needs to be preserved.

USAGE: tree2dir <path_list>

OUTPUT:  

         for each path in path list, generates a symbolic link to path in current directory
         the symbolic link name is identical to path, with "/" replaced with "_"
        
AUTHOR:   Oren Civier 
       
EXAMPLES: 

1) tree2dir dira/1.txt dira/dirb/2.txt

        will create two symbolic links in the current directory:
        dira_1.txt pointing to dira/1.txt
        dira_dirb_2.txt pointing to dira/dirb/2.txt

2) tree2dir $(find /dira -name 1.txt)

        will create symbolic links in the current directory, to all the files named 1.txt in the tree below the directory /dira

3) tree2dir $(find /dira)

        will create symbolic links in the current directory, to all the files in the tree below /dira
