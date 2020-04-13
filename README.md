# AMD Radeon R7 370 / AMD Radeon R9 270 - Graphics Support for Hackintosh

***I completely drop using this Graphics card. Because In catalina, new APFS file system has change the way it's support. Before the macOS system file had only one system volume, now in catalina the main boot files has been moved to the whole new read-only volume. So, there is lot of trouble to mount that volume and place those kext inside the Extension folder. It's possible to support but you have to figure out those problems.***

***OR, if you want to run macOS < Catalina then you just follow the guide and you're done!*** 


[Lilu kext]: https://github.com/acidanthera/Lilu/releases
[Whatevergreen kext]:https://github.com/acidanthera/WhateverGreen/releases

![AMD Radeon R7 370](https://github.com/rabbidwan/amd-r7_r9-qe-ci/blob/master/image/example.png)

### Instructions:

Go to Finder. Now, open the path (S/L/E) = HDD/System/Library/Extensions. Copy 3 kext below named: 

+ AMD7000Controller.kext
+ AMDRadeonX4000.kext
+ AMDRadeonX4000HWServices.kext

Create a folder in Desktop & paste them. 

---



Now, show content with right click each kext files. 

#### - AMD7000Controller.kext

Go inside & edit **info.plist** with any text editor. find out **"IOPCIMatch"** which is on the top & bottom positioned. Then change one string value with your device id example **(r7: 0x68111002)**.  Save it.

#### - AMDRadeonX4000.kext

Same way as first one edit **info.plist** and find this **"AMDPitcairnGraphicsAccelerator"** . Now, change string value with device id as like first one **"IOPCIMatch"**. Save it.

#### - AMDRadeonX4000HWServices.kext

Same way as second one edit **info.plist** and find this **"AMD Radeon X4000 SI Services"** . Now, change string value with device id as like first one **"IOPCIMatch"**. Save it.

---



Now, Repair Kext with ~~(Deprecated but still handy in below all version of Catalina. You may struggle to mount the read-only volume which in "Catalina")[Kext Utility](http://cvad-mac.narod.ru/index/0-4)~~ [Hackintool](https://github.com/headkaze/Hackintool). Hackintool is now a days the best tool for audio, video, graphics, pcie devices patching, reparing kext, always makes your system keep up-to-date. 

Restart PC & Enjoy! 🙂



### 👉 [***P.S - Make sure Lilu.kext & Whatevergreen.kext must be the latest version in EFI folder***]

### For OpenCore Development:
---

So, what is OpenCore?
> OpenCore is completely new way to boot up the macOS system. It is blazingly fast to boot and kind of work like a native macOS. 

**_And It is highly not recommended for beginners or new to hackintosh because lot of things setup, configure plist file manually. Well if you want to try it out make sure backup your EFI files. Then you can follow lot of youtube tutorials step by step to make your system up._**

To setup vanilla opencore follow the guide: [OpenCore Guide](https://khronokernel-2.gitbook.io/opencore-vanilla-desktop-guide/)

### Graphics support
---

**In Catalina or later Catalina, we don't know which graphics to support or drop the support. With this graphics card, every macOS version need to support following this guide. So, it's a huge pain to do support the every macOS version. That's why 
I'm sharing the guide which graphics card works oob(_OUT OF THE BOX_) and LTS means you don't need to do anything to support graphics card. Just plug and play.**

Follow the GPU Buyers guide: (https://khronokernel-3.gitbook.io/gpu-buyers-guide/)


# Thank You
