# Update Phase 1 Installations

Now that you have WSL installed, it's time to check the software that you
installed during the Learning Challenges. You need to make sure that you can
access this software through WSL.

## Google Chrome

Check that Google Chrome is installed and working properly by finding it in
Windows Explorer, and double-click to open it.

## Visual Studio Code

Check that Visual Studio Code is installed and working properly by finding it
in Windows Explorer, and double-click to open it.

If either Google Chrome or Visual Studio Code are not installed or you cannot
access them, install them using the instructions in __Phase 1: Learning
Challenges Setup__. If you run into trouble, talk to an instructor for support.

## GitHub

_Using the Ubuntu terminal_, follow the instructions in the [GitHub Setup]
article to sign up for a GitHub account, and set up the Git Credential Manager
in Windows.

## Git

In your Ubuntu distribution in WSL 2, you should already already have Git
installed. However, you need to configure Git to use the Git Credential Manager
to connect GitHub with your installed Git.

_In the Ubuntu terminal, tell the installed Git to use Windows Credential Manager._

```shell
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"
```

Check that Git is configured properly and working through WSL by typing the
following commands _into the Ubuntu terminal_. You should see your real name and
the email address that you used to sign up for GitHub.

```shell
git config --global user.name    # your name returned
git config --global user.email   # your email address returned
```

__Make sure that the installed git is using the email that you used to sign up for
GitHub.__

If you do not see the correct output, configure Git within WSL using the following commands:

- Type `git config --global user.name "Your Name"`, replacing "Your Name" with your real name
  (i.e. "Jane Doe").
- Then type `git config --global user.email your@email.com`, replacing "your@email.com" with your GitHub email.

Congratulations! You've confirmed that you have Google Chrome and Visual Studio
Code are installed on your machine, created an account with GitHub, and configured Git
in the Ubuntu distribution in WSL 2.

[GitHub Setup]: https://github.com/appacademy/practice-for-SETUP-swe-online-setup/blob/main/phase-2-prepwork-setup/02-github-setup.md
