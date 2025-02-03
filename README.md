# platform-tools-installers-cli

🚀 It is a command-line script designed to quickly install [Android SDK Platform Tools](https://developer.android.com/studio/releases/platform-tools) (ADB, Fastboot) via PowerShell on Windows

## 🛠️ Installation

To install Android SDK Platform Tools (ADB, Fastboot) on Windows, simply run the following command in PowerShell:

```powershell
powershell -c "irm cutt.ly/platform-tools | iex"
```

This command downloads and executes the PowerShell script, which automatically installs the required tools from the [original Google package](https://dl.google.com/android/repository/platform-tools-latest-windows.zip).

## 🤔 How does it work?

1. The script first asks for agreement to the [Android SDK Platform-Tools Terms and Conditions](https://developer.android.com/studio/terms)
2. After your consent, the script downloads the archive with these tools, which is available at the link <https://dl.google.com/android/repository/platform-tools-latest-windows.zip> (the file name may be different depending on your operating system, in this case the archive for Windows)
3. The archive is unpacked into the folder `C:\platform-tools` (soon it will be possible to choose the folder for installation)
4. This folder is then added to the user's `Path` environment variable so that you can use these tools from the terminal regardless of which folder you are in (Read [https://en.wikipedia.org/wiki/PATH_(variable)](https://en.wikipedia.org/wiki/PATH_(variable)#DOS,_OS/2,_and_Windows:~:text=When%20a%20command%20is,locations%2C%20or%20invalid%20locations.))

## 🚀 Usage

After installation, you need to restart the computer, after which you can use `adb` and `fastboot` commands from your terminal:

```bash
adb --version
fastboot --version
```

These commands will output the installed versions of the respective tools.

## 🧑‍💻 Contributing

Feel free to open a [pull request](https://github.com/cli-stuff/platform-tools-installers-cli/pulls) or [issue](https://github.com/cli-stuff/platform-tools-installers-cli/issues) if you have any suggestions, improvements, or bug reports.

## ❤️ Support

If you like this project, consider supporting it by starring ⭐ it on GitHub, sharing it with your friends, or [buying me a coffee ☕](https://github.com/cli-stuff/platform-tools-installers-cli?sponsor=1)

## 📜 License

This project is licensed under the [MIT License](LICENSE).
