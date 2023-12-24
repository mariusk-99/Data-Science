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

> (You can access and write data in repositories on GitHub.com using SSH (Secure Shell Protocol). When you connect via SSH, you authenticate using a private key file on your local machine. For more information.

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

- Open Git Bash.

- Paste the text below, replacing the email used in the example with your GitHub email address.
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
Note: If you are using a legacy system that doesn't support the Ed25519 algorithm, use:
```
 ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
This creates a new SSH key, using the provided email as a label.

`> Generating public/private ALGORITHM key pair.`
When you're prompted to "Enter a file in which to save the key", you can press Enter to accept the default file location. Please note that if you created SSH keys previously, ssh-keygen may ask you to rewrite another key, in which case we recommend creating a custom-named SSH key. To do so, type the default file location and replace id_ALGORITHM with your custom key name.

`> Enter a file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]`
At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases."

`> Enter passphrase (empty for no passphrase): [Type a passphrase]`
`> Enter same passphrase again: [Type passphrase again]`

7. [Adding a new SSH key to your GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

- Copy the SSH public key to your clipboard.
Inside bash:
```
$ clip < ~/.ssh/id_rsa.pub
# Copies the contents of the _ id_rsa.pub _ file to your clipboard
```
- In the upper-right corner of any page, click your profile photo, then click Settings.
<img src="https://github.com/mk-hack-18/Data-Science/assets/68790682/be7964a2-7c64-443b-9da2-c7ea0f403408" alt="Alt text" width="200"/>

- In the "Access" section of the sidebar, click  SSH and GPG keys.

- Click New SSH key or Add SSH key.

- In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal laptop, you might call this key "Personal laptop".

- Select the type of key, either authentication or signing. For more information about commit signing, see "About commit signature verification."

- In the "Key" field, paste your public key.

- Click Add SSH key.

- If prompted, confirm access to your account on GitHub.

### Using Git 

> If you get into VIM by accident, here's how to get out.
> 1. Type commit message
> 2. Press `Esc`
> 3. To save the message and commit: `:wq`
