Step 1 - Make a GitHub Account
What is GitHub
Why is it important
How do developers use it
How we’ll be using it
Step 2 - Configure Git
INSTALL GIT: During the installation, you will be prompted to install XCode Command Line Tools. Agree and allow the installation to continue. You may also need to enter your computer password a couple of times.
Git has been installed but still needs to be configured with your personal account information. First, run the following to add your GitHub account name:
git config --global user.name <YOUR USERNAME>
Replace <YOUR USERNAME> with your actual account username. We also want to add the email account associated with your account. Run the command below to do so:
git config --global user.email <YOUR EMAIL>
You can verify these have been saved by running the same commands without providing your information:
git config --global user.name
git config --global user.email
This information is used when you send code from your local machine to GitHub.
Step 3 - Add Your SSH Key to GitHub

Generating a new SSH key
Open Terminal.
Paste the text below, substituting in your GitHub email address.
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
This creates a new ssh key, using the provided email as a label.
> Generating public/private rsa key pair.
When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
> Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
Aftering generating SSH key

Currently, if you were to send code to GitHub (commonly referred to as 'pushing'), you would be prompted to enter your credentials. To avoid having to enter this information every time, you can add an SSH key from your computer to GitHub as an alternative way to verify who you are. To see your SSH key, run the following command:
cat ~/.ssh/id_rsa.pub
Go to https://github.com, sign in, and navigate to SSH and GPG keys in Settings. Create a new SSH key and copy and paste your SSH key in.
For more information, check out GitHub's help article on adding SSH keys.
Step 4 - Download Atom Text Editor
