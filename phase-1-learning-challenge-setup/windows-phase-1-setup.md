# Environment Setup I - Windows

You'll need to install some basic development tools to complete these Learning
Challenges.  There are a few different ways to accomplish this, but please use
the method below.  It's good practice for how you'll normally install other
tools as a developer!

## Operating System

Much of the software you will be using is updated regularly and will eventually
stop working on older versions of operating systems.  You can save yourself many
tears by making sure that you keep your OS up-to-date:

1. Search for "system information" in the Windows Search Bar and open the System
   Information panel.  If you do not have a search bar or your OS Name is not
   some variation of "Windows 10" or "Windows 11", please see the note in the
   article in **Part 5: Analysis of My Computer** for information on updating
   older versions of Windows.
1. Search for "update" in the Windows Search Bar.
1. Click "Check for Updates".
1. In the window that opens, click the "Check for Updates" button.
1. Follow the prompts on the screen to install all available updates.

## Required Software for Learning Challenges

To complete the Learning Challenges, you will need to install __Google Chrome__, __Visual Studio Code__,  and __Git__.

Please follow the instructions and commands below exactly.  While you are
normally strongly encouraged to experiment with changing parts of the code
examples you learn, this can cause problems during environment setup, and later
on in the course itself.

### Google Chrome

Here at App Academy, our browser of choice is Google Chrome, due to its valuable
suite of developer tools. If you do not already have the Google Chrome browser
installed, you will first need to install it, and then set it as your default
browser.

1. Navigate to the [Google Chrome] website and look for the blue "Download
   Chrome" button.
2. Check to make sure the text underneath the button matches your operating
   system (Windows 10 or Windows 11).
   - If it matches, click on the "Download Chrome" button.
   - If it does not match, click on "Other Platforms" at the bottom of the page,
     and click on the link for your version of Windows.
3. Follow the instructions on the Chrome installer to complete the download and installation.
4. When prompted at the end of the installation, set Chrome as your default browser.

Check that Google Chrome is installed and working properly by finding it in
Windows Explorer, and double-click to open it.

### Visual Studio Code

Visual Studio Code (or VSCode) is a multi-language code editor that can handle
almost any programming language for any platform.

1. Navigate to the [Visual Studio Code] website and look for the blue "Download" button towards the middle of the page.
2. Check to make sure the text inside the button matches your operating system (Windows).
   - If it matches, click on the "Download" button.
   - If it does not match, click on "other platforms" underneath the button, and
     click on the blue "Windows" button.
3. Follow the instructions on the installer to complete the download and
   installation.

Check that Visual Studio Code is installed and working properly by finding it in
Windows Explorer, and double-click to open it.

### Git

Git is a Version Control System or VCS. It keeps track of a set of files over
time, and is used through the command line.

1. Navigate to the [Git For Windows] download page.
2. Click on the "Click here to download" hyperlink at the top of the page to
   download and install the latest version.
3. Follow the instructions on the installer to complete the download and
   installation. Use the configuration options below:
   - On the "Select Components" box, make sure "Windows Explorer Integration" is checked, and BOTH checkboxes are checked underneath ("Git Bash Here" and "Git GUI here")
     - ![Select components][Select components]
   - On the next screen, select "Use Visual Studio Code as Git’s default editor". Do not change the default branch name.
     - ![VScode default][VScode default]
   - Select "Let Git decide"
   - Select "Git from the command line and also from 3rd party software".
     - ![Git command line][Git command line]
   - Select "Use bundled OpenSSH".
   - Select "Use the OpenSSL library".
   - Select "Checkout Windows-style, commit Unix-style line endings".
   - Select "Use Windows’ default console window".
     - ![Window default][Window default]
   - Select "Default (fast-forward or merge)".
   - Select "Git Credential Manager".
   - Select "Enable file system caching"
     - ![Enable caching][Enable caching]
   - Then "Install"
     - **Note**: No need to select any of the boxes on the final installation page.
4. Open your terminal by right-clicking the icon of your git bash and click "Run as administrator"
    -  ![cmd admin][cmd admin]
5. You need to configure Git, so type `git config --global user.name "Your
   Name"`, replacing "Your Name" with your real name.
6. Then type `git config --global user.email
   your@email.com`, replacing "your@email.com" with your real email.

Check that Git is installed and configured properly by typing the following
commands into the terminal. You should see your real name and real email address
returned.

```shell
git config --global user.name    # your name returned

git config --global user.email   # your email address returned
```

> _Note: Every environment is different, so you may need to do some
> troubleshooting to get this setup to work. Reach out to the Prepwork Mentors
> on Discord if you run into any difficulties._

[Google Chrome]: https://www.google.com/chrome/
[Visual Studio Code]: https://code.visualstudio.com/
[Git For Windows]: https://git-scm.com/download/win
[Select components]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/select-components.png
[VScode default]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/vscode-git-default.png
[Git decide]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/git-decide.png
[Git command line]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/git-command-line.png
[Checkout window]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/checkout-window-style.png
[Window default]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/use-window-default.png
[Enable caching]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/enable-caching.png
[cmd admin]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/cmd-admin.png
