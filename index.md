## Existing file-system partition without destroying data

1)	Take the backup of existing data for safer side

![1.png](1.png?raw=true "Title")

2)	Check the target partition and mount point 

![2.png](2.png?raw=true "Title")

3) Take the note of the existing partition using parted. Here we are working with device /dev/sdb but  not partition name /dev/sdb1

![3.png](3.png?raw=true "Title")

4)	Unmount the target partition

![4.png](4.png?raw=true "Title")

5)	Delete the existing partition with parted by specifying the partition number listed in step 3.

![5.png](5.png?raw=true "Title")

6)	Verify from fdisk command

![6.png](6.png?raw=true "Title")

7)	Recreate the partition with the larger size. Specify the same starting sector as the previous partition, and use 100% to fill the whole disk. And run the below commands and verify the data.

![7.png](7.png?raw=true "Title")
