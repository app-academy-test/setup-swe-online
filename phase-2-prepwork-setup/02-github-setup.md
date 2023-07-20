# GitHub Setup

GitHub is one of the key collaborative tools that enable
teams of developers to build and maintain web applications. In this article,
we'll learn more about some of the key features of the tool, as well as set up
an account if you do not have one already.

By the end of this article you will be able to:

1. Sign up for a GitHub account and set up a basic user profile
2. Configure GitHub authentication using Git Credential Manager (GCM).
3. Describe how you can leverage your profile throughout the program in order to
   prepare for the job search
4. Identify the main elements of a repository that support collaboration

If you already have a GitHub account, you can skip ahead to "Setting up a GitHub
profile".

## Creating a GitHub account

In order to start collaborating on GitHub, you will need to create an account.

1. Navigate to the [GitHub Homepage] and click on the "Sign up" button in the
   top right-hand corner of the window.
1. Fill out all of the information on the form, and verify that you are a real
   person before clicking "Create account".

## Setting up a GitHub profile

You can think of your GitHub profile as your way of introducing yourself to the
developer world. In this section, we will get started by setting up some basic
elements, but you will revisit this profile as you gain experience, and will
ultimately polish it up before starting your job search.

1. Sign in to your account from the [GitHub Login Page].
1. Navigate to your profile by clicking on the avatar in the top right-hand
   corner of the window. Click on "Your profile".
1. Click on "Edit profile" to create your profile. Fill out the fields and click
   "Save".

Remember, this profile is what other developers will see when they look at your
work. Make sure it shows who you are, but in a professional manner. To see an
example and learn more, check out [About your profile] in GitHub's
documentation.

## Configuring Default Git Branch

You already installed Git while working on the Learning Challenges. Now, you
will complete some further configuration that will help you to start integrating
Git with GitHub.

First, enter the following command in your Mac or Windows terminal:

```shell
git config --global init.defaultBranch main
```

This specifies that your default Git branch should be the `main` branch.

## Configuring GitHub Authentication

Because GitHub allows you to share code with other developers, there needs to be
a way to authenticate to make sure that you are authorized to access or
contribute new code.

Thankfully, git handles this authentication flow automatically. But for GitHub,
there are several options for handling this authentication. These instructions
will walk you through setting up authentication through Git Credential Manager,
which is App Academy's preferred method.

__If you have _never_ configured GitHub authentication before, follow the
instructions below to set up Git Credential Manager. If you already have
authentication set up using a PAT or SSH key, you may continue using that
approach. You can reference this [SSH article] or [PAT article] for
troubleshooting your existing setup if needed.__

### Git Credential Manager

[Git Credential Manager] is the recommended secrets manager for GitHub authentication for Windows, Mac, and Linux.

#### Windows

If you followed the setup instructions for the Learning Challenges and installed Git for Windows, you will already have Git Credential Manager installed and ready to go.

_If you did not install Git Credential Manager through Git for Windows, follow the more detailed instructions in the [Git Credential Manager Setup] article._

_If you are already using WSL, run the following command in your terminal to tell git to
use Windows Credential Manager. If you are NOT using WSL, do not enter this
command._

```shell
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"
```

#### Mac

To install Git Credential Manager on Mac, you will use Homebrew. Open your Terminal, and run the following two commands:

```shell
brew tap microsoft/git

brew install --cask git-credential-manager-core
```

### Testing Git Credential Manager

Once Git Credential Manager is set up, you need to **restart your terminal**.

You can test to make sure GCM is working by attempting to clone or push to a
private repository. When you do this, you should get prompted by a new Window to
enter your GitHub credentials.

![GCM-browser-screenshot]

Choose "Browser/Device" and click "Sign in with your browser". You will then
need to enter your GitHub username and password. Upon providing your
credentials, your terminal should report it's success with the given operation.


## Keeping your garden green

When you go to your GitHub profile page, you will notice a section for the
amount of contributions in the last year. Underneath that, there is a grid of
green squares. The green squares represent all of your coding contributions to
GitHub. Employers use this information to help determine how active you are in
developing your coding abilities. As App Academy students, your job is to
populate this green garden as much as possible during your time here to build
your reputation as a developer!

