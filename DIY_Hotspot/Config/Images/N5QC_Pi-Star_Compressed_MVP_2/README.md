# 🧩 Custom Raspberry Pi Image: PiStar_MVP_2

This is a custom Raspberry Pi system image for **PiStar_MVP_2**, tailored for specific configurations and optimized to fit on an **8 GB microSD card**.

## 📦 What's Included

- Pre-configured Raspberry Pi OS  
- Custom scripts, services, and settings  
- Compressed using [PiShrink](https://github.com/Drewsif/PiShrink) for minimal size  
- Automatically resizes filesystem on first boot  

## 💾 Installation Instructions

### 🔹 Option 1: Raspberry Pi Imager (Recommended)

1. [Download Raspberry Pi Imager](https://www.raspberrypi.com/software/)
2. Open the Imager and:
   - Click **“Choose OS”** → scroll down and select **“Use custom”**
   - Choose `pistar_MVP_2.img.xz`
   - Click **“Choose Storage”** and select your microSD card
3. Click **Write** and wait for it to finish
4. Insert the card into your Raspberry Pi and power it on

### 🔹 Option 2: Linux Terminal (Advanced)

1. Insert the microSD card and identify its device name:

   ```bash
   lsblk


Write the image to the SD card:

    xz -d -c pistar_MVP_2.img.xz | sudo dd of=/dev/sdX bs=4M status=progress && sync

    ⚠️ Replace /dev/sdX with your actual SD card device (e.g., /dev/sdb). Be careful — the dd command will overwrite the target disk.

🔐 File Integrity Check (MD5)

Verify your download by checking the MD5 checksum:

md5sum pistar_MVP_2.img.xz

Expected result:

b6086e94fa3419ea192bd7a9cebbd1c5  pistar_MVP_2.img.xz

If the checksum matches, the file is valid and uncorrupted.
📝 Notes

    This image auto-expands to fill the SD card on first boot

    Suitable for most Raspberry Pi models compatible with the base OS

    Created and maintained by [Your Name or Project Name]

    For updates or custom requests, please contact the maintainer
