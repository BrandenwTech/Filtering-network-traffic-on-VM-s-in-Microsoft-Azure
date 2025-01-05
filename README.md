# Filtering-network-traffic-on-VMs-in-Microsoft-Azure
In this Project I guide you though how to make 2 virtual machines in the cloud ( Microsoft Azure ) and detect network traffic using Powershell and Wireshark
----------------------------------------------------------
( Technologies / OS ) used
1. Microsoft Azure
2. Powershell
3. Wireshark
4. Remote Desktop
5. Windows 10
-----------------------------------------------------------

INSTALLATION STEPS

Step 1 ; Create a free Microsoft Azure account using your email address of choice
![image](https://github.com/user-attachments/assets/bf4b79d6-a09a-4595-882b-9aae1a35ce7f)

-----------------------------------------------------------
Step 2 ; Go to Microsoft Azure home page while signed in and create a Resource group

Note: if your azure services does not display resource groups then use the Search bar located at the top of the screen
![image](https://github.com/user-attachments/assets/8730d11c-4f74-43cd-a268-3fd94a5099c7)

-----------------------------------------------------------
Use the create button once clicking on resource groups
![image](https://github.com/user-attachments/assets/f2aecae6-c0c7-49ed-b2d0-a00dfc926ca9)


-----------------------------------------------------------
Name Resource Group
![image](https://github.com/user-attachments/assets/49f5a30f-a1c1-40ee-9e2d-915c628ae5b7)


-----------------------------------------------------------
Click review & create and then Create once more at the bottom left
![image](https://github.com/user-attachments/assets/9bbe2a31-f40a-4869-b956-dae6c8aa50b6)


-----------------------------------------------------------
Open the resource group you created and select create inside

note: If you cant relocate your group then use the search at the top of the screen
![image](https://github.com/user-attachments/assets/31e8e230-db43-4684-ad39-34f370943a9a)

-----------------------------------------------------------
Search for VM in your marketplace searchbar and create one
![image](https://github.com/user-attachments/assets/c3d95645-452d-4697-b704-c2e9dc73d2f3)

-----------------------------------------------------------

Verify that your VM is in the resource group that you named

Name your Virtual machine
![image](https://github.com/user-attachments/assets/a3528b2b-ab78-4cba-9fef-69079821dbf6)

-----------------------------------------------------------

Select a Windows 10 image and for size select D2s_v3 - 2cpu's 8 gig memory

note: select see all sizes if you cant locate this size
![image](https://github.com/user-attachments/assets/f085feb8-4aad-4ac4-bc51-7c90c12a8bba)

-----------------------------------------------------------

Create a text document containing a username and password for 2 virtual machines
![image](https://github.com/user-attachments/assets/f95c619b-ee65-4f0c-858a-f40c8a6a2544)

-----------------------------------------------------------

Enter you first username and password into the administrator account section of the page
![image](https://github.com/user-attachments/assets/19c0f7b7-3b1b-458b-80f0-da3b0a5c3663)

-----------------------------------------------------------

Check your licensing box at the bottom of the page
![image](https://github.com/user-attachments/assets/38de9c21-0191-4771-8ccb-e49857574c4c)

-----------------------------------------------------------

Scroll to the top and select the networking tab
![image](https://github.com/user-attachments/assets/0c82c581-7e28-4a8b-af3e-45861aa2b9de)

-----------------------------------------------------------

Create a new virtual network and give it a name
![image](https://github.com/user-attachments/assets/8807bddb-4de1-4ab8-b47a-25b32dc50d3a)

-----------------------------------------------------------

Select view & create and once your validation passes select create once more at the bottom of the screen
![image](https://github.com/user-attachments/assets/43916d0e-fc50-443d-9faf-93b8664599a7)

-----------------------------------------------------------

Once your deployment succeeds go to your resource group
![image](https://github.com/user-attachments/assets/7cff9c38-1015-437e-9fb9-26f60dba93f8)

-----------------------------------------------------------

In your resource group create another VM using the second username and password that you typed in your note

verify that your resouce group is correct

verify that your network is the same in the networking tab
![image](https://github.com/user-attachments/assets/917eba98-e733-4768-9f6d-cc2c9c51f371)

-----------------------------------------------------------

Click on your first virtual machine and locate the Public ip address on the right side of the screen

save this ip address into your note
![image](https://github.com/user-attachments/assets/a1a053a6-e516-4f54-8673-f8ed646020c3)

-----------------------------------------------------------

Open Remote desktop connection on your pc and enter the ip address from machine 1

Enter your username and password to login to the VM
![image](https://github.com/user-attachments/assets/0afe2e5d-d3a8-4453-a894-8b6d29eae9f8)

-----------------------------------------------------------

Select Yes
![image](https://github.com/user-attachments/assets/4f7b92e7-9ae2-41a7-a744-a85905c554a4)

-----------------------------------------------------------

Toggle off all once your windows 10 VM loads
![image](https://github.com/user-attachments/assets/58285d75-2848-4cbd-ae5f-6e7fed9edb8d)

-----------------------------------------------------------

Select Yes and X on the tab in the middle of the screen
![image](https://github.com/user-attachments/assets/60638310-a305-4581-8b41-ade7763bb9a2)

-----------------------------------------------------------

Open microsoft edge and seach for wireshark

download windows x64 installer

open your .exe file

note ; go to file explorer then downloads if you cant find your .exe
![image](https://github.com/user-attachments/assets/a96ab778-81d8-451b-909e-bb0dae709d11)

-----------------------------------------------------------

Continue clicking the blue button until wireshark installs
![image](https://github.com/user-attachments/assets/638aea5c-1458-4f6f-9007-e93912ca20fb)

-----------------------------------------------------------

Open wireshark and start capturing packets by clicking the blue fin under file at the top of the screen
![image](https://github.com/user-attachments/assets/9deae51e-7dc7-4b0c-bb98-c8e6cda6202d)

-----------------------------------------------------------

Use the search and type icmp and enter to start filtering only for ping traffic

After this log into your second VM and access your windows 10 home page
![image](https://github.com/user-attachments/assets/703fa28a-b931-44ba-ac1b-4a2b4cf06105)

-----------------------------------------------------------

Open windows Powershell on your second VM and ping the IP address of your 1st VM

Observe wireshark on your first virtual machine and you should be able to see the ping from VM 2
![image](https://github.com/user-attachments/assets/574713f1-eab7-4d2d-a210-1cebf4f5e2a7)

-----------------------------------------------------------



















