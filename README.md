# Remove USB Partition

1. Identify your pen drive using the command `lsblk`.

![image](https://github.com/ShubhamKumar89/usb-partition/assets/97805339/aff7b5ac-a637-40e0-8616-e29128d8ae6b)

2. Start `fdisk` for the pen drive with:

```bash
sudo fdisk /dev/sdb
```
Now you will enter a command prompt that looks like `Command (m for help):`

3. Print the current partition layout using the `p` command.

4. Delete the partition using the `d` command. It will ask for the partition number, you can enter `1` to delete the first partition. Repeat this step until all partitions are deleted. 

> **Note**:
> If you only have one partition, it will be deleted automatically without asking for the partition number.

5. After deleting all partitions, write the changes to the disk with the `w` command.

![image](https://github.com/ShubhamKumar89/usb-partition/assets/97805339/fb9a508c-9085-4071-a367-38f01acfd7d0)

You should now have a blank pen drive. You can verify this by running `lsblk` again.

![image](https://github.com/ShubhamKumar89/usb-partition/assets/97805339/57b96abb-0b47-4228-a1ea-4a187807a649)

