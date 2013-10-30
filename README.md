node(uint32_t inum) to extent_server
add get_inode(uint32_t inum) to extent_client
make get_inode(uint32_t inum) public

For dir inode, the inode content is blocknum -> inodeid + filename

