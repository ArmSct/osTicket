
![68747470733a2f2f692e696d6775722e636f6d2f7278463149686a2e706e67](https://github.com/user-attachments/assets/7fa9f6dd-dbb0-45db-b07b-2031041045fb)

# osTicket Setup on Azure Windows VM
In this project, we create a Windows 10 Virtual Machine in Microsoft Azure and install the open-source support ticket system, osTicket v1.15.8. This includes setting up IIS, PHP, MySQL, and configuring required dependencies to get osTicket running locally.

## Technologies Utilized
- Microsoft Azure (Virtual Machine deployment)
- Windows 10 (Guest OS)
- Remote Desktop Protocol (RDP) (VM access)
- Internet Information Services (IIS) (Web server)
- PHP 7.3.8
- MySQL 5.5.62
- osTicket v1.15.8
- HeidiSQL (MySQL client)

## Actions and Observations

### 1. VM Deployment and Access
 Create an Azure Windows 10 VM.
![BicXUQ75Pn](https://github.com/user-attachments/assets/57cbd880-7393-4576-974d-5de02f85b706)

Login to the Widows 10 VM using RDP and download the osTicket-Installation-Files.zip.
![mstsc_ZpBRv50EQ2](https://github.com/user-attachments/assets/4530a63a-6489-4d3a-a98c-7e2bfe70af44)


### 2. Install/Enable IIS in Windows with CGI and install PHP manager
![mstsc_0BhqVQInyI](https://github.com/user-attachments/assets/c14ed0e6-e15d-45b7-87b8-c0d125ac68cb)
![mstsc_qelfIqUhOH](https://github.com/user-attachments/assets/1e03f384-c8dd-4a0d-9741-0b960036388b)

### 3. Install Required Components
Install Visual C++ Redistributable: (VC_redist.x86.exe.) and MySQL 5.5.62:(mysql-5.5.62-win32.msi.).

![mstsc_Gcyg8IR516](https://github.com/user-attachments/assets/cbd33a89-4ef6-4011-8be2-3c49e0a8d85f)
![mstsc_TICjEeQyAi](https://github.com/user-attachments/assets/d42b5d51-e002-4e72-b87c-adf4c5de0929)

### 4. Configure IIS for osTicket
Open IIS Manager as Administrator, register PHP at C:\PHP\php-cgi.exe using PHP Manager, then reload IIS to apply changes.
![mstsc_zReCGRQkGD](https://github.com/user-attachments/assets/b75ddb57-7927-45ae-94ea-df582333329c)

### 5. Install osTicket
Unzip osTicket-v1.15.8.zip and copy the upload folder to: C:\inetpub\wwwroot and rename upload to osTicket: C:\inetpub\wwwroot\osTicket
![mstsc_irFm8AsUHS](https://github.com/user-attachments/assets/d68daf39-9a7a-48bb-a5f2-5ce40a99a402)

### 6. Reload IIS, then go to Sites, select Default Web Site, choose osTicket, and click "Browse :80" on the right panel to launch the site.   
![mstsc_dcGTjyCnrL](https://github.com/user-attachments/assets/ee84ce95-268e-411a-84f5-9d40562f56a3)

### 7. Enable Extensions in IIS
Enable some extensions that are not are not enabled.
![mstsc_NYk3Q1JEPA](https://github.com/user-attachments/assets/3f182974-3382-48af-88b5-1bda9ee17a28)
![mstsc_HOiXPMAzlA](https://github.com/user-attachments/assets/ba3d2e5b-99e2-4618-a4a3-cb5b92448f03)
![mstsc_2XnqNe8izS](https://github.com/user-attachments/assets/8f13605c-5cab-4267-bd61-4434991d77e5)

