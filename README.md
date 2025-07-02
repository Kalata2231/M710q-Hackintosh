# L380 Clover
<p align="center">
  <img src="https://github.com/user-attachments/assets/aa5c1f8e-4101-4290-8275-bb3cde5530f5" alt="L380 EFI" width="600"/>
</p>


<!-- Badges -->
<p>
  <img src="https://img.shields.io/badge/macOS-Sequoia-green" />
  <img src="https://img.shields.io/badge/license-MIT-purple" />
</p>

<p align="center">
  <strong>Status:</strong> Maintained<br>
  <strong>Version:</strong> 1.0
</p>

# ⚠️ Disclaimer
This guide is only for the Lenovo ThinkCentre M710q. I am NOT responsible for any harm you cause to your device. This guide is provided "as-is" and all steps taken are done at your own risk.

# Introduction
This EFI is made with Open Core and it works for Sequoia.

<details>
  <summary>💻 My Hardware</summary>
  
| Category  | Component                    |
|-----------|------------------------------|
| CPU       | Intel Core i5-6500           |
| GPU       | Intel UHD Graphics 520       |
| SSD       | Intel 256GB M.2 SSD          |
| Memory    | 16GB DDR4 2400Mhz            |
</details>

<details>
  <summary>📸 Photos</summary>
  
  ![P7010069](https://github.com/user-attachments/assets/5e346b60-59d2-4c5d-bf8d-dd354759a186)

</details>

<details>
  <summary>🔧 Requirements</summary>

  - Lenovo ThinkPad L380  
  - 32GB Flash Drive  
  - Windows PC with Python  
  - An internet connection  
  - MiniTool Partition Wizard  
  - Balena Etcher  
  - [Sequoia](https://www.mediafire.com/file/q0yseezc7atymon/Olarila+Sequoia+15.5+24F74.raw/file)

</details>

<details>
  <summary>💾 How to make USB</summary>

  1. Flash the `.raw` file (Sequoia) to your USB drive using **Balena Etcher**.  
  2. Open **MiniTool Partition Wizard**.  
  3. Right-click the 200MB EFI partition on the USB and select **"Assign letter"**.  
  4. Download and unzip this repository.  
  5. Delete all existing files from the USB's EFI partition.  
  6. Unzip .EFI and put the EFI folder in the EFI particion on the flash drive.

</details>

<details>
  <summary>🛠️ BIOS Settings</summary>

  Make sure the following settings are adjusted in your BIOS:

  - **Disable** Secure Boot  
  - **Disable** TPM (Trusted Platform Module)  
  - **Disable** Intel SGX (if available)  
  - **Enable** USB Boot  
  - **Enable** UEFI Boot Mode  
  - Set **SATA Controller Mode** to AHCI  
  - **Disable** Fast Boot  
  - Enable **Virtualization** (optional, for macOS performance)  

</details>

# Status
<details>
  <summary>🧩 Compatibility Status</summary>

| Feature             |Status         |Notes                                                |
|---------------------|----------------|---------------------------------------------------------|
| Bootloader (Op Core)| ✅ Working     | Stable boot with Sequoia                              |
| Graphics Accel.     | ✅ Working     | Full acceleration with Intel UHD 520                  |
| Audio               | ✅ Working     | Internal speakers and headphone jack                  |
| HDMI                | ✅ Working     | Display output and audio over HDMI                    |
| Bluetooth           | ✅ Working     | Detected and usable                                   |
| Lan                 | ✅ Working     | Works fine                                            |
| USB Ports           | ✅ Working     | All USB-A and USB-C ports function normally           |
| Sleep               | ❌Not Working  | Works fine with lid close/wake                        |
| Bluetooth           | 🔲 Not Tested  | Detected and usable                                   |
| iMessage/FaceTime   | 🔲 Not Tested  | I don't have an apple device to test it with          |
| Wifi                | 🔲 Not Tested  | I don't have wifi on the machine                      |
| Handoff/Airdrop     | 🔲 Not Tested  | I don't have wifi on the machine                      |
</details>

# Credits
Whole repository inpired by MultimediaLucario 
