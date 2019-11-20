# tree2dir
Facilitates accessing files in a tree structure from a single directory

USAGE: tree2dir <path_list>

OUTPUT: for each path in path list, generate a symbolic link to path in current directory
        the symbolic link name is identical to path, with "/" replaced with "_"
        
AUTHOR: Oren Civier 
       
EXAMPLE: 
tree2dir a/1.txt a/b/2.txt

will create two symbolic links in the current directory:

a_1.txt pointing to a/1.txt

a_b_2.txt pointing to a/b/2.txt         
       
