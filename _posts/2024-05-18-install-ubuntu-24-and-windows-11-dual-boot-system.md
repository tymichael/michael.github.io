---
title: 'Install Ubuntu 24.04 and Windows 11 dual boot system'
date: 2024-05-18
permalink: /posts/2024/05/install-ubuntu-24-and-windows-11-dual-boot-system/
tags:
  - ubuntu
  - windows
---

# 安裝Ubuntu 24.04 與 Windows 11雙系統
原電腦是Windows 10系統、8GB記憶體、2TB硬碟空間，紀錄與分享安裝Ubuntu 24.04與Windows 11雙系統的過程
## 事前準備
 1. 16GB 隨身碟 * 3，Ubuntu、Windows開機碟與備份資料使用，建議使用8GB以上，因為安裝作業系統容量可能會超過8GB
 2. [Rufus](https://rufus.ie/en/) USB燒錄驅動，用於燒錄Ubuntu映像檔
 3. [Ubunut 24.04 ISO](https://ubuntu.com/download/desktop)
 4. [Windows 11 Installation Media Tool](https://www.microsoft.com/software-download/windows11)

## 步驟
原電腦是Windows 10系統，這邊會先使用Windows 11燒錄工具，將一個16GB隨身碟燒錄Windows 11，另一16GB隨身碟燒錄Ubuntu 24.04，把原電腦的資料備份到第三個隨身碟，使用燒錄好的Windows 11開機，安裝Windows 11作業系統，分割硬碟空間，分出Ubunut與Windows系統空間與使用者空間

1. 安裝[Windows 11 Installation Media Tool](https://www.microsoft.com/software-download/windows11)，使用工具將Windows 11映像檔燒錄到硬碟
2. 下載[Rufus](https://rufus.ie/en/)、[Ubunut 24.04 ISO](https://ubuntu.com/download/desktop)，使用Rufus工具將Ubunut 24.04映像檔燒錄到隨身碟
3. 重新開機，進入Bios，調整Windows 11隨身碟boot priority為第一個，儲存離開。
4. 進入Windows 11 boot，安裝Windows 11系統，參考[Windows 11 23H2 系統安裝教學](https://unikoshardware.com/2023/12/install-windows-11-23h2-home.html)，分割硬碟空間，分出Windows與Ubuntu系統空間與使用者空間
    * Windows系統空間128GB
    * Windows使用者空間896GB
    * Ubuntu空間1024GB
4. 重新開機，進入Bios，調整Ubunut 24.04隨身碟boot priority為第一個，儲存離開。
5. 進入buntu 24.04 boot，安裝Ubuntu 24.04，分割硬碟
    * SWAP：16GB，是記憶體的2倍
    * 根目錄：1008GB，系統與使用者空間
6. 安裝完成，自己常用Ubuntu，Bios調整Ubuntu的boot priority為第一個
7. 若要切換Windows 11系統，使用Ubuntu grub，開機後第一個畫面可以切換Windows boot system

## 參考
1. [Windows 11 Installation Media Tool](https://www.microsoft.com/software-download/windows11)
2. [Ubunut 24.04 ISO](https://ubuntu.com/download/desktop)
3. [Rufus](https://rufus.ie/en/)
4. [Windows 11 23H2 系統安裝教學](https://unikoshardware.。com/2023/12/install-windows-11-23h2-home.html)
5. [Ubuntu與Windows的雙系統安裝教學](https://www.youtube.com/watch?v=yMHOpOuyjdc)