# matebook-13/14-2019/2020-OpenCore-EFI  hackintosh

readme in other language:  
[中文🇨🇳](readme.md) | [日本語🇯🇵](readme-jp.md) | [English🇬🇧](readme-en.md)   


```
This project supports 2018-2020version's Matebook 13&14 (intel ver)
```


Sister project:[Matebook-D14-2020-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-D14-2020-hackintosh)  

<details> 
<summary>appology to: @Edoardo001 </summary>  
 
very much thanks to [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh)on test bigsur(beta),and i am so sorry for wasted his time,because of i did a totally wrong EFI for testing bigsur,my apology.  
 
 </details>  

Now:you can use this efi boot both catalina and bigsur now.it is steadily and worked well.  
  
<details>  
<summary>⭐️click this to check how macos works on matebook 13</summary>  
 
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88%202020-11-14%2019.30.41.png?raw=true)     
![image](https://i0.hdslb.com/bfs/article/0d73e23780c4a4a5b80b1e956dc8957bb95f3372.jpg@1320w_880h.webp)  
![image](https://i0.hdslb.com/bfs/article/3c89fd7615510c1b2e9efa1c6024348b4b635abc.jpg@1320w_1760h.webp)  

</details>   

Report & Feedback：[issues](https://github.com/ske1996/matebook-13-2019-oc-efi/issues)  

  
EFI download：[releases](https://github.com/ske1996/matebook-13-2019-oc-efi/releases)  

**If you Star my repo (click star⭐️ at upper right of this page), I will so happy.**  


A telegram group in ：https://t.me/hackintosh_matebook13  




## Update log:  

<details>  
<summary>click for details</summary>  

- 20201113:  
Upgraded all Bigsur version's EFI to OpenCore 0.6.4，Supported Bigsur 11.0.1 Public Release  

- 20201106:  
Upgraded OpenCore which is for MB13/14 2018-2019(BigSur ver) to 0.6.3  

- 20201031:  
Upgraded OpenCore which is for MB13/14 2018-2019(BigSur ver) to 0.6.2  
 

- 20200918:  
deleted two fakepcid kexts and some other things，now efi is very clean，and try to fix wifi-bluetooth conflict issue    


- 20200917:  
upgrade oc to 0.6.1,and removed itlwm.kext,added AirportItlwm.kext,heliport is not necessary now  
you need to download correct version for efi,it according to your os version.   
 
- 20200916:  
delete more useless kext and ssdt,this version will take less ram,and upgrade opencore to 0.6.1  

 
 
- 20200905:    
added something interesting+SMCLightSensor.kext  


  
  
- 20200822:    
Deleted some useless ssdt.  

- 20200814:  
Rebuild some ssdt make it more compact.  
and you can use this efi boot both catalina and bigsur now.it is steadily and worked well.  

- 20200806:  
Upgrade OpenCore to official 0.6.0  


- 20200802:  
updated itlwmx.kext for 2020ver laptop,[click for download](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/itlwmx%20beta0802.zip)  

    
- 20200728:  
added public beta of itlwm.kext and heliport  

- 20200725:  
Support Macos 10.15.6  

- 20200724:  
upgrade opencore to 0.5.9  


- 20200715:  
audio jack fixed,thanks randomprofilename  

- 20200712:  
this efi could be used in matebook 13/14 2019  
and under 2020 version likes:  
except wifi couldnt be load,everything is as same as 2019 version,works fine.  
the reason might be the 2020 version use 2gen ac9560,maybe can be fixed in future.


- 20200710:  
add a clover efi be used to install macos,  
this clover efi could be used to boot your hackintosh,too  
But I strongly recommand to use opencore(oc) efi to boot your device.  


</details>  

Supported BigSur  

## Works fine：
  
  
1.bluetooth From IntelBluetoothFirmware [@zxystd](https://github.com/OpenIntelWireless/itlwm)  

2.wifi (added AirportItlwm from [@zxystd](https://github.com/OpenIntelWireless/itlwm) you can use wifi without heliport now)  


3.sleep-wakeup works well

<details>  
<summary>4.hdmi（audio of hdmi,too））*click</summary>   
  
⭕️MataBook 13 2018-2020 you dont have to do anything  
❌MataBook 14 2019-2020 the Framebuffer part of config.plist ⇨ should be changed to this：[Plan A](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/49) |  [Plan B](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/121)   
but there are some cases which they havent changed anything in config.plist,and their device's hdmi works fine.  
so,if your device's hdmi works,strongly recommand to NOT change anything of config.plist(except MLB,SN)  

 </details>   

5.TrackPad

6.perfect powermanagement(after disable cfg lock)  

7.igpu(uhd620) works well

8.cpu boost（cpufriend set in：1800mhz，maximum）

9.usb（by ssdt）

10.FN key(brightness and sound)  

11.audio jack (need to use 【Install ComboJack to fix audio jack】under this page) 


  
  
## Doesnt work：  


1. Camera（UVC Camera VendorID_1480 ProductID_975 is available）  
*If you need a workable webcam,buy Logicool c270,I'm using it,pretty good.  


2. mx250/150/350（hopeless）

  
## Info of my device     


oc version:0.6.4  

macos: BigSur 11.0.1 Public Release  

matebook13 2019 i7-8565u mx250 sn720  


## About installation

<details>  
<summary> How to install：</summary> 

A perfect guide in:  

https://dortania.github.io/vanilla-laptop-guide/preparations/installer-overview.html  



</details>  



<details>  
<summary> How to create dual boot：</summary> 

[click to download the guide](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/A%20guide%20for%20dualBoot%20of%20Matebook13%20from%20%40Francisco%20Novoa.pdf)  

Thanks [@Francisco Novoa(from Chile🇨🇱)](https://t.me/hackintosh_matebook13/8557) and this dual-boot guide is written by him   


</details>  

<details>  
<summary>For someone who wants to run BigSur on his/her device</summary> 


1. OTA works for upgrading to BigSur from Catalina  
2. However you want to install BigSur on your device,I recommand you to unlock CFG at frist for avoiding some problem you maybe will get.  
3. Before you upgrade your osx to BigSur from Catalina,you should remove your EFI in you ESP partition and switch to BigSur version EFI which is publiced in my [release](https://github.com/ske1996/matebook-13-2019-oc-efi/releases).  




</details>  


## After installation

<details>  
<summary>⚠️Warning</summary>  
⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️  
  
1.DO NOT BOOT YOUR WINDOWS OR OTHER OS WITH OpneCore.  
you may lose your Genuine license,except you know how to inject your own correct UUID/MLB/SN in config.plist.  
it is not 100% happen,but it is still risky.  
you should just set Macos as defaul boot at OpenCore with pressing ctrl + enter to choose Mac partition.  
and edit config to disable "showpicker" which is at EFI/OC.  
then press F12 immediately after you press power button,and choose the option named like "windows xxxx" to boot windows with original uefi bootloader.  
Or follow that guide "how to create dual boot" upper this page.  


2.You should edit the config.plist to customize MLB/SN/UUID which is unique before you start to use your laptop as daily pc.  

3.Do not enable "serch my mac" in setting.  

4.Do not enable "file vault" in setting.  


</details>  



<details>  
<summary>Install ComboJack to fix audio jack  </summary>  
  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/audiojack.png?raw=true)  


From Heporis:  

https://github.com/randomprofilename/ComboJack


run install.sh in terminal:  

```bash
ComboJack_Installer/install.sh
```
  
</details>     



<details>  
<summary>How to enable HIDPI：</summary>  
 
⚠️Attention：  
according to your OS version,the program which you will use is different.        
BigSur：[click to download](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/Bigsur/%EF%BC%88BigSur%E6%96%B9%E6%A1%882%EF%BC%89hidpi.zip)  
Catalina：https://github.com/xzhih/one-key-hidpi  

 

My selection：  
1. enable HiDPi (with patch/inject EDID)ーーーーーーーselete "2" at frist step
2. macbook pro   
3. input 6    
4. input  1600x1066 1343x895 2160x1440  



You should lock your resolution to 1343x895 at setting since you enabled HiDPI.Otherwise you will get bug from wakeup.  


*Attention⚠️you should select resolution like left part of this photo(1343x895 under the monitor),but the correct button(right part of photo) maybe not same as this photo.   


![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5q01OKCJFpwjG8DeWk34ZAlT4PiIkTwV7VOQNDBpBB7OkqG1Id2.r35y0gnRAtugvhPBj1i6J0*cx1bGL996lhQ!/b&bo=NAV8AwAAAAADB2w!&rf=viewer_4)  

*Attention⚠️you should select resolution like left part of this photo(1343x895 under the monitor),but the correct button(right part of photo) maybe not same as this photo.  



</details>     
  

<details>  
<summary>How to disable CFG lock：</summary>  

✨For perfect power management and smooth boost  
if you got unnormal cpu boost issue or overheating issue,i recommand to do this  

upgrade your bios to 1.28,could be download in HUAWEI's official page  

1.Format a usb stick to fat32  

2.create a new floder named "EFI" at root  

3.create a new floder named "BOOT" At /EFI  

4.download [cfgunlock.zip(click)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)  

5.copy bootx64.efi from cfgunlock.zip to EFI/BOOT in your usb 

Restart and boot with this usb  

After you boot   

Press alt and "＝" in same time  
(BTW,my keyborad is standard USA version,the hot key is not same between different language version keyboard,so strongly recommand to get an external USA version keyborad for this guide)  

And use ↑and↓ in your keyboard to find "cpusetup"  


And press enter in keyboard to enter "cpusetup"  


You will see this.  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/RU.jpg?raw=true)

  
0030-0E in your computer must be 01  

Use ←→↑↓ key to pick it and press enter  

Then,put "00" in  

Then,press ctrl and w in same time to save setting   

If save successfully,it will tell you like"update written"(i forget what it was)  

And alt+q to quit  

Btw.DO NOT use opencore to boot what i uploaded  

You should use that usb stick to boot again for check the change is saved  
then use [propertree](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip) to change kernel/add/quirks which is at EFI/OC/config.plist of ESP partition as this picture 
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5mhOVTuQ0sSbBPmet1ZSU1zDz7zUBccaFytwrKxAqPz4ygQph98Mo9E5.JjYf6DFuuWhDZs8DFFN1ujnFI9OIz4!/b&bo=wASKAwAAAAADB28!&rf=viewer_4)  

That is all of how to unlock cfg in matebook13 2019  

And you will get a perfect power management  

</details>     
      
<details>  
<summary>Change dvmt to 64mb</summary>  
    
our dvmt is 32m in defult,and it just support hdmi to 4k30p  

and you can get 4k60p hdmi work after you unlock dvmt to 64m  

basically same as my cfg guide  

use that bootx64.efi from cfgunlock.zip,copy it to EFI/BOOT in your usb stick and boot with it  

after you boot press alt and = at same time in usa version keyboard  

use pagedown to find SaSetup and getin to it  

then press crtl and pgdown ,your screen will like that picture  
![image](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/%E6%9D%82%E9%A1%B9/dvmt64.bmp)  

change 0107 to 2 and 0108 to 3  

then crtl and w to save the change  

You should use that usb stick to boot again for check the change is saved  
then use [propertree](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip) to change DeviceProperties/Add/PciRoot(0x0)/Pci(0x2,0x0) which is at EFI/OC/config.plist of ESP partition as this picture 　
⚠️This setting of config.plist is just for matebook 13 2018-2019(maybe it works for 2020ver,too)  
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/45NBuzDIW489QBoVep5mcbvyqMw5*Y0jP8mcu7Ee3hom9v.4vLrclVXlW1qZQR3tuWj.fDrSEOF5cBubLM5p6joREA5a6pqrLmFG0msz5yg!/b&bo=0AQsAgAAAAADJ*g!&rf=viewer_4)  
  
[the inspiration of this guide from @laozhiang](https://github.com/laozhiang)  
  


</details>   

<details>  
<summary>fix time issue between windows and macos(for double boot)</summary>     
  
in windows press WIN+x run CMD with administrator  
  
  input：  
  
```bash
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```  


</details>       
  

If this EFI could run in your laptop well,  
please create a issues and send info of your device like year,cpu,matebook 13 or 14.  
for helping more people who using matebook to build their hackintosh.

## If you want to support my work：

Please donate in paypal  

[click to donate](https://paypal.me/ske1996)  

![image](https://github.com/ske1996/matebook-13-2019-oc-efi/blob/master/%E6%9D%82%E9%A1%B9/paypal.png?raw=true)  

[click to donate](https://paypal.me/ske1996)  


## Thanks：

- [@intel](https://www.intel.com/content/www/us/en/homepage.html) make cpu for us

- [@apple](https://www.apple.com/) create macos for us
 
- [@zxystd](https://github.com/OpenIntelWireless/itlwm) create kext of wifi and bluetooth  

- [@MoZyo](https://github.com/MoZyo/RedmiBook-13-10th-Gen-Intel-Hackintosh) teached me alot

- [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh)  thanks him done a remarkable job in clover version hackintosh in matebook 13

- [@Zero-zer0](https://github.com/Zero-zer0) learned how to fix brightness key from him
