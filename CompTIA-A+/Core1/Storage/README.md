# 💾 Storage & Partitioning Lab

This lab explores the concepts of disk management, partitions, formatting, and storage expansion using VirtualBox virtual machines. 

---

## 🛠️ Lab Tasks

### 1. Add a Virtual Hard Disk

- In VirtualBox:
  - Attach a **new virtual hard disk** (10–20 GB, dynamically allocated)

---

### 2. Boot the VM and Recognize the New Disk

**Linux:**
- Use `lsblk` or `sudo fdisk -l` to view all attached drives
- You should see `/dev/sdb` (or similar)

**Windows:**
- Use `diskmgmt.msc` to open Disk Management
- You’ll be prompted to initialize the new disk (choose GPT)

---

### 3. Partition and Format the Disk

**Linux (Ubuntu):**
```bash
sudo fdisk /dev/sdb
# Create new partition, write changes

sudo mkfs.ext4 /dev/sdb1  # Format as ext4
sudo mkdir /mnt/storage
sudo mount /dev/sdb1 /mnt/storage
