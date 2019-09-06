# ZZupreme Build of Franco Kernel

Here i condensed some informations about my 'just for fun project' [Franco Kernel ZZupreme Build](https://github.com/zanezam/enchilada)
which contains following little 'icing' on top of the latest version of Francos great kernel for the OnePlus 6/6T aka 'enchilada/fajita'

## Changes

* Build with Clang toolchain, [thx to nathanchance!](https://github.com/nathanchance/android-kernel-clang)
* Build with [-O3 compiler optimization](https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html)
* Added/ported good old [ZZMoove Governor](https://github.com/zanezam/cpufreq-governor-zzmoove)  
  HINT: You can change to that governor in FK-Manager by tapping on "CPU Governor"  
  on both clusters in "CPU section".
* Added a [build script](https://github.com/zanezam/enchilada/blob/zzupreme/build.sh) for easy building  
  ```bash
  Usage: ./build.sh gcc | clang | clean
  gcc   - build with gcc toolchain
  clang - build with clang toolchain
  clean - clean sources (deletes compile dir)
  ```

Detailed changelog can be found in the [Kernel Source Repo](https://github.com/zanezam/enchilada/commits/zzupreme)

## Aim

As mentioned in the introduction i actually made this kernel just for fun and to see what happens after adding a few changes.
It's always a bit subjective as it depends on the usage of the particular user but tests has shown if you are using my provided builds 
from here in combination with zzmoove governor that you in sum might get a bit 'snappier/faster' gui experience (which admittingly 
is hard to see on that alredy blazing fast device) and even more important also a better battery 'staying power' with same phone usage (!)
So this would be beneficial in two ways and i hope this is the experience you will make too if you are using it. Enjoy!

## Used GCC/Clang Toolchains

Here are the links to the toolchains i used in case you want to compile yourself:  
[Google Stock Toolchain](https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+archive/55a930690d28f7b4f4f84d23ac94b3cffc034106.tar.gz)  
[Clang Toolchain](https://android.googlesource.com/platform/prebuilts/clang/host/linux-x86/+archive/android-9.0.0_r1/clang-4691093.tar.gz) (recommended by Nathan Chancellor)

## Supported Devices and Compatibility of pre-built Images

The pre-built images i provide are 100% compatible with [Franco Kernel Manager](https://francokernel.app/) and are made to be used with the OnePlus 6 or 6T ONLY.
Features and additional functionalities are the same in this kernel as the ones in original kernel on which it's based on. So all infos about the usage with Kernel Manager 
and all other Franco Kernel related things apply here too. NOTE: You can always flash this kernel images over the original one from Franco and vice versa without the need to
prepare anything.

About OnePlus 6T support:
Due to lack of having a OnePlus 6T device the images i provide are ONLY tested on a OnePlus 6 device, however since the sources of these two devices are unified and original 
Franco Kernel supports both devices within one image it should be fine to also flash my pre-builts on a OnePlus 6T.

## Downloads

Pre-built images can be downloaded from [HERE](http://www.mediafire.com/folder/791mkwlmfklow/FK-ZZupreme-Build) and [HERE](https://www.androidfilehost.com/?w=files&flid=298769)

## Credits

Many thanks and credits to:

[Francisco Franco](https://github.com/franciscofranco) for all his great work! (kudos for the constant quality for years!)  
[Nathan Chancellor](https://github.com/nathanchance) for profound infos about building and toolchains and the rest of his great work, which also includes upstreaming of this kernel btw.!  
[TheEmpressMiaw](https://github.com/TheEmpressMiaw) for testing ZZupreme test images and ZZMoove governor! thx girl for risking it on ur one and only daily driver! much appreciated!  

## Support

Im NOT providing any support for the kernel images i build, however for the original kernel itself there is a 
[offical XDA support thread](https://forum.xda-developers.com/oneplus-6/development/kernel-francokernel-r1-18th-june-t3806062) available.
**In case of issues please BEFORE posting there flash the original Franco kernel and see if the issue is gone then, if not u can go on and post there. thx!**

## Disclaimer

IMPORTANT NOTE!! PLEASE READ IT CAREFULLY!! 

# NO WARRANTY OR SUPPORT! FLASH ON YOUR OWN RISK! #

This product includes copyrighted third-party software licensed under the terms of the GNU General Public License. Please see The GNU General Public License for the exact terms and conditions of this license. The firmware or any other product designed or produced by this project may contain in whole or in part pre-release, untested, or not fully tested works. This may contain errors that could cause failures or loss of data, and may be incomplete or contain inaccuracies. You expressly acknowledge and agree that use of software or any part, produced by this project, is at Your sole and entire risk

ANY PRODUCT IS PROVIDED 'AS IS' AND WITHOUT WARRANTY, UPGRADES OR SUPPORT OF ANY KIND. ALL CONTRIBUTORS EXPRESSLY DISCLAIM ALL WARRANTIES AND/OR CONDITIONS, EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES AND/OR CONDITIONS OF SATISFACTORY QUALITY, OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY, OF QUIET ENJOYMENT, AND NONINFRINGEMENT OF THIRD PARTY RIGHTS.