To ensure that all of your activity shows up on your garden, click on
"Contribution Settings" just above the garden box. Make sure that "Private
Contributions" is checked to make sure that all of your work will be represented
on the chart.

![enable-private-repo-contributions]

## Collaborating on a Repository

In GitHub, you will create a _repository_ for every project you create. The
repository houses all of the code for the project, as well as other important
information such as the license and a _README_ file which describes the project
and shares important information on how to run, and contribute to the project.

![collaboration-workflow-1]

The project repository includes all of the tools needed for the collaborative
workflow described above. You start by cloning the project, or saving it to your
computer, you can then work on the project, and push your updated code back up
to the repository so others can work with it.

### Cloning a repository

When you _clone_ a project, you are making a copy of the code from a remote
server, and saving it locally. In this case, GitHub is the remote server, and
your computer is where you are storing the local copy, so you can work on the
code.

Follow these steps to clone the practice repository at this URL: [Practice
Cloning a Repository]. This will allow you to check whether your Git
configuration and GitHub authentication are working properly.

1. Visit the repository above, and click on the green "Code" button on the main
   page of the repository.
2. Click on the clipboard icon to copy the repository information.
3. From the command line, navigate to the directory where you plan to save your
   projects. For example: `cd aa-projects`
4. Next, run the following command, replacing the bracketed commands with your
   own information: `git clone <repository-info-from-your-clipboard>
   <local-repo-name>`
   - Replace `<repository-info-from-your-clipboard>` with the text you copied
     from GitHub. This will tell your computer what to copy from the remote
     server.
   - Replace `<local-repo-name>` with the name of a directory you want to create
     on your own computer to store the project files. This will create a folder
     in your current directory named "local-repo-name" containing the contents
     of the repository on the remote server.
   - Putting it all together, your final command should look like this: `git
     clone https://github.com/appacademy/github-cloning-practice.git
     cloning-practice`
5. At this point, you may see a prompt to enter you GitHub authentication
   information (username and password). Enter this information when
   prompted.
6. Finally, you can open your cloned project in VSCode to check that it exists,
   and start coding! Run `code <local-repo-name>`, replacing the bracketed
   command with the directory name you used in the step above. Open the
   `README.md` file, and you should see a success message. If you're not
   successful, take a step back and use Polya's framework to help you debug.

To learn more about cloning repositories from GitHub, you can read the [Cloning
a Repository Documentation].

> _Note: The instructions above assume that you have configured GitHub
> authentication using GitHub credential Manager through the browser. If you are
> using SSH, then make sure you are copying the SSH link from GitHub when you
> click the green "Code" button, and enter your SSH key when prompted. If you
> are using a PAT, enter your PAT when prompted._

Now that you have a GitHub account and know how to clone a remote repository,
you are ready to apply these skills in the next set of practices.

[GitHub Homepage]: https://github.com/
[GitHub Login Page]:
https://github.com/login
[Cloning a Repository Documentation]:
https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository
[enable-private-repo-contributions]:
https://appacademy-open-assets.s3-us-west-1.amazonaws.com/Modular-Curriculum/content/git/assets/enable-private-repo-contributions.gif
[About your profile]:
https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/about-your-profile
[Practice Cloning a Repository]:
https://github.com/appacademy/github-cloning-practice
[collaboration-workflow-1]:
https://appacademy-open-assets.s3-us-west-1.amazonaws.com/Module-Solo-Prep-Work/assets/Collaboration-workflow-1.png
[PAT]: https://github.com/settings/tokens
[SSH article]: https://hackmd.io/@AgDXdHgSSPKsJIhCxlaTuA/BJtNu88fF
[Git Credential Manager]: https://github.com/GitCredentialManager/git-credential-manager
[GCM assets documentation]: https://github.com/GitCredentialManager/git-credential-manager/releases/tag/v2.0.785
[Git Credential Manager Setup]: https://github.com/appacademy/practice-for-SETUP-swe-online-setup/blob/main/setup-resources/git-credential-manager.md
[PAT article]: https://github.com/appacademy/practice-for-SETUP-swe-online-setup/blob/main/setup-resources/setting-up-pat.md 
[GCM-browser-screenshot]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Modular-Curriculum/content/setup/07-gcm-browser.png
