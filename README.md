# ssh key for GPU renting
Step by step guide to obtain ssh key for renting GPU

## Create a Public SSH using PowerShell
### 1- Open Windows PowerShell
In Windows Start Menu, Find **Windows PowerShell**, Right click on it and click on Run as Administrator

### 2- In the terminal run:
```bash
ssh-keygen -t rsa -b 4096
```
* You'll see:
```
Generating public/private rsa key pair.
Enter file in which to save the key (C:\Users\YourUsername\.ssh\id_rsa):
```
* Press `Enter` to accept the default location (C:\Users\YourUsername\.ssh\id_rsa). This ensures the private key is named id_rsa and the public key is id_rsa.pub.

### 3- Set a Passphrase (Optional but Recommended)
* Output will look like:
```
Your identification has been saved in C:\Users\YourUsername\.ssh\id_rsa.
Your public key has been saved in C:\Users\YourUsername\.ssh\id_rsa.pub.
The key fingerprint is: SHA256:...
```

### 4- Navigate to `.ssh` directory
```
cd $env:USERPROFILE\.ssh
```

### 5- Copy the `id_rsa.pub` file content in clipboard
```
Get-Content id_rsa.pub | Set-Clipboard
```
* Your public key is now copied into your `clipboard`
