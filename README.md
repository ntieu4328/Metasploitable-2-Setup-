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

On Kali Linux install Nessu from tenable
