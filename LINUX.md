# Set-up instructions for Linux

Welcome to **Linux/Ubuntu set up** repository!

Your first step in this journey is to **carefully read** the steps in this tutorial. You'll learn:

- :arrow_right: How to set up your environment;

1. [Initial Setup](#initial-setup)
    1. [Ubuntu Setup](#Ubuntu-Setup)

<br>

## Initial Setup

<br>

### Ubuntu Setup

So you're using Ubuntu, hun? Well, kudos to you. You just need to install a couple of packages.


**Step 1:** Open a terminal and check what version of Python you have by using the command below. If your version is `Python 3.8.x` (`x` = any number), you can skip to step 2, otherwise continue with step 1.1 and 1.2

```bash
python3.8 --version
```

**Step 1.1:** Run the following commands to setup _Python 3.8_ (if you get an error with this command, check [this](#6-When-setting-up-python-3.7-i-get-an-error)
):

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
```

**Step 1.2:** Run the following commands to install _Python 3.8_

```bash
sudo apt update && sudo apt install python3.8 -y
```

**Step 2** Run the following command to get `pip` and `venv`:
```bash
sudo apt update && sudo apt upgrade && sudo apt install python3-pip python3.8-venv -y
```

>**Why do we install these?**
>
> We'll be using `pip` which is the reference Python package manager. You should always use a virtual environment to install python packages. We'll use `venv` to set them up.

<br>