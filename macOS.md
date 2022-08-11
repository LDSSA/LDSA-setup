# Set-up instructions for MacOS 

Welcome to **MacOS set up** repository!

Your first step in this journey is to **carefully read** the steps in this tutorial. You'll learn:

- :arrow_right: How to set up your environment;
- :arrow_right: The weekly workflow to follow during the Academy

1. [Initial Setup](#initial-setup)
    1. [MacOS Intel Setup](#MacOS-Intel-Setup)
    1. [MacOS M1 Setup](#MacOS-M1-Setup)


<br>

## Initial Setup

<br>

### MacOS Intel Setup

Some of the steps in the following sections will require _Homebrew_ for MacOS.
Homebrew will make it easier to install software that we will use later on.

**Step 1:** To open the terminal, choose one:
* In Finder <img src='assets/finder.png' alt='Finder' width="4%" />, open the /Applications/Utilities folder, then double-click Terminal.
* By pressing <kbd>cmd</kbd> + <kbd>space</kbd> then type `terminal` and press <kbd>enter</kbd>.

    The terminal should now be open:

    <img src='assets/mac_terminal.png' width="50%" />

**Step 2:** To install Homebrew for MacOS, copy and paste the following line in the terminal:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

**Step 2.1:** Sometimes it's necessary to install xcode command line utils. To do so, do the following command before installing homebrew:

```bash
xcode-select --install
```

You may be prompted to install the _Command Line Developers Tools_. Confirm and, once it finishes, continue installing _Homebrew_ by pressing <kbd>enter</kbd> again.

**Step 3:** open a terminal and run the following command:

```bash
brew update --verbose
```

**Step 4:** then run the following command:

```bash
brew install git
```

**Step 5:** then run the following command:

```bash
brew install python@3.7
```

**Step 6:** then run the following command:

```bash
brew link python@3.7
```

<br>

### MacOS M1 Setup

So you got the new M1 and you're supper happy with how fast it is.. Unfortunately dealing with apple silicon requires a little get around. But don't worry, we'll be able to get there in the end.

**Step 1:** To open the terminal, choose one:
* In Finder <img src='assets/finder.png' alt='Finder' width="4%" />, open the /Applications/Utilities folder, then double-click Terminal.
* By pressing <kbd>cmd</kbd> + <kbd>space</kbd> then type `terminal` and press <kbd>enter</kbd>.

    The terminal should now be open:

    <img src='assets/mac_terminal.png' width="50%" />

<br>

**Step 1.1:** To use intel-based software, you'll need **Rosetta2**. Most of you should already have it installed for varied reasons. If you don't simply run the following line in the terminal:

```bash
softwareupdate --install-rosetta
```

This will launch the rosetta installer and you’ll have to agree to a license agreement.


**Step 2:** To install Homebrew x86 version, aka `ibrew` for MacOS, copy and paste the following line in the terminal:

```bash
arch -x86_64 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

**Step 2.1:** Sometimes it's necessary to install xcode command line utils. To do so, do the following command before installing homebrew:

```bash
xcode-select --install
```

**Step 3:** Add an alias with `ibrew` to your $PATH

```bash
echo 'alias ibrew="arch -x86_64 /usr/local/bin/brew"' >> ~/.zshrc
```

**Step 4:** Activate the alterations done to .zshrc
```bash
source ~/.zshrc
```

**Step 5:** Install Python 3.8 with `ibrew`

```bash
ibrew install python@3.8
```

**Step 6:** Add Python 3.8 to $PATH

```bash
export PATH="/usr/local/opt/python@3.8/bin:$PATH" >> ~/.zshrc
```

**Step 7** Re-activate the alterations done to .zshrc
```bash
source ~/.zshrc
```

<br>
