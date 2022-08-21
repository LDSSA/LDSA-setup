# Creating a Python Virtual Environment

Bellow are the instructions that are enough to get the setup done and get you up and running :)
You can also follow [this guide](guides/How_to_set_up_python_virtual_environments.md) for a more in depth set of instructions that accomplish exactly the same thing.

:warning: **You should always be using a virtual environment to install python packages.** :warning: We'll use _venv_ to set them up.

To install and update packages, we'll be using _pip_ which is the reference Python package manager.

**Step 1** Start by installing ensuring pip, setuptools, and wheel are up to date:

```bash
python3.8 -m pip install --user --upgrade pip setuptools wheel
```

**Step 2** Create a virtual environment with the name `slu00`

```bash
python3.8 -m venv ~/.virtualenvs/slu00
```

**Step 3** Activate the environment

```bash
source ~/.virtualenvs/slu00/bin/activate
```

>Note: after you activate your virtual environment you should see at the leftmost of your command line the name of your virtual environment surrounded by parenthesis, like this:

```bash
mig@my-machine % source ~/.virtualenvs/slu00/bin/activate
(slu00) mig@my-machine %
```

And you're able to make sure your virtual environment is active using the `which` command (it outputs the location of your virtual environment's python installation):

```bash
(slu00) mig@my-machine % which python
/Users/mig/.virtualenvs/slu00/bin/python
```

**Step 4** Now update pip.

```bash
(slu00) pip install -U pip
```
