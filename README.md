# Python_Keylogger
A basic Python keylogger that sends captured keystrokes to a listener on a lab machine, built to understand how keystroke capture and exfiltration work.

> ⚠️ **Disclaimer — educational use only.** This project was built and tested in an isolated lab (Windows VM + Kali Linux) that I own. Running it on any device or network without explicit written authorization is illegal. I am not responsible for any misuse.

# Change the ip address on the file
Before converting it you should first locate your ip address on your kali linux machine and change it in the code
To do so open the terminal then type " ifconfig" and you find your machine's ip address
Then as root start listening to the port 443 by entering this command "nc -nvlp 443"


# Convert to .exe
To convert the keylogger into a .exe file you need to have "pyinstaller" installed in your python scripts
To do so open you CMD and type "pyinstaller --onefile .\keylogger.py"
This will create a folder called dist, inside you will find the keylogger.exe file so you can execute it

# Use
Open the .exe file then start typing on your browser for exameple, you will see on the pop up everything you're typing
When you're done press "Esc" to quit the program
On your kali linux machine you should see everything word that was typed
