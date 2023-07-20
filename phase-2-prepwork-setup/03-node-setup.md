# Node.js Setup

Up until now, you've been running your JavaScript in the browser's console.
However, sometimes being in the browser environment just isn't necessary. An
alternative to run and test code locally is using [Node.js][about node].

So what is Node exactly? Node.js is a very powerful runtime environment built
on Google Chrome's JavaScript V8 Engine. It is used to develop I/O intensive
applications like video streaming sites, robots, and other general purpose
applications. For your purposes the most advantageous feature of Node is that it
provides a way for you to run JavaScript outside of the browser.

In this reading, you will:

- Learn about how Node.js came to be
- Install Node.js and use it to run JavaScript in the terminal

## Same specification, different implementation

Since JavaScript is a single programming language, you may be wondering why
there are **any** differences between Node.js and browsers in the first place.
If they are in fact different, why wouldn't you classify them as different
programming languages? The answer is complicated, but the key idea is this: even
if you just consider browser environments, different browsers themselves can
differ wildly because JavaScript is a **specification**.

During the rise of the World Wide Web in the 90s, companies competed for
dominance. As Netscape's "original" JavaScript language rose to prominence
along with their browser, other browser companies needed to also support
JavaScript to keep their users happy. Imagine if you could only visit
pages as they were intended if you used a certain browser. That would be a
terribly inefficient way to use the Internet. As companies "copied" Netscape's
original implementation of JavaScript, they sometimes took creative liberties
in adding their own features.

In order to ensure a certain level of compatibility across browsers, the
European Computer Manufacturers Association (ECMA) defined specifications to
standardize the JavaScript language. This specification is known as
**ECMAScript** or **ES** for short. This allows competing browsers like
Google Chrome, Mozilla Firefox, and Apple Safari to have a healthy level of
competition that doesn't compromise the customer experience. So now you know
that when people use the term "JavaScript" they are really referring to the
core standards set by ECMAScript, although exact implementation details may
differ from browser to browser.

The Node.js runtime was released in 2009 when there was a growing need to
execute JavaScript in a portable environment, without any browser.

> **Did you know?** Node.js is built on top of the same JavaScript engine as
> Google Chrome (V8). Neat.

There are many differences between Node.js and browser environments, but for
now you don't have to worry about them.

## Installing Node.js

Follow the instructions below for installing Node.js for your Mac or Windows environment:

### Mac Installation: Node Version Manager and Node.js

__Node Version Manager (`nvm`) for Mac__

Often as a developer, you will need to juggle multiple projects on our computer,
each running a different version of Node.JS. Because of this, just installing a
new version from the Node.js website would be difficult and error-prone.

Luckily, there's a piece of open source software that can help called Node
Version Manager, or `nvm`.

To install nvm, check out the `nvm` github page here:

[nvm Github Page]

Copy the curl command listed in the README, and paste it in your Mac or Windows
terminal.  It should look something like this, although the version number in
the URL might vary:

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
```

Press enter, and you'll see a lot of information logged:

```shell
# ... a lot of information logged

=> Appending nvm source string to /home/your-user/.bashrc
=> Appending bash_completion source string to /home/your-user/.bashrc
=> Close and reopen your terminal to start using nvm or run the following to use it now:

# ... this is the important part below
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```

The lines to pay attention to are the last three. These are the shell commands
necessary to initialize `nvm`.  These commands need to be added into your _shell startup file_.

The general rule on this is:

If your shell is `zsh`, use `~/.zshrc`
If your shell is `bash`, use `~/.bashrc`

> You can determine which shell you have by typing `echo $SHELL` at the command
> line.

You'll notice, in the example above, the nvm installer automatically added the
lines to the `~/.bashrc` even though the example runs zsh.  You need to verify
that the lines were correctly added to your startup file. Don't trust the
installer to always do the right thing in this case. Everyone's system is
different.

To verify it, open up your startup file in vscode with the `code` command. Use
the appropriate startup filename depending on which shell you have (`~/.zshrc`
or `~/.bashrc`).

```shell
code ~/.zshrc   # if you run zsh

code ~/.bashrc   # if you run bash
```

If you do not see the `nvm` startup lines in your file already, add them in
there.

There are two ways to run your startup file. You can run it live in your current
shell by typing the `source` command and following it with your startup file, or
an even easier option is to just close your terminal window and open it back up.

Once you have done these steps, run `nvm` by itself at the command prompt. You
should see the help messages from nvm. If this doesn't work, double check your
shell startup files.

__Installing Node.JS for Mac__

Now that you have `nvm` installed and ready to go, you can use it to install a
particular version of Node.JS.

Currently in this course, you will use version 16.

Enter the following command in your Mac terminal:

```shell
nvm install 16
```

You should see something like this:

```shell
Downloading and installing node v16.14.0...
Downloading https://nodejs.org/dist/v16.14.0/node-v16.14.0-darwin-arm64.tar.xz...
######################################################################### 100.0%
Computing checksum with shasum -a 256
Checksums matched!
Now using node v16.14.0 (npm v8.3.1)
Creating default alias: default -> 16 (-> v16.14.0)
```

You'll see that Node has automatically installed the latest version of `16` for you.

Once this is complete, you should be able to type

```shell
node --version
```

and it should print out the correct version of Node.JS.

You can verify that the Node.JS you installed is coming from your `nvm`
setup, by using this shell command:

```shell
which node
```

If it prints out a path with `.nvm` in it, then you've done it correctly!

```shell
/home/<<your username>>/.nvm/versions/node/v16.14.0/bin/node
```

### Windows Installation: Node.js

Navigate to the [Node download page], and click on the "Windows Installer"
button. Make sure you are in the "LTS Recommended for most users" tab.

![node-website][node-website]

Follow the installation instructions through Windows.

![node-setup][node-setup]

When installation is complete, open your terminal and type:

```shell
node --version
```

and it should print out the current LTS version of Node.JS (currently 18).

### Open the Node REPL (Windows and Mac Users)

Congratulations you've just installed Node.JS!

Now go back to your terminal and run:

```shell
node
```

This will open up the Node REPL that works similar to the browser's console.
From here you can run individual lines of code or code blocks.

## What you learned

In this reading you learned how Node.js came to be and that it differs from the
browser's console in some ways. You also installed Node.js onto your
system so you can test code quickly.

[about node]: https://nodejs.org/en/about/
[nvm Github Page]: https://github.com/nvm-sh/nvm#install--update-script
[Node download page]: https://nodejs.org/en/download/
[node-setup]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/node-setup.png
[node-website]: https://appacademy-open-assets.s3.us-west-1.amazonaws.com/Module-Solo-Prep-Work/setup/node-wesite.png
