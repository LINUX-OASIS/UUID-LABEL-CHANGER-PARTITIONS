# 🚀 Partition UUID & Label Changer 🚀

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![Shell Script](https://img.shields.io/badge/Shell_Script-100%25-lightgrey?logo=gnubash&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Linux-yellow.svg?logo=linux)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-welcome-brightgreen.svg?style=flat)](https://github.com/LINUX-OASIS/uuid-label-changer/issues)
[![GitHub issues](https://img.shields.io/github/issues/LINUX-OASIS/uuid-label-changer)](https://github.com/LINUX-OASIS/uuid-label-changer/issues)
[![GitHub PRs](https://img.shields.io/github/issues-pr/LINUX-OASIS/uuid-label-changer)](https://github.com/LINUX-OASIS/uuid-label-changer/pulls)

A powerful and safe TUI (Text-based User Interface) utility for changing the `UUID` and `LABEL` of your Linux partitions. Built with `bash` and `whiptail`, this script provides a user-friendly way to manage partition identifiers without needing to memorize complex command-line arguments.

!Script Demo

---

## ✨ Features

*   **Interactive TUI**: Easy-to-navigate menus powered by `whiptail`.
*   **🛡️ Safe Operations**: Automatically checks for mounted partitions and prompts to unmount them before making changes.
*   **🔍 Filesystem Checks**: Performs pre-flight consistency checks (`e2fsck`, `btrfs check`) to ensure data integrity.
*   **📂 Broad Filesystem Support**: Works with `ext4`, `btrfs`, and `vfat` (FAT32) partitions.
*   **🤖 Automatic Dependency Installation**: Checks for required tools and installs them via `apt` if missing.
*   **🎨 Custom UUIDs**:
    *   Generate a fully **random** UUID.
    *   Create a "vanity" UUID with a **repeating character** (e.g., `AAAAAAAA-AAAA-AAAA-AAAA-AAAAAAAAAAAA`).
*   **🏷️ Label Management**: Easily change partition labels for better organization.
*   **🔄 Kernel Update**: Forces the kernel to re-read the partition table after changes using `partprobe`.

---

## 💻 Compatibility

This script is designed for Debian-based Linux distributions that use the `apt` package manager. It is known to be compatible with:

*   Debian
*   Ubuntu (and its flavors like Kubuntu, Xubuntu)
*   Linux Mint
*   ...and other Debian derivatives.

---

## 🛠️ Dependencies

The script requires several command-line utilities to function. It will automatically check for these and attempt to install any that are missing using `sudo apt install`.

*   `btrfs-progs`
*   `whiptail`
*   `mtools`
*   `uuid-runtime` (for `uuidgen`)
*   `dosfstools` (for `fatlabel`)
*   `e2fsprogs` (for `e2fsck`, `tune2fs` - usually pre-installed)

---

## ⚙️ Installation & Usage

1.  **Clone the repository (or download the script):**

    ```bash
    # Replace with your actual repository URL
    git clone https://github.com/LINUX-OASIS/uuid-label-changer.git
    cd uuid-label-changer
    ```

2.  **Make the script executable:**

    ```bash
    chmod +x custom-UUID-OR-LABEL-CHANGER-PARTITIONS.sh
    ```

3.  **Run the script with `sudo`:**

    The script requires root privileges for installing packages, unmounting partitions, and modifying filesystem metadata.

    ```bash
    sudo ./custom-UUID-OR-LABEL-CHANGER-PARTITIONS.sh
    ```

4.  Follow the on-screen interactive prompts to select your partition and the desired action.

---

## 💬 Contributing

Pull requests, issues, and suggestions are warmly welcomed!

For major changes, please open an issue first to discuss what you would like to change. See CONTRIBUTING.md for guidelines.

---

## 🧙‍♂️ Maintainer

*   **LINUX-OASIS**

---

## 📜 License

This project is licensed under the **GNU General Public License v3.0**.

See the LICENSE file for details.

```
Copyright (C) 2023 LINUX-OASIS

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
