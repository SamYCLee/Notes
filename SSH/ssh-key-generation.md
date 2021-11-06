# SSH Key Generation

## OS

### Windows

#### OpenSSH

To generate ssh key using OpenSSH Client:

1. Check if OpenSSH Client is installed
    - By checking Windows' Setting > Apps & Feature > Optional features
    - By typing `ssh-keygen --help` in Windows Command Prompt to check if `ssh-keygen` is installed
2. Open Windows CMD
3. Type `ssh-keygen -t ed25519 -C "email"` and it will generate the public and private key pair in algorithm ED25519 and comment with your email
4. Choose the place to store and if passphrase is needed, the default storing location will be `C:\Users\User\.ssh`
