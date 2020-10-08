## Setting up Node the right way on Linux

Node works on many platforms, and there are many ways to install Node on each platform. This short article covers the best-practice setup of Node.js on Linux machines.

By the end of this article, you should be able to:
- Discover the best way to set up and use Node on Linux.
- Learn how to manage multiple Node versions.


> 
This article is specifically base on the Linux machine but can be used to install Node on macOS.

**How Not to Install Node**

Frequently Node.js can be installed by simply visiting `https://nodejs.org` and downloading for a particular operating system. Or from a package manager, for instance, `apt-get install nodejs` on Debian/Ubuntu. It is strongly recommended against using this approach to install Node. This approach tends to lag behind the faster Node.js release cycle.

Another notable issue using this approach is that installing global modules with Node's module installer (`npm`) tends to require the use of `sudo` (a command which grants root privileges). This is not an ideal setup for a developer machine and granting root privileges to the install process of third-party libraries is not a good security practice.

**A Better Way to Install Node Using a Version Manager**


> 
It's strongly recommended that if Node is installed via an Operating System package manager or directly via the website, that it be completely uninstalled before proceeding to the following sections.

The recommended way to install Node.js on Linux is by using a Node Version Manager (`nvm`). See https://github.com/nvm-sh/nvm for more details.

We're going to install `nvm` and then use it to install Node.

The way to install `nvm` is via the install script at `https://github.com/nvm-sh/nvm/blob/v0.36.0/install.sh`. If `curl` is installed (it usually is) a single command can be used to install and setup nvm:


> 
If using `zsh`, the bash part of the command can be replaced with `zsh`

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.36.0/install.sh | bash
```

Or using Wget command:

```bash
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.36.0/install.sh | bash
```
To check that the installation was successful execute the following in the terminal:

```bash
command -v nvm
```
It should output nvm. If this fails, close and reopen the terminal (or SSH session) and try running the command again.

Now that we have a version manager, let's install the Node.

```bash
nvm install 12
```

This will install the latest version of Node 12:


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1602170228103/HWzR4MNA0.png)

The command installed Node v12.19.0 which is the latest Long Term Support (LTS) version at the time of writing this article.

We can verify that Node is installed, and which version, with the following command:

```bash
node -v
```

**Managing multiple Node versions**

To install other versions of Node, we can simply execute these commands: 

Where x.x.x is the version of Node we want to install.

```bash
nvm install x.x.x
```

Where x.x.x is the version of Node we want our machine to use

```bash
nvm use x.x.x
```

Congratulations, you now have the right setup on your Linux machine.



