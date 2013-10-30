Part 1 pass!
add #include<unistd.h> in rpc/rpc.h for it say the getid function are not declared.
For dir inode, the inode content is blocknum -> inodeid + filename

Part 2 pass!
What should be noticed is that the hole('\0') in the file when the tester try to write beyond the end of an existing file.
The write and setattr of fys_client should consider about the comparion of the size want to set and the length of the file.

Part 3 pass!
Use yfs->remove to delete file and should check a lot of things, if the file is a dir you will never delete it.
you should also change the ctime, atime, mtime when you create you file in the directory or delete something in it. However I wander if we should change the "vreate time" when we just delete something in a folder?
To change the time, I added a function in extent_client & extent_server & inode_manager.
