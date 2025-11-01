# wmt_ios_study
My iOS study

## weibo record
* iOS 15.8 xcode 14.1 device debug
```
经过最近几天的研究，我成功搭建了一个xcode 14.1开发环境来编译安装iOS程序到iphone7plus上，
iOS版本15.8，这是可行的，而且我查过也有人成功用xcode 14.2真机调试
（1）需要appleid签名，即便是闭源也可以appleid签名，越也要appleid，非越安装ipa也需要appleid
（2）现在可以便宜买到的常见的有iphone4s，iphone6，iphone7plus，如果想真机调试的话不建议买iphone4s
（不知道为什么会连不上macos），但iphone4s（iOS9）有好处是支持32位，
但iphone6和7（iOS15.8）都不支持了
（3）如果用xcode 14，需要macos升级到Monterey，
升完之后xcode 11和xcode 12就不能用了，大概需要3个半小时左右，下完和重启安装前需要用鼠标点确定
（4）模拟器不需要签名，真机调试需要appleid签名和在iphone上设置-通用-设备管理-信任，
另外xcode的设备支持文件夹需要把15.5（不是15.7）复制到15.8，
参考《手机升级到iOS15.8后无法在xcode(14.2)上真机调试》
```
* Copy /Appliccations/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport
from 15.5 (NOT 15.7) to 15.8  
https://blog.csdn.net/SHUIYI_24/article/details/134787232   
https://stackoverflow.com/questions/77429993/looking-for-ios-15-8-support-files-for-xcode14-214c18?noredirect=1&lq=1  
* Upgrade to macOS Monterey, to run Xcode 14.1 (or XCode 14.2)
* iPhone7Plus in iOS 15.8, but it doesn't support 32bit APP  
* If Xcode says 'because it has an invalid code signature' when device debugging, solve: Settings -> General -> VPN & Device (设置-通用-设备管理-信任)  
https://blog.csdn.net/weixin_43758377/article/details/120859650  
* Download xcode xip file from developer.apple.com, need login with appleid, search xcode 13, but actually need to download xcode 14     
https://developer.apple.com/download/all/?q=xcode%2013  
Double click xip to extract, wait for a long time, and then copy it to Applications folder (rename if need)        
