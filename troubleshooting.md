# Troubleshooting

1. [When I open Windows Explorer through Ubuntu it goes to a different folder than in the guide](#When-I-open-Windows-Explorer-through-Ubuntu-it-goes-to-a-different-folder-than-in-the-guide)
1. [Ubuntu on Windows 10 high CPU usage crashes](#Ubuntu-on-Windows-10-high-CPU-usage-crashes)
1. [When I pull from the `batch6-students` repository I get an error](#When-I-pull-from-the-batch6-students-repository-I-get-the-error)
1. [When I try to open `jupyter notebook` I get an error](#When-I-try-to-open-jupyter-notebook-I-get-the-error)
1. [When I use the `cp` command the `>` sign appears and the command does not execute](#When-I-use-the-`cp`-command-the->-sign-appears-and-the-command-does-not-execute)
1. [When setting up Python 3.x I get an error](#when-setting-up-python-3x-i-get-an-error)
1. [Nothing happens when I type my password](#Nothing-happens-when-I-type-my-password)
1. [I still have a NotImplemented error](#I-still-have-a-NotImplemented-error)
1. [I get an error when creating the virtual environment](#I-get-an-error-when-creating-the-virtual-environment)
1. [Checksum verification failed](#Checksum-verification-failed)
1. [My problem is not listed here what should I do?](#My-problem-is-not-listed-here-what-should-I-do?)
1. [Tutorial videos from Prep Course 2020](#Tutorial-videos-from-Prep-Course-2020)

#### When I open Windows Explorer through Ubuntu it goes to a different folder than in the guide

Please make sure:

* you are running the command `explorer.exe .` including the dot at the end.
* you are running Windows 10 version `1909` or newer.

#### Ubuntu on Windows 10 high CPU usage crashes

* First please make sure you are running Windows 10 version `1909` or newer.
* Then, try following [these steps](https://teckangaroo.com/enable-windows-10-virtual-machine-platform/)

#### When I pull from the `batch6-students` repository I get the error

```bash
error: Your local changes to the following files would be overwritten by merge:
<some files>
Please commit your changes or stash them before you merge.
Aborting
```

_git_ is telling us that changes were made by you to the files on the `~/projects/batch6-students` folder, and is not pulling the changes made by the instructors because they would override the changes that you made there. To fix this do the following:

1. make sure that any change you made to the files on `~/projects/batch6-students`  (that you want to not lose) is saved in your `~/projects/batch6-workspace` repository (see `https://github.com/LDSSA/batch6-students#updates-to-learning-units` for how to do this), and if you don't want to keep the changes you made to these files, just continue on to the next step
2. go to the `~/projects/batch6-students` folder and run:

    ```bash
    cd ~/projects/batch6-students
    git stash
    ```

3. now you can pull from the `batch6-students` repository:

    ```bash
    git pull
    ```

#### When I try to open `jupyter notebook` I get the error

```bash
migs-MBP% jupyter notebook
zsh: command not found: jupyter
```

Before opening `jupyter notebook` activate your virtual environment:

```bash
source ~/.virtualenvs/slu00/bin/activate
```

#### When I use the `cp` command the `>` sign appears and the command does not execute

```bash
cp -r ~/projects/batch6-students/"S01 - Bootcamp and Binary Classification"/"SLU01 - Pandas 101" ~/projects/batch6-workspace/"S01 - Bootcamp and Binary Classification"
>
```

Make sure to use this type of quotes `"` and not these ones `“`.

#### When setting up Python 3.x I get an error

When I run this command:

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
```

I get this error:

```bash
W: GPG error: http://apt.postgresql.org/pub/repos/apt focal-pgdg InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 7FCC7D46ACCC4CF8
```

Solution: Take the id in front of `NO_PUBKEY` (in my case its `7FCC7D46ACCC4CF8`) and run the following command:

```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 7FCC7D46ACCC4CF8
```

#### Nothing happens when I type my password

In **step two** it asks me for the computer password. However, I am not being able to write anything

Solution:
When you write your password you might not get any visual feedback and that's okay! Write it as normal and hit <kbd>enter</kbd> when you're done!

#### I still have a NotImplemented error

I've completed the exercise in the Exercise Notebook but when I run the cell I get a **NotImplementedError**.

Solution:
The `raise NotImplementedError()` are added to the exercise cell as a placeholder for where you're supposed to add your solution/code. It is meant to be removed!

#### I get an error when creating the virtual environment

I ran `python3.8 -m venv ~/.virtualenvs/slu00`, but got the following error:

>The virtual environment was not created successfully because ensurepip is not available.

This can happen if either you [skipped the installation of python-pip](https://github.com/LDSSA/LDSA-setup/blob/main/python-venv.md), or the version of the python you're calling doesn't have python pip installed.

As we're using python3.8 for this academy, and if you've followed all the steps in this README correctly, you should be able to create the virtual environment with:

```bash
python3.8 -m venv ~/.virtualenvs/slu00
```

#### Checksum verification failed

I'm getting "checksum verification failed" on a portal submission.

Some metadata can change when you open your jupyter notebook using vscode. Try running the notebooks from start to end in Jupyter and resubmit.

#### My problem is not listed here what should I do?

If the above steps didn't solve the problem for you, please contact us on Slack or [open an issue](https://guides.github.com/features/issues/) in this repo.

#### Tutorial videos from Prep Course 2020

If you want a visual guide, you can look at the **tutorial videos** from the **Prep Course of year 2020**.

:warning: These videos are **out of date**, and should only be used as a visual guide of what the setup process looks like. The steps you should follow are detailed in this document.

 * [Setup guide for Windows - Part 1](https://www.youtube.com/watch?v=fWi3bYoHW18)
* [Setup guide for Windows - Part 2](https://www.youtube.com/watch?v=bnJOQHh9pJ4)
* [Setup guide for Mac](https://www.youtube.com/watch?v=qs0z4ibMFdU)
* [Updates to Learning Units guide for Windows 10](https://www.youtube.com/watch?v=Q2Cezm6ufrE)
* [Updates to Learning Units guide for Mac](https://www.youtube.com/watch?v=-fzIDfNBZ0I)

### Other

If your problem doesn't fit in any  of the previous categories head over to slack and ask.
Someone will surely point you in the right direction.

If you're looking for some specific part of our organization head over to the
[Member Directory](https://ldssa.github.io/wiki/About%20us/Member-Directory/)
and search for the area of responsibility you're looking for.