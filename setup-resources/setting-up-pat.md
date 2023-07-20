# Setting Up a Personal Access Token (Optional)

App Academy's recommended approach to GitHub authentication is through Git
Credential Manager, and using your GitHub credentials through the browser. This
article describes an alternate approach: Using a Personal Access Token instead
of using your GitHub username and password. One benefit to this approach is that
you can set up multiple tokens for the same account (for example, you could set
up different tokens for each of your devices).

Once Git Credential Manager is setup, you need to **restart your terminal**.

Once restarted, you want to do two things. Generate a token from Github, and use
that as your authentication for a privileged command.

1. To get a new token, navigate to [Personal access tokens][PAT] in Github
   settings. You can navigate there yourself by going to `Settings > Developer
   Settings > Personal Access Tokens`.

2. Once here, click **Generate new token**.

3. Give your token a descriptive name. You can name it for the device you will
   use the token from. This way, each computer can have their own unique token
   and if you ever need to, you can revoke a token. You also want to use this
   menu to set when your token expires and give it the allowed permissions. For
   your purposes, you want to at least have all the repo permissions.

> Once you have your token ready to generate, you should try running a
> privileged command in git so you get a password prompt. Once you click
> **Generate token** at the bottom of the *new token form* you will only be able
> to see the token once.

4. Now that you have your token, you can use it when Git prompts you for a
   password. Choose "Token", and enter your new PAT in the input box as shown
   below.

![PAT-prompt]

[PAT]: https://github.com/settings/tokens
[PAT-prompt]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Modular-Curriculum/content/setup/08-gcm-pat.png
