<h1>Metasploitable 2 Setup</h1>

<h2>Description:</h2>

This project consists of setting up the environments to run Metasploitable 2. This will also go over creating the environment to do ethical hacking and penetration testing.

<h2>Environments Used:</h2>

- VirtualBox
- Kali Linux
- Linux

<h2>Walk-through:</h2>

<b>IMPORTANT</b> Create a NAT Network:
  - File -> Tools -> Network Manager -> NAT Networks -> Create
  - Name: Whatever you want
  - Keep everything else default
<br>

Create a Kali Linux virtual machine using my guide:
  - [Kali Linux Creation Guide](https://github.com/ntieu4328/Virtual-Box-Kali-Linux)
  - <b>IMPORTANT</b> Settings -> Network -> (Attached to: NAT Network) & (Name: Whatever name you put)
<br>

Create the Metasploitable 2 virtual machine:
  - Download the Metasploitable Virtual Machine Disk: [Metasploitable 2](https://sourceforge.net/projects/metasploitable/)
  - Make a new virtual machine with these settings:
    - Type: Linux
    - Version: Debian (64-bit)
    - Settings -> General -> Advanced -> (Shared Clipboard: Bidirectional) & (Drag'n'Drop: Bidirectional)
    - Settings -> Storage -> Mount Metasploitable.vmdk to Controller: SATA
![mount metasploitable](https://github.com/ntieu4328/Metasploitable-2-Setup-/assets/156137990/e722778d-c05a-4570-bf87-bfdb10e8cbd0)
    - <b>IMPORTANT</b> Settings -> Network -> (Attached to: NAT Network) & (Name: Whatever name you put)
   
*Creating the NAT Network allows the two virtual machines to communicate with each other.
<br>
<br>

After Metasploitable 2 finishes installing it should look like this:
![After download](https://github.com/ntieu4328/Metasploitable-2-Setup-/assets/156137990/e8d228e2-2b22-48b2-9239-d7db2153d533)
<br>
<br>

On Kali Linux install Nessus from Tenable:
  - Get access code that will be used later: [Access code website](https://www.tenable.com/products/nessus/nessus-essentials)
  - Download Nessus: [Nessus Download Website](https://www.tenable.com/downloads/nessus?loginAttempted=true)
![install nessus](https://github.com/ntieu4328/Metasploitable-2-Setup-/assets/156137990/84e1382e-c82b-488a-b7a8-758e448308fe)
  - Go into Kali Linux Terminal and install Nessus:
```bash
sudo dpkg -i (name of Nessus package)
```
  - At the end of the installation it will show you instructions on how to start Nessus:
![start nessus instructions](https://github.com/ntieu4328/Metasploitable-2-Setup-/assets/156137990/77c07ec2-1bfc-4f81-90e0-102b8bf46174)
  - Start Nessus Scanner:
```bash
/bin/systemctl start nessusd.service
```
  - Open a web browser. For me, I opened Firefox
  - go to https://kali:8834/
  - Nessus welcome page: Press continue

![nessus welcome page](https://github.com/ntieu4328/Metasploitable-2-Setup-/assets/156137990/947a694e-984d-42ac-9174-55f24720cca8)

  - Register for Nessus Essentials:

![Register for Nessus Essential](https://github.com/ntieu4328/Metasploitable-2-Setup-/assets/156137990/b7f0681e-8ee0-4ba8-ad5e-6671f0100018)
  
  - Skip
  - Input the activation code that you got
  - You will then be brought to the Nessus dashboard:
![nessus dashboard](https://github.com/ntieu4328/Metasploitable-2-Setup-/assets/156137990/51f6520c-635a-499d-8a79-8202d56fb65f)

<b>Setup is finished!!!</b>
