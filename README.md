<div align="center">

# 🐉 Install Kali Linux in VMware Workstation Pro

**A complete, screenshot-by-screenshot guide: download Kali Linux 2025.4, build a virtual machine, and finish the graphical install.**

![Kali Linux](https://img.shields.io/badge/Kali_Linux-2025.4-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![VMware](https://img.shields.io/badge/VMware_Workstation_Pro-25H2-607078?style=for-the-badge&logo=vmware&logoColor=white)
![Steps](https://img.shields.io/badge/Steps-32-2ea44f?style=for-the-badge)
![Level](https://img.shields.io/badge/Level-Beginner-blue?style=for-the-badge)

[📄 Download the PDF version](Kali-Linux-VMware-Install-Guide.pdf)

</div>

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Requirements](#-requirements)
- [Part 1 – Download Kali Linux](#-part-1--download-kali-linux)
- [Part 2 – Create the Virtual Machine](#-part-2--create-the-virtual-machine)
- [Part 3 – Install Kali Linux](#-part-3--install-kali-linux)
- [Part 4 – First Boot](#-part-4--first-boot)
- [Settings Cheat Sheet](#-settings-cheat-sheet)
- [Troubleshooting](#-troubleshooting)
- [Responsible Use](#-responsible-use)

---

## 🔎 Overview

[Kali Linux](https://www.kali.org/) is a Debian-based distribution built for security testing and digital forensics. It ships with hundreds of ready-to-use security tools, which makes it a popular choice for labs and courses.

Running Kali inside a **virtual machine (VM)** is the safest way to start: you can delete, re-create, or modify the VM at any time without affecting your real operating system.

This guide walks through the whole process in **4 parts and 32 steps**.

## ✅ Requirements

| Item | Details |
|---|---|
| **Hypervisor** | VMware Workstation Pro (this guide uses **25H2**) |
| **ISO image** | Kali Linux **2025.4 Installer** (x86_64) |
| **Apple Silicon Macs** | M1/M2/M3/M4 users must download the **Apple Silicon (ARM64)** image instead |
| **RAM for the VM** | 4 GB recommended (2 GB minimum) |
| **CPU cores for the VM** | 4 recommended |
| **Disk space** | 50 GB free (Debian 13.x recommends at least 20 GB) |
| **Internet** | Needed to download the ISO and, optionally, packages during install |

---

## ⬇️ Part 1 – Download Kali Linux

### Step 1 · Open the official download page

Go to **<https://www.kali.org/get-kali/>** and choose **Installer Images**. Always download from the vendor's website.

<img src="images/01-download-page.png" alt="Kali Linux download page with Installer Images highlighted" width="800">

### Step 2 · Download the installer ISO

Select **Kali Linux 2025.4**, open the **x86_64** tab, and click the download icon on the **Installer** card.

> [!IMPORTANT]
> If you use a MacBook with an Apple **M-series** chip (M1, M2, M3, M4), select **Apple Silicon (ARM64)** instead.

> [!TIP]
> Use the **sum** link next to the download to verify the file's checksum before installing.

<img src="images/02-download-iso.png" alt="Selecting the x86_64 Installer image" width="800">

---

## 🖥️ Part 2 – Create the Virtual Machine

### Step 3 · Create a new virtual machine

When the download finishes, open **VMware Workstation Pro** and click **Create a New Virtual Machine**.

<img src="images/03-new-vm.png" alt="VMware Workstation home screen" width="800">

### Step 4 · Choose the Typical configuration

Select **Typical (recommended)** and click **Next**.

<img src="images/04-typical.png" alt="New Virtual Machine Wizard, Typical selected" width="800">

### Step 5 · Install the operating system later

Select **I will install the operating system later**. This lets you adjust the hardware before the machine is created. Click **Next**.

<img src="images/05-install-later.png" alt="Install the operating system later option selected" width="800">

### Step 6 · Select the guest operating system

Select **Linux**, then choose **Debian 13.x 64-bit** as the version, because Kali is Debian-based. Click **Next**.

<img src="images/06-guest-os.png" alt="Guest operating system set to Linux, Debian 13.x 64-bit" width="700">

### Step 7 · Name the virtual machine

Enter a name such as **Kali Linux** and choose a folder to store the VM files. Click **Next**.

<img src="images/07-vm-name.png" alt="Virtual machine name and location" width="700">

### Step 8 · Specify the disk capacity

Set **Maximum disk size** to **50 GB** and choose **Store virtual disk as a single file**. Click **Next**.

<img src="images/08-disk.png" alt="Disk capacity set to 50 GB" width="700">

### Step 9 · Open Customize Hardware

The summary page shows the defaults (2048 MB RAM, 2 CPU cores). Click **Customize Hardware…** to change them.

<img src="images/09-customize.png" alt="Ready to Create Virtual Machine with Customize Hardware highlighted" width="700">

### Step 10 · Adjust memory, processors and attach the ISO

- Set **Memory** to **4 GB**
- Set **Processors** to **4**
- Select **New CD/DVD (SATA)** → **Use ISO image file** → browse to `kali-linux-2025.4-installer-amd64.iso`
- Click **Close**

<img src="images/10-hardware.png" alt="Hardware settings with the Kali ISO attached" width="700">

### Step 11 · Finish creating the VM

The summary now shows **4096 MB** memory and **4 CPU cores**. Click **Finish**.

<img src="images/11-finish.png" alt="Final summary before creating the VM" width="700">

### Step 12 · Power on the virtual machine

Click **Power on this virtual machine** to boot from the Kali installer ISO.

<img src="images/12-power-on.png" alt="Kali Linux VM ready to power on" width="800">

---

## 💿 Part 3 – Install Kali Linux

### Step 13 · Start the graphical installer

In the installer boot menu, select **Graphical install** and press **Enter**.

<img src="images/13-graphical-install.png" alt="Kali installer boot menu with Graphical install highlighted" width="800">

### Step 14 · Select the language

Choose **English** and click **Continue**.

<img src="images/14-language.png" alt="Language selection" width="800">

### Step 15 · Select your location

Choose the country where you live. The screenshot uses **United States**; your choice sets the time zone and locale. Click **Continue**.

<img src="images/15-location.png" alt="Location selection" width="800">

### Step 16 · Configure the keyboard

Select your keymap (**American English** in this guide) and click **Continue**.

<img src="images/16-keyboard.png" alt="Keyboard keymap selection" width="800">

### Step 17 · Set the hostname

Keep the default hostname **`kali`** or enter your own, then click **Continue**.

<img src="images/17-hostname.png" alt="Hostname prompt" width="800">

### Step 18 · Set the domain name

Leave the domain name **empty** for a home or lab setup and click **Continue**.

<img src="images/18-domain.png" alt="Domain name prompt" width="800">

### Step 19 · Enter the user's full name

Enter the real name for the new non-root user and click **Continue**. The installer then asks for a **username**; accept the suggestion or type your own and click **Continue**.

<img src="images/19-full-name.png" alt="Full name for the new user" width="800">

### Step 20 · Choose a password

Enter a strong password, re-enter it to verify, and click **Continue**.

> [!WARNING]
> The password in the original lab was a weak example and has been **masked** here. Never reuse it. Choose a unique password of your own.

<img src="images/20-password.png" alt="Password prompt with the password masked" width="800">

### Step 21 · Configure the clock

Select your time zone and click **Continue**.

<img src="images/21-timezone.png" alt="Time zone selection" width="800">

### Step 22 · Choose the partitioning method

Select **Guided – use entire disk and set up LVM** and click **Continue**.

> [!NOTE]
> This only affects the **virtual** disk. Your real computer is not touched.

<img src="images/22-partition-method.png" alt="Partitioning method with LVM selected" width="800">

### Step 23 · Select the disk to partition

Select the single virtual disk (**`sda`**, about 53.7 GB) and click **Continue**.

<img src="images/23-select-disk.png" alt="Disk selection" width="800">

### Step 24 · Choose the partitioning scheme

Select **All files in one partition (recommended for new users)** and click **Continue**.

<img src="images/24-scheme.png" alt="Partitioning scheme" width="800">

### Step 25 · Write the changes and configure LVM

Select **Yes** and click **Continue**.

<img src="images/25-write-lvm.png" alt="Confirm writing LVM changes" width="800">

### Step 26 · Set the volume group size

Keep the maximum value (about **52.7 GB**) and click **Continue**.

<img src="images/26-vg-size.png" alt="Volume group size" width="800">

### Step 27 · Confirm writing the partitions

Review the summary, select **Yes** to write the changes to disk, and click **Continue**. The base system is then installed.

<img src="images/27-write-changes.png" alt="Final confirmation to write partitions" width="800">

### Step 28 · Select the software to install

Keep the defaults and click **Continue**:

- ✅ **Xfce** desktop environment
- ✅ **top10** – the 10 most popular tools
- ✅ **default** – recommended tools

<img src="images/28-software.png" alt="Software selection with defaults" width="800">

### Step 29 · Install the GRUB boot loader

Select **Yes** to install GRUB to the primary drive and click **Continue**.

<img src="images/29-grub.png" alt="Install GRUB boot loader prompt" width="800">

### Step 30 · Choose the boot loader device

Select **`/dev/sda`** and click **Continue**.

<img src="images/30-grub-device.png" alt="Boot loader device selection" width="800">

### Step 31 · Finish the installation

When you see **Installation complete**, click **Continue** to reboot into your new system.

> [!TIP]
> If the installer menu appears again after the reboot, disconnect the ISO in the VM's CD/DVD settings and restart the VM.

<img src="images/31-complete.png" alt="Installation complete screen" width="800">

---

## 🚀 Part 4 – First Boot

### Step 32 · Log in to Kali Linux

After the reboot, log in with the **username and password you created**. Kali Linux is now ready, with its security tools available from the application menu.

Recommended first commands (open a terminal):

```bash
# Update the package lists and upgrade everything
sudo apt update && sudo apt full-upgrade -y

# Optional: better screen resizing and copy/paste between host and VM
sudo apt install -y open-vm-tools-desktop
```

---

## 🧾 Settings Cheat Sheet

| Setting | Value |
|---|---|
| VM name | `Kali Linux` |
| Guest OS | Linux → Debian 13.x 64-bit |
| Disk | 50 GB, single file |
| Memory | 4096 MB |
| Processors | 4 |
| Network adapter | NAT |
| Installer option | Graphical install |
| Partitioning | Guided – entire disk with LVM, all files in one partition |
| Desktop | Xfce |
| Tools | top10 + default |
| Boot loader | GRUB on `/dev/sda` |

---

## 🛠️ Troubleshooting

<details>
<summary><b>The VM does not boot into the installer</b></summary>

Open **Edit virtual machine settings → CD/DVD (SATA)** and make sure **Connect at power on** is checked and the path points to the Kali ISO.

</details>

<details>
<summary><b>The VM is slow or freezes</b></summary>

Give it more memory (4 GB or more) and make sure your computer has enough free RAM. Close other heavy applications while the VM runs.

</details>

<details>
<summary><b>The installer keeps appearing after reboot</b></summary>

The ISO is still attached. Power off the VM, disconnect the ISO under **CD/DVD (SATA)**, and power it on again.

</details>

<details>
<summary><b>The screen is small or copy/paste does not work</b></summary>

Install the VMware guest tools inside Kali: `sudo apt install -y open-vm-tools-desktop`, then reboot.

</details>

<details>
<summary><b>I am on a Mac with an M-series chip</b></summary>

VMware Workstation Pro runs on Windows and Linux hosts. On Apple Silicon, use the ARM64 Kali image with a Mac-compatible hypervisor, and follow that tool's own setup steps.

</details>

---

## ⚖️ Responsible Use

Kali Linux contains powerful security tools. Use them **only on systems you own or have explicit written permission to test**. Unauthorized testing is illegal.

---

<div align="center">

If this guide helped you, please consider giving the repository a ⭐

</div>
