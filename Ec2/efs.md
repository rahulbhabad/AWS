## EFS - Elastic File System

### **Steps:**

1. **Create Security Group**
   - Create a security group with the name `efs-sg`.
   - Add the following inbound rule:
     - **Port:** 2049
     - **Protocol:** NFS

2. **Launch Instances**
   - Launch two instances in different availability zones (AZs).
     
   ![image](https://github.com/user-attachments/assets/1ae79377-def5-4fbd-8b38-57fe9de265ee)

   - Login to both instances.
   - Create a directory named `efs`:
     ```bash
     mkdir efs
     ```
     ![image](https://github.com/user-attachments/assets/3bee2e58-178c-4807-81ba-f6dd1d9218de)
     

   - Install the Amazon EFS utilities:
     ```bash
     yum install amazon-efs-utils -y
     ```

     ![image](https://github.com/user-attachments/assets/2accea4e-1985-412a-8a40-619e0d1d5355)


3. **Setup EFS**
   - Navigate to the EFS service in AWS Management Console.
   - Create a new file system.
   - Change the security group to `efs-sg`.
   ![image](https://github.com/user-attachments/assets/7eaec9e4-8d0e-44a5-95d7-864a6531bb9f)

   ![image](https://github.com/user-attachments/assets/046d035f-1d79-4721-82ba-d61e6c2bdb0b)


   - Click on **Attach File System**.
   
   ![image](https://github.com/user-attachments/assets/bce12083-be58-43fa-9a0e-a98b98d36b3e)

   - Two mounting options will be provided:
     1. Mount via DNS
     2. Mount via IP
   - Copy the **Mount via DNS** commands.
     
   ![image](https://github.com/user-attachments/assets/ee9a9621-24b9-4f98-8eed-299e22db56f4)

4. **Mount EFS on Instances**
   - Paste the commands into both virtual machines to mount the file system.
   - Navigate to the `efs` directory:
     ```bash
     cd efs
     ```
   - Create demo files on one instance:
     ```bash
     touch demo-file-1 demo-file-2
     ```
   - Check the second instance; the same files will be visible there as well.
