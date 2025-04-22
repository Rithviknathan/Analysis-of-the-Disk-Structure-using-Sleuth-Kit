Analysis-of-the-Disk-Structure-using-Sleuth-Kit

AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

DESIGN STEPS:
Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:
```
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```
OUTPUT:
![image](https://github.com/user-attachments/assets/5068592b-2040-4489-a36b-8a3858a59638)


Create Disk
![image-1](https://github.com/user-attachments/assets/60e230b6-58e7-42d6-bd40-a7dca1728371)


mmls
```
mmls disk.dd
```
fls
```
fls -f fat -o 0 disk.dd
```
![image-2](https://github.com/user-attachments/assets/ac3f0e98-0a69-430f-98ae-1e49f23371d3)

![image-3](https://github.com/user-attachments/assets/f5f43c31-e547-4bff-8aa9-37ba76137a44)


![image-4](https://github.com/user-attachments/assets/5dc5a1ed-d685-41c8-9be9-4211d0f6548f)





RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
