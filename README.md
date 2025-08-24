# 206 111 331

# Hey! I'm Filing Here

In this lab, I successfully implemented a mountable ext2 filesystem. It contains a root and lost+found directory, as well as a hello-world file and a symbolic link pointing to it.

## Building

make

### Now run the executable to create the file system image "cs111-base.img":
./ext2-create

## Running

### To mount the file system:
mkdir mnt
sudo mount -o loop cs111-base.img mnt

### To Dump the file system:
dumpe2fs cs111-base.img

### To check the ile system is created properly:
fsck.ext2 cs111-base.img


## Cleaning up

### To unmount the file system:
sudo umount mnt
rmdir mnt

### To clean the executable and other files
make clean
