# **Ubuntu-Gem5-Launchpad** 🚀  
Welcome to the **Ubuntu-Gem5-Launchpad**! This repository is your go-to guide for setting up **Linux (Ubuntu)** and the **gem5 simulator** on your system. Whether you're a student, researcher, or enthusiast, this guide will help you get started with system simulation and computer architecture in no time.

---

## **What’s Inside?**  
- 🐧 **Step-by-step instructions** to install **Ubuntu** (Linux).  
- ⚙️ A detailed guide to installing and running **gem5**.  
- 📚 **Background information** on Ubuntu, gem5, and their uses.  
- 💡 **Tips and tricks** to make the most of gem5 for research and learning.  
- 📂 **Additional Resources**: Tutorial PDFs, YouTube videos, and documentation.  

---

## **What is Ubuntu?**  
Ubuntu is a free, open-source Linux operating system based on Debian. It’s widely used for development, server management, and academic/research purposes due to its stability, ease of use, and extensive software library.

---

## **What is gem5?**  
**gem5** is a modular, open-source platform for computer architecture research. It simulates CPUs, memory systems, caches, and other hardware components. It’s used to:  
- 🧠 Test new hardware designs.  
- 🛠️ Optimize software for specific architectures.  
- 🎓 Teach computer architecture concepts.  
- 🔍 Validate hardware designs before fabrication.  

---

## **Installation Guide**  

### **1. Installing Ubuntu**  
#### **Option 1: Dual-Boot with Windows/Mac**  
Dual-booting allows you to install Ubuntu alongside your existing operating system (Windows or macOS). You can choose which OS to boot into when you start your computer.  

**Steps**:  
1. **Backup Your Data**: Before proceeding, back up all important files to avoid data loss.  
2. **Download Ubuntu ISO**:  
   Visit the [Ubuntu Desktop](https://ubuntu.com/download/desktop) website and download the latest LTS version (e.g., Ubuntu 22.04 LTS).  
3. **Create a Bootable USB**:  
   - Use tools like [Rufus](https://rufus.ie/) (Windows) or [BalenaEtcher](https://www.balena.io/etcher/) (Mac/Windows/Linux) to write the ISO to a USB drive.  
4. **Partition Your Disk**:  
   - On Windows, use **Disk Management** to shrink your existing partition and create free space (≥20GB recommended).  
   - On macOS, use **Disk Utility** to resize your partition.  
5. **Install Ubuntu**:  
   - Boot from the USB drive (restart your computer and select the USB drive from the boot menu).  
   - Follow the installation wizard:  
     - Choose "Install Ubuntu alongside Windows/macOS."  
     - Allocate disk space for Ubuntu.  
     - Create a user account and set a password.  
6. **Complete Installation**:  
   - Once installed, restart your computer. You’ll see a boot menu to choose between Ubuntu and your original OS.  

**Video Tutorials**:  
- **English**:  
  - [How to Dual-Boot Ubuntu with Windows](https://youtu.be/GXxTxBPKecQ)
  - [How to Dual-Boot Ubuntu with macOS](https://youtu.be/KIgxEEzT9ek)  
- **Persian**:  
  - [نصب اوبونتو به صورت Dual-Boot با ویندوز](https://youtu.be/oRC4jNQrnMU)  
  - [نصب اوبونتو به صورت Dual-Boot با مک](https://it-planet.ir/8527)  

#### **Option 2: Virtual Machine (VM)**  
If you don’t want to dual-boot, you can run Ubuntu inside a virtual machine using tools like VirtualBox or VMware.  

**Steps**:  
1. **Install VirtualBox/VMware**:  
   Download [VirtualBox](https://www.virtualbox.org) or [VMware Workstation Player](https://www.bing.com/ck/a?!&&p=8ad9b8648572845286d19d466e3e083481ab665931a504d74c6f90bd8308e171JmltdHM9MTc0MDcwMDgwMA&ptn=3&ver=2&hsh=4&fclid=0da4df0f-03c4-6b03-1b37-cb2002a46a21&psq=VMware+Workstation+Player.&u=a1aHR0cHM6Ly9ibG9ncy52bXdhcmUuY29tL3dvcmtzdGF0aW9uLzIwMjQvMDUvdm13YXJlLXdvcmtzdGF0aW9uLXByby1ub3ctYXZhaWxhYmxlLWZyZWUtZm9yLXBlcnNvbmFsLXVzZS5odG1s&ntb=1).  
2. **Create a New VM**:  
   - Allocate RAM (≥4GB) and disk space (≥20GB).  
   - Mount the Ubuntu ISO and complete the installation.  

#### **Post-Installation Setup**  
Update your system and install essential tools:  
```bash
sudo apt update && sudo apt upgrade  # Update packages
sudo apt install build-essential git python3  # Essential tools
```

---

### **2. Installing gem5**  
#### **Step 1: Install Dependencies**  
Run the following commands to install all required dependencies:  
```bash
sudo apt install build-essential git m4 scons zlib1g zlib1g-dev \
libprotobuf-dev protobuf-compiler libprotoc-dev libgoogle-perftools-dev \
python3-dev python3-pip python-is-python3
```

#### **Step 2: Clone the gem5 Repository**  
Clone the official gem5 repository:  
```bash
git clone https://github.com/gem5/gem5.git
cd gem5
```

#### **Step 3: Build gem5**  
Build gem5 for your desired architecture (e.g., ARM, X86):  
```bash
# Build for ARM (example, replace with X86 if needed)
scons build/ARM/gem5.opt -j4  # Use "-jN" where N = number of CPU cores
```

#### **Step 4: Test gem5**  
Run a simple test to verify the installation:  
```bash
build/ARM/gem5.opt configs/example/se.py --cmd=tests/test-progs/hello/bin/arm/linux/hello
```

**Video Tutorials**:  
- **English**:  
  - [How to Install and Run gem5](https://youtu.be/d59ct6SYmzg)  
  - [Introduction to gem5 Simulation](https://youtu.be/n-jeY_tWzVY)  
- **Persian**:  
  - [نصب و راه‌اندازی gem5](https://www.aparat.com/v/6L0mK/)  
---

## **Additional Resources**  
### **Linux (Ubuntu) Tutorials**  
- **PDFs**: Check out the `docs/ubuntu-tutorials` folder in this repository for beginner-friendly guides.  
- **YouTube Videos**:  
  - **English**: [Ubuntu Beginner’s Guide](https://www.youtube.com/watch?v=XYZ)  
  - **Persian**: [آموزش اوبونتو برای مبتدیان](https://www.youtube.com/watch?v=XYZ)  

### **gem5 Tutorials**  
- **PDFs**: Explore the `docs/gem5-tutorials` folder for detailed documentation and guides.  
- **YouTube Videos**:  
  - **English**: [gem5 Simulation Tutorial](https://www.youtube.com/watch?v=XYZ)  
  - **Persian**: [آموزش شبیه‌سازی با gem5](https://www.youtube.com/watch?v=XYZ)  

---

## **License**  
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.  
