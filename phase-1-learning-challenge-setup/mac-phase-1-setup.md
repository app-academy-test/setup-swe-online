# Environment Setup I - Mac

You'll need to install some basic development tools to complete these Learning
Challenges.  There are a few different ways to accomplish this, but please use
the method below.  It's good practice for how you'll normally install other
tools as a developer!

## Operating System

Much of the software you will be using is updated regularly and will eventually
stop working on older versions of operating systems.  You can save yourself many
tears by making sure that you keep your OS up-to-date:

1. Click the Apple Menu in the upper left
1. Select "About this Mac"
1. Click the "Software Update" Button
1. Follow the instructions in the "Software Upgrade" window and complete all
   available updates and/or upgrades.

## Required Software for Learning Challenges

To complete the Learning Challenges, you will need to install __Google Chrome__,
__Visual Studio Code__,  __Homebrew__ and __Git__.

Please follow the instructions and commands below exactly.  While you are
normally strongly encouraged to experiment changing parts of the code examples
you learn, this can cause problems during environment setup, and later on in the course itself.

### Google Chrome

Here at App Academy, our browser of choice is Google Chrome, due to its valuable
suite of developer tools. If you do not already have the Google Chrome browser
installed, you will first need to install it, and then set it as your default
browser.

1. Navigate to the [Google Chrome] website and look for the blue "Download
   Chrome" button.
1. Check to make sure the text underneath the button matches your operating
   system (Mac).
- If it matches, click on the "Download Chrome" button.
- If it does not match, click on "Other Platforms" at the bottom of the page,
  and click on the link for your Mac version.
1. Follow the instructions on the Chrome installer to complete the download and installation.
1. When prompted at the end of installation, set Chrome as your default browser.

Check that Google Chrome is installed and working properly by finding it in your
Applications directory, and double-clicking to open it.

### Visual Studio Code

Visual Studio Code (or VSCode) is a multi-language code editor that can handle
almost any programming language for any platform.

1. Navigate to the [Visual Studio Code] website and look for the blue "Download"
   button towards the middle of the page.
1. Check to make sure the text inside the button matches your operating system
   (Mac).
- If it matches, click on the "Download" button.
- If it does not match, click on "other platforms" underneath the button, and
  click on the blue "Mac" button.
1. Follow the instructions on the installer to complete the download and
   installation.
1. To open the VS Code editor, open the Command Palette (`Cmd+Shift+P`) and type
   "shell command".
1. Click on `Shell Command: Install 'code' command in PATH command` - this will
   allow you to use the `code` command from the Terminal to open projects in VS
   Code.

Check that Visual Studio Code is installed and working properly by finding it in
your Applications directory, and double-clicking to open it.

### Homebrew

Homebrew is a piece of software for macOS that lets you install extra unix
software on your Mac.

1. Select "Terminal" to start Terminal.
1. Open Safari and navigate to https://brew.sh.
1. Copy the command to be pasted into the Terminal by clicking on the clipboard
   icon.
1. Paste the command into Terminal and press Enter.
1. Press Enter when prompted.
1. Enter your password when prompted. _Wait...this could take a long time!_

You can check that Homebrew was installed correctly by typing  `brew doctor`
into the Terminal. If it reads that "Your system is ready to brew.", then you
are done. If not, address the errors that you see. _If there are any warnings,
you can ignore them for now and continue._

### Git

Git is a Version Control System, or VCS. It keeps track of a set of files over
time, and is used through the command line.

1. Return to your Terminal.
1. Type `brew install git`.
1. You need to configure Git, so type `git config --global user.name "Your
   Name"`, replacing "Your Name" with your real name.
1. Then type `git config --global user.email
   your@email.com`, replacing "your@email.com" with your real email.
1. Finally, install xcode command line tools by typing `xcode-select --install`.

Check that Git is installed and configured properly by typing the following
commands into the Terminal. You should see your real name and real email address
returned.

```shell
git config --global user.name    # your name returned

git config --global user.email   # your email address returned
```

> _Note: Every environment is different, so you may need to do some
> trouble-shooting to get this setup to work. Reach out to the Prepwork Mentors
> on Discord if you run into any difficulties._

Resources:

- [Visual Studio Code]
- [Google Chrome]
- [Homebrew]
- [Git]

[Visual Studio Code]: https://code.visualstudio.com/
[Google Chrome]: https://www.google.com/chrome/
[Homebrew]: https://brew.sh/
[Git]: https://git-scm.com/download/mac
