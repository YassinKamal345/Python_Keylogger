# Python_Keylogger

A basic Python keylogger that captures keystrokes and sends them to a listener on a lab
machine, built to understand how keystroke capture and exfiltration work under the hood.

> ⚠️ **Disclaimer — educational use only.** This project was built and tested in an isolated
> lab (a Windows VM + Kali Linux) that I own. Running it on any device or network without the
> owner's explicit written authorization is illegal. I am not responsible for any misuse.

## How it works

The script records keystrokes and streams them over the network to a listener you control.

## Setup

1. **Set the listener IP.** On your Kali machine, run `ifconfig` to find its IP address and
   set it in `keylogger.py`.
2. **Start the listener.** As root, listen on port 443:

   ```bash
   nc -nvlp 443
   ```

## Build an executable (optional)

With [PyInstaller](https://pyinstaller.org/) installed:

```bash
pyinstaller --onefile keylogger.py
```

The executable is created in the `dist/` folder.

## Usage

Run the script (or the built `.exe`). Keystrokes are captured and sent to your listener, where
you will see every key that is typed. Press `Esc` to quit.
