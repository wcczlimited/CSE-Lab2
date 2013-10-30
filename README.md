node(uint32_t inum) to extent_server
add get_inode(uint32_t inum) to extent_client
make get_inode(uint32_t inum) public

For dir inode, the inode content is blocknum -> inodeid + filename

Part 2 pass!
What should be noticed is that the hole('\0') in the file when the tester try to write beyond the end of an existing file.
The write and setattr of fys_client should consider about the comparion of the size want to set and the length of the file.
