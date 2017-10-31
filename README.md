# EMFILE

`ulimit -a`
lsof meaning list open files command gives the list of open files. Assume your nodeJS program is having leak so to find out total number of file descriptors opened by your program :

`lsof | grep node | wc -l`

To find out the file descriptors for sockets, use:

`lsof -n -i -P | grep node`
