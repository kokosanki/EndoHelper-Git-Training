# EndoHelper-Git-Training
A training repository for EndoHelper team members.

## Download
You can train locally, by simply cloning the repository, or fork it, so that
you can push your changes. Local clone is simpler and only requires git,
while a fork requires github account and setting ssh key.

### Local clone
If you prefer to work locally, enter command:

```bash
git clone https://github.com/Udiknedormin/EndoHelper-Git-Training.git
```

It should create a new directory named EndoHelper-Git-Training.
This is the sandbox for the training. 

Note that if you try to push to it, an error will be reported.

### Fork
To work with a fork, you will need a GitHub account. You can register for
free if you don't have one already.

#### Set up SSH
Once you have a github account, you'll need to get an ssh key associated
with it. Follow the steps for
[setting up ssh with Github](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh),
which is more or less:
 * generate new ssh key
   * `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
 * add your ssh key to ssh agent
   * `eval "$(ssh-agent -s)"` ([bash](https://www.gnu.org/software/bash/) and
     [zsh](http://www.zsh.org/)) or
     `eval (ssh-agent -s)` ([fish](https://fishshell.com/))
   * `ssh-add ~/.ssh/id_rsa`
 * [add the key to your github account](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
   * copy the public key to the clipboard
     * Arch: `sudo pacman xclip xsel; xclip -sel clip < ~/.ssh/id_rsa.pub`
     * Debian, Ubuntu, Mint: `sudo apt-get install xclip; xclip -sel clip < ~/.ssh/id_rsa.pub`
     * Fedora: `sudo dnf xclip xsel; xclip -sel clip < ~/.ssh/id_rsa.pub`
     * MacOS: `pbcopy < ~.ssh/id_rsa.pub`
   * on GitHub, go to: `Settings -> SSH and GPG keys -> New SSH key`
   * Title: enter any title you like
   * Key: paste the public key
     * PC: Ctrl + V
     * MacOS: Command + V (⌘ + V)
   * confirm with `Add SSH Key`

Now you should be able to commit to repositories cloned via ssh.

#### Fork and clone
On this repostory github page, click `Fork` (next to `Star` and
`Watch`/`Unwatch`). You will now get your own copy of this repository.

Click `Code`. If the pop-up's title is `Clone with HTTPS`, click `Use SSH`.
Copy the link in the window (you can do it easily by clicking on a button
next to it).

Go to your shell and enter `git clone ` - space - paste-what-you-copied.

Now, your local copy refers to your fork instead of this repository and
threfore you can push your commits (and make PRs to the original repo).

## Usage
Subsequent steps to be executed can be found in numbered files. Start with
[00_hello.md](./00_hello.md).
