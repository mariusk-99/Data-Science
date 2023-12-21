# Data-Science
Step-by-step guide on my journey into Data Science

## MAKEMORE series - inspired by Andrej Karpathy

#### [Intro to language modeling](https://www.youtube.com/watch?v=PaCmpygFfXo)

## Git & GitHub Intro

1. [Install Git](https://git-scm.com/download/win)

2. When you've successfully started the installer, you should see the Git Setup wizard screen. Follow the Next and Finish prompts to complete the installation. The default options are pretty sensible for most users.

3. Open a Command Prompt (or Git Bash if during installation you elected not to use Git from the Windows Command Prompt).

4. Run the following commands to configure your Git username and email using the following commands, replacing Emma's name with your own. These details will be associated with any commits that you create:
```
$ git config --global user.name "John Doe"
$ git config --global user.email "johndoe@mail.com"
```
### SSH Authentication

> (You can access and write data in repositories on GitHub.com using SSH (Secure Shell Protocol). When you connect via SSH, you authenticate using a private key file on your local machine. For more information, see "About SSH."

> When you generate an SSH key, you can add a passphrase to further secure the key. Whenever you use the key, you must enter the passphrase. If your key has a passphrase and you don't want to enter the passphrase every time you use the key, you can add your key to the SSH agent. The SSH agent manages your SSH keys and remembers your passphrase.

5. [Check for existing SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys)

- Open Git Bash.

- Enter ls -al ~/.ssh to see if existing SSH keys are present.
```
$ ls -al ~/.ssh
```
#### Lists the files in your .ssh directory, if they exist
Check the directory listing to see if you already have a public SSH key. By default, the filenames of supported public keys for GitHub are one of the following.
_
id_rsa.pub
id_ecdsa.pub
id_ed25519.pub
_
Tip: If you receive an error that ~/.ssh doesn't exist, you do not have an existing SSH key pair in the default location. You can create a new SSH key pair in the next step.

6. [Generate a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

