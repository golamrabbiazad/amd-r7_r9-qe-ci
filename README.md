# AMD Radeon R7 370 / AMD Radeon R9 270 - Graphics Support for Hackintosh

[kext utility]:http://cvad-mac.narod.ru/index/0-4	"repair kexts"
[Lilu kext]: https://github.com/acidanthera/Lilu/releases
[Whatevergreen kext]:https://github.com/acidanthera/WhateverGreen/releases

![AMD Radeon R7 370](https://github.com/rabbidwan/amd-r7_r9-qe-ci/blob/master/image/example.png)

### 							Instructions:

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



Now, paste all the kext on [Kext Utility](http://cvad-mac.narod.ru/index/0-4) to repair. After finish...

Restart PC & Enjoy! 🙂



##### 👉 [P.S - Make sure Lilu.kext & Whatevergreen.kext must be the latest version in EFI folder]

