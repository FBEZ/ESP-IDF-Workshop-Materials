Here is the English translation, with a clear and friendly technical-writing tone:
# 🍎 Installing VS Code and Prerequisites – macOS

## Installing VS Code

* Go to the [VS Code download page](https://code.visualstudio.com/download)
* Download and install the macOS version
  ![](../../assets/setup/1_ubuntu_vscode_download.webp)

> [!WARNING]
> This guide uses macOS Sequoia.

* After downloading the file, install VS Code
* Press `CTRL+SPACE`, search for **Code**, and click the VS Code icon
* You should now see the VS Code interface
  ![](../../assets/setup/2_vscode_screen.webp)

> [!NOTE]
> When opening a folder in VS Code, you may see a pop-up asking whether you trust the authors of the folder. This matters when working with `git` repositories, but for now it makes no difference. Click **Yes**.

## Installing prerequisites

To *install* and configure the ESP-IDF toolchain, you must have Python and Git already installed.
This guide uses the [Homebrew](https://brew.sh/) (`brew`) package manager.

### Install Homebrew

To install Homebrew:

* Open a terminal
* Run:

  ```console
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

### Python

ESP-IDF uses the system Python.
You can verify your python version by running:

```console
python3 --version
```

> [!NOTE]
> If Python is not installed, you can install it with:
>
> ```console
> brew install python3
> ```

### Git

ESP-IDF development is based on [`git`](https://git-scm.com/), the version control tool used by many major open-source projects, including the Linux kernel. Git is also the foundation of GitHub.

To install git:

* Open a terminal
* Install `git`:

  ```console
  brew install git
  ```
* Verify installation:

  ```console
  git --version
  git version 2.43.0
  ```

### Installing additional prerequisites

To *use* the ESP-IDF toolchain, you must install additional tools.

* Open a terminal
* Run:

  ```console
  brew install cmake ninja dfu-util
  ```

If you encountered errors during installation, refer to the [Troubleshooting](#troubleshooting) section to see if your issue matches one of the common cases described there.

## Next steps

> Continue with the [next step](README.md#installazione-dellestensione-per-vs-code).

---

## Troubleshooting

During installation, you may encounter some common errors.
Below are the most frequent issues along with their causes and solutions.

### Xcode Command Line Tools not installed

**Error**

```console
xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools),
missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun
```

**Cause**
The Xcode Command Line Tools are not installed or not configured correctly.

**Solution**

```console
xcode-select --install
```

### Toolchain not found (`xtensa-esp32-elf`)

**Error**

```console
WARNING: directory for tool xtensa-esp32-elf version esp-2021r2-patch3-8.4.0 is present, but tool was not found
ERROR: tool xtensa-esp32-elf has no installed versions. Please run 'install.sh' to install it.
```

**Cause**
On macOS with Apple Silicon, some binary tools require Rosetta 2.

**Solution**

```console
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```

### “Bad CPU type in executable” error

**Error**

```console
zsh: bad CPU type in executable: ~/.espressif/tools/xtensa-esp32-elf/esp-2021r2-patch3-8.4.0/xtensa-esp32-elf/bin/xtensa-esp32-elf-gcc
```

**Cause**
The executable requires Rosetta 2 to run on Apple Silicon systems (M1/M2/M3).

**Solution**

```console
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```

