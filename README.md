<h1> Active Directory Home Lab </h1>

<h2>Description</h2>
 In this Lab we're creating and Active Directory Home Lab Environment using Oracle Virtual Box. Configuring and running of this lab shows us how the active directory and windows networking works.
 we're using Windows Server 2022, Windows 10 iso  and creating virutal machines in the virtual box and configuring the networking and running lab setup.
<br />


<h2>Languages and Utilities</h2>

- <b>PowerShell </b> 
- <b> Oracle Virtual Box </b>

<h2>Environment</h2>

- <b> Windows Server 2022 </b>
- <b> Windows 10 </b> 

<h2>Lab walk-through:</h2>

- <b> After downloading of windows server 2022, windows 10 iso, and Oracle Virutal box</b>
- <b> Install the virtual box and windows server 2022</b>
- <b> While setting up of the server configure it with first adapter with nat and second one with internal so   that we can use the internal to connect back with the client</b>

![0-2](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/30a92db6-34a1-4166-9c56-db7f7dbd3f3b)
 Naming them as Internal     so we can differenciate while setting up in server 2022 adressing
  Changing the ipv4 as ip: 172.16.0.1
                       mask: 255.255.255.0
                       and for DNS server : 127.0.0.1
![0-1](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/d0c31db8-e40c-4659-bfeb-244c544f16a7)
 Naming this as Internet 
 
 - <b> Creating Domain </b>
![s1](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/30dc70f6-d413-4d8d-a68a-286f3a277a4e)

![s2](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/36b60056-461c-4f40-86ab-c3d14c0f597b)

![s3](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/e86b0b96-ae63-49da-98c0-237eaaa9ca18)

![s4](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/46eb37fa-0614-4af3-981a-323b521da325)
Activedirectory domain server and continue to install
and creating domain servers after installing with mydomain.com -> using password -> Install
Restarting the windows and login with mydomain/Administrator - password we created.

- <b>creating custom domain name </b>
![1 -1 ](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/d11db61b-5524-4696-983a-8b3b75f802cc)

selecting active directory users and computers

![1-2](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/ac2f412a-c9fe-4ee8-9a82-9c79f2f70511)

![1-3](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/d176cfc7-620e-4669-b720-5d3da974e92d)
and now logging in with our a-pganesh and with password 

- <b> Creating Remote Acess Server / Network Address Translation on Domain Controller

![s4](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/59fd7d36-7b06-4dba-9099-215d82a22ca8)
after installing open Tools - Routing and Remote Access

![s5](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/f626cf8e-cbde-4cd6-b726-2f26978f6753)

![s6](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/1f2d3e3b-374f-4885-997d-6e71c94c484e)
configure and enable - enabling the NAT - using the public interface to connect to the internet - finish

- <b> Creating the DHCP server </b>
going through add roles and feature - selecting server - select DHCP and Install
Toos - DHCP and setting up the scope.
DHCP - client can automatically connect with the server.

![s7](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/c926267e-4a53-494f-bc55-52f196e5ec22)
![s8](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/45755db7-fa1b-4036-8beb-7d03dc5e4265)
![s9](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/8a5b0912-9b34-4632-bb29-efc11a2d12e8)
after all setting up
Before attaching the client to our domain - we have to create users and their passwords so that we can use to login with client computer.
We are configuring the local server - Internet Explore Enhanced Security configuration to off - In lab environment.

![s10](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/dfd06145-5cd9-46b8-b8a6-f2d90dc1b0e2)

Creating users with first and last name 
![s11](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/7feb5f75-99e5-45df-b8ea-fb0dcedea3be)

opening the Windows Powershell ISE run as administrator.

![s12](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/1dae505c-007a-436f-9b3a-a6bc52059228)

and using powershell scripting 

![s13](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/d76deabd-86ca-4b5c-950c-739579c4c3cb)

Set-ExecutionPolicy - Unrestricted to not get distrubed while executing
going to directory where we saved the names
C:\users\a-pganesh\desktop\AD_PS-master and click play

after execution of the script it creates the user accounts with passwords where it uses the names list which we provided in previous steps.
![s14](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/6ca995df-d0a8-4861-8732-be605fe61fc8)

- <b> Opening up the client system </b>
and using our user credentials we can login into the systesm

![s15](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/3cb4be23-04ff-4cb6-94f1-b3f49b2fe913)

Checking the system by cmd -> command - ipconfig

![s16](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/42dcd145-9420-4438-993e-a8dac567f705)

Pinging the internet and pinging our domain to check does it really connected or not

![s17](https://github.com/GiridharNaagar/Active-Directory-Home-Lab-/assets/114043681/6bc1b731-28b1-485e-8d53-fdf7741906dd)







 

