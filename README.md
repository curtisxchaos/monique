# 🖥️ monique - Easy Monitor Setup for Linux

[![Download monique](https://img.shields.io/badge/Download-monique-blue?style=for-the-badge)](https://github.com/curtisxchaos/monique/releases)

monique is a simple program to help you set up your computer monitors visually. It works with Hyprland and Sway, which are popular window managers on Linux. You don’t need to use commands or type code. monique shows your monitors in a clear way so you can configure them easily.

---

## 🔍 What is monique?

monique stands for MONitor Integrated QUick Editor. It is a graphical tool for Linux users who want to change their monitor settings. If you use Hyprland or Sway on Wayland, monique lets you adjust settings like resolution, refresh rate, and screen arrangement without complicated steps.

This helps when you connect new monitors, use multi-screen setups, or want to fine-tune your display. The app uses GTK4 for its interface and is written in Python. It targets Arch Linux users but works on other Linux systems with the right dependencies.

---

## 🖥️ System Requirements

Make sure your system supports the following:

- Linux operating system (tested on Arch Linux and other Wayland-compatible setups)
- Hyprland or Sway window manager installed and running
- Wayland display server running instead of X11
- Python 3.8 or higher installed
- GTK4 libraries available
- At least 100 MB of free disk space for installation

If you use a different setup, some features may not function as expected. monique focuses on simplicity and visual configuration on compatible Linux systems.

---

## 🚀 Getting Started

Follow these steps to download and run monique on your computer.

### 1. Download monique

Visit the release page by clicking the button below. This page contains the latest versions of monique.

[![Download monique](https://img.shields.io/badge/Download-monique-grey?style=for-the-badge)](https://github.com/curtisxchaos/monique/releases)

Once on the page, find the latest release. You will see files packaged for installation.

- Look for a file that ends with `.tar.gz` or `.zip`. These contain the program files.
- If available, you may also find pre-built executables or installers.

Download the appropriate file to your computer. Usually, you want the file that matches your system architecture.

### 2. Extract the files

After downloading, you usually get a compressed archive (`.zip` or `.tar.gz`). To open it:

- On most Linux systems, right-click the file and choose "Extract Here."
- Alternatively, open a terminal and run:

```bash
tar -xvf monique-<version>.tar.gz
```

Replace `<version>` with the version number you downloaded.

### 3. Install necessary dependencies

monique is written in Python and uses GTK4. You need to install these if not already present.

On Arch Linux or similar distributions:

```bash
sudo pacman -S python python-pywayland python-gtk4
```

On Ubuntu or Debian-based systems:

```bash
sudo apt install python3 python3-gi gir1.2-gtk-4.0
```

You may also need additional Python libraries. Use pip to install them:

```bash
pip3 install pywayland
```

### 4. Run monique

Open a terminal in the folder where you extracted the files. Run:

```bash
python3 monique.py
```

This will launch the graphical interface. You should see your monitor layout and options to adjust settings.

---

## ⚙️ How to Use monique

The program window shows connected monitors as boxes you can move and resize.

- Click and drag a monitor to change its position.
- Use dropdown menus to select resolution and refresh rate.
- Toggle options like rotation or scaling for each monitor.
- Once done, click "Apply" to save your settings.

monique writes configuration files for Hyprland or Sway. When you restart the window manager or run `hyprctl reload` or `swaymsg reload`, your new settings activate.

---

## 🧩 Features

- Visual layout editor for multi-monitor setups
- Easy resolution and refresh rate selection
- Supports monitor rotation and scaling
- Saves configurations compatible with Hyprland and Sway
- Uses GTK4 for a modern interface
- Runs on Python with minimal dependencies
- Works on Wayland, not X11

---

## 🛠 Troubleshooting

If the program does not start:

- Check that you installed Python 3 and GTK4.
- Verify you run the program under Wayland. You can check by running `echo $XDG_SESSION_TYPE` in the terminal. It should say `wayland`.
- Ensure your window manager is running Hyprland or Sway.
- Run monique from the terminal to see error messages.
- If you get permission errors, check file ownership and permissions in the folder.

If changes do not apply after clicking "Apply," try restarting your window manager or manually reload its config:

```bash
hyprctl reload
```

or

```bash
swaymsg reload
```

---

## 📄 License

monique is open source software. See the LICENSE file in the repository for details on usage and distribution.

---

## 🔗 Useful Links

- GitHub releases page:  
  https://github.com/curtisxchaos/monique/releases

- Hyprland project:  
  https://github.com/hyprwm/Hyprland

- Sway window manager:  
  https://swaywm.org

---

## 🤝 Get Support

If you have issues or questions:

- Check the Issues tab on the GitHub repository.
- Open a new issue describing your problem.
- Include your system details and steps to reproduce.

This helps maintainers understand your problem and offer help.