# Set-up instructions for Windows

Welcome to **Windows set up** repository!

Your first step in this journey is to **carefully read** the steps in this tutorial. You'll learn:

- :arrow_right: How to set up your environment;

1. [Initial Setup](#initial-setup)
    1. [Windows 10 Setup](#Windows-10-Setup)
    1. [Windows 11 Setup](#Windows-11-Setup)
    
<br>

## Initial Setup

<br>

### Windows 10 Setup

This section deals with setting up **Windows Subsystem for Linux (WSL) on Windows 10**.

> If you are using MacOS or Linux you can skip this section.

**Why do I need to install WSL?**

Because of the differences in command line syntax between Windows vs Mac OS/Linux, it would be a great challenge for us to support and provide instructions for both Operating Systems. For this reason, we’d ask you to **install Windows Subsystem for Linux** which enables you to run Linux command lines inside Windows.

:warning: Keep in mind that these are simply extensions to your Windows operating system, hence, installing this software will not do any changes on your laptop. It is also quick to do so. :warning:

**Step 1:** Follow **[this guide](../guides/Windows_Subsystem_for_Linux_Installation_Guide_for_Windows_10.md)** to setup WSL on Windows 10.

**Step 2:** Open a terminal (remember **[this](guides/Windows_Subsystem_for_Linux_Installation_Guide_for_Windows_10.md#Opening-the-WSL-terminal)**!!) and run the following command:

```bash
sudo apt update && sudo apt upgrade && sudo apt install git
```

**Step 3:** Open a terminal (remember **[this](guides/Windows_Subsystem_for_Linux_Installation_Guide_for_Windows_10.md#Opening-the-WSL-terminal)**!!) and check if you already have `python3.8` by usind the command below. If your version is `Python 3.8.x` (`x` = any number), you can skip to step 4, otherwise continue with step 3.1 and 3.2

```bash
python3.8 --version
```
**Step 3.1:** Run the following commands to setup _Python 3.8_ (if you get an error with this command, check [this](#6-When-setting-up-python-3.7-i-get-an-error)
):

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
```

**Step 3.2:** Run the following commands to install _Python 3.8_

```bash
sudo apt update && sudo apt install python3.8 -y
```

**Step 4** Run the following command to get `pip` and `venv`:
```bash
sudo apt update && sudo apt upgrade && sudo apt install python3-pip python3.8-venv -y
```
>**Why do we install these?**
>
> We'll be using `pip` which is the reference Python package manager. You should always use a virtual environment to install python packages. We'll use `venv` to set them up.

<br>

