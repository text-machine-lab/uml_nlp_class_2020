Read the handout.pdf for full homework instructions.
Download the starter code [here](http://web.stanford.edu/class/cs224n/assignments/a4.zip).

**Deadlines:**
1. March 30 2020 (set up a remote repository)
1. April 6 2020 (code)
1. April 8 2020 (written)

To check the late submission policy, go to https://sites.google.com/site/umlnlpspr2020/assignments.

# Before you start

We recommend creating a git repository for this homework.
If you are not familiar with Git, we recommend [Codecademy Git tutorial](https://www.codecademy.com/learn/learn-git).

1. Create a **private** repository on GitHub ([guide](https://help.github.com/en/enterprise/2.16/user/github/getting-started-with-github/create-a-repo)).
1. In the command line (on your local computer) execute `git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY` to download the repository from git.
1. Download the [starter code](http://web.stanford.edu/class/cs224n/assignments/a4.zip) and unzip it to the repository folder
1. Commit project files and execute `git push` to upload them to GitHub

This will allow you to sync your local code and remote machine code. Every time you want to upload a new version, commit it locally, push it and pull it on a remote machine.


# How to connect to remote GPU servers

CS department provides you with GPU machines you can use for the homeworks (and you will need it for this one).
In total there are ~30 servers. Their addresses are of the form `dan417-XX.uml.edu` where `XX` is the server number in range 01-30. E.g., if you want to connect to server number 8 you use `dan417-08.uml.edu`.

To do this, use `ssh`. If you're not familiar with `ssh` we would recommend [this tutorial](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys).

We recommend developing and debugging your code locally and only using the server to actually train the full model.

Since the lab machines are not accessible from the outside network, you need to first connect to the cs server (`cs.uml.edu`) and then connect to a lab machine (i.e. `dan417-16.uml.edu`). You can do this manually:

1. `ssh YOUR_USERNAME@cs.uml.edu` - connect to the cs network
1. `ssh dan417-16.uml.edu` - from the cs network, connect to the machine number 16

You will see something like this:

```bash
~$ ssh vlialin@cs.uml.edu  # You are on your local machine, connect to CS
Welcome to Ubuntu 18.04.3 LTS (GNU/Linux 4.15.0-88-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage


 * Canonical Livepatch is available for installation.
   - Reduce system reboots and improve kernel security. Activate at:
     https://ubuntu.com/livepatch

96 packages can be updated.
7 updates are security updates.

*** System restart required ***
Last login: Tue Jan 21 12:01:18 2020 from 10.91.224.200
vlialin@cs4:~$ ssh dan417-16.uml.edu  # You are on CS network, connect to dan417 machine
The authenticity of host 'dan417-16.uml.edu (10.116.13.49)' can't be established.
ECDSA key fingerprint is SHA256:VvWIlTuMC+SRuhVKXON2gaLl5ThB3eqFuBgsbMdD+Wk.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'dan417-16.uml.edu,10.116.13.49' (ECDSA) to the list of known hosts.
vlialin@dan417-16.uml.edu's password:
Welcome to Ubuntu 18.04.3 LTS (GNU/Linux 4.15.0-88-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage


 * Canonical Livepatch is available for installation.
   - Reduce system reboots and improve kernel security. Activate at:
     https://ubuntu.com/livepatch

220 packages can be updated.
1 update is a security update.

vlialin@dan417-16:~$ # You are on dan417 machine
```

Alternatively, you can setup `~/.ssh/config` using [this guide](https://github.com/text-machine-lab/uml_nlp_class_2020/blob/master/env_setup.md).

# How to upload your code

Initial setup:
1. Create a git repository as it was described in _Before you start_ section
1. Connect to cs GPU machine
1. Clone your git repository (just as you did _Before you start_ section on your local computer)

Now you have your repository on a cs server and can sync it with GitHub using a single command
1. `git pull`

We do not recommend editing your code on a remote machine if you are not familiar with git and `git merge`. If you need to make any code changes, make them on your machine, commit and push them to GitHub.

Note that you don't need to upload your code to every server you use. CS machines use [distributed file system](https://en.wikipedia.org/wiki/Clustered_file_system#Distributed_file_systems) so your home folder is synced between them.
