# ZZupreme Kernel Builds

Here i condensed some informations about my 'just for fun projects' [Franco Kernel ZZupreme Build](https://github.com/zanezam/enchilada)
(for OOS9 and **meanwhile obsolete!**) and [blu_spark Kernel ZZupreme Build](https://github.com/zanezam/op6) (for OOS10, **actively maintained**) which contains following
little 'icing' on top of the corresponding latest version of [Francisco Francos](https://github.com/franciscofranco) and [eng.stk's](https://github.com/engstk)
great kernels for the OnePlus 6/6T aka 'enchilada/fajita'

## Changes

* [Upstreamed](https://github.com/android-linux-stable/notes) 4.9 kernel stable base [thx to nathanchance!](https://github.com/android-linux-stable/op6) with bue_spark kernel changes merged in (needed only with blue_spark, francos kernel was already upstreamed back then).
* Build with recent Clang/Linaro toolchains, [thx to nathanchance!](https://github.com/nathanchance/android-kernel-clang) for the useful 'Clang-infos'!
* Build with [-O3 in Clang and -Ofast compiler optimization in Linaro build](https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html).
* Fixed all possible to fix compiler/optimization related warnings (some 'dts' ones remain).
* Added/ported good old [ZZMoove Governor](https://github.com/zanezam/cpufreq-governor-zzmoove).   
  *HINT: You can switch to that governor for example with 'FK-Manager' or 'Kernel Adiutor' app by using the 'CPU Governor' section in these apps. It's however already set as default governor after boot on blu_spark kernel ZZupreme Builds via kernel init process.*
* Brought the ol' couple Zen I/O Scheduler + ZZmoove CPU Governor 'completely together again' by making Zen scheduler default on all partitions (only in blu_spark kernel)
* Added a build script for easy [building of blu_spark kernel](https://github.com/zanezam/op6/blob/zzupreme-clang/build.sh) and for easy [building of franco kernel](https://github.com/zanezam/enchilada/blob/zzupreme/build.sh)
  ```bash
  Usage:  ./build.sh gcc | linaro | clang | clean
  gcc     - buid with stock toolchain (obsolete option in blu_spark kernel)
  linaro  - build with linaro toolchain (new option in blu_spark kernel)
  clang   - build with clang toolchain
  clean   - clean sources (deletes compile dir)
  ```
Detailed changelog of corresponding ZZupreme Build kernels can be found in the [ZZupreme blue_spark kernel source repo](https://github.com/zanezam/op6/commits) and in the [ZZupreme franco kernel source repo](https://github.com/zanezam/enchilada/commits)

## Aim

As mentioned in the introduction i actually made this kernel just for fun and to see what happens after adding a few changes.
It's always a bit subjective as it depends on the usage of the particular user but tests has shown if you are using my provided builds 
from here in combination with zzmoove governor that you in sum might get a bit 'snappier/faster' gui experience (which admittingly 
is hard to see on that alredy blazing fast device) and even more important also a better battery 'staying power' with same phone usage (!)
So this would be beneficial in two ways and i hope this is the experience you will make too if you are using it. Enjoy!

## Used GCC/Clang/Linaro Toolchains

Here are the links to the toolchains i used in case you want to compile yourself:

Franco Kernel ZZupreme Builds:  
[Google Stock Toolchain](https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+archive/55a930690d28f7b4f4f84d23ac94b3cffc034106.tar.gz) (meanwhile obolete as the [clang toolchain is the new stock default!](https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+/fc97ce6abfe822403eb219dcbd1067a53c49e4f1))  
[Clang Toolchain](https://android.googlesource.com/platform/prebuilts/clang/host/linux-x86/+archive/android-9.0.0_r1/clang-4691093.tar.gz) (recommended by Nathan Chancellor)

blue_spark Kernel ZZupreme Builds:  
[Clang Toolchain](https://android.googlesource.com/platform/prebuilts/clang/host/linux-x86/+/refs/heads/master/clang-r383902/) (latest as of may 2020)  
[Linaro Toolchain](https://releases.linaro.org/components/toolchain/binaries/latest-7/aarch64-linux-gnu/gcc-linaro-7.5.0-2019.12-x86_64_aarch64-linux-gnu.tar.xz) (latest as of may 2020)

## Supported Devices and Compatibility of pre-built Images

The pre-built images i provide are 100% compatible with [Franco Kernel Manager](https://francokernel.app/) and [Kernel Adiutor](https://f-droid.org/en/packages/com.nhellfire.kerneladiutor/) and are made to be used with the OnePlus 6 or 6T ONLY.
Features and additional functionalities are the same in this kernel builds as the ones in original kernel builds on which they are based on. So all infos about the usage with 'FK-Kernel Manager' and all other Franco Kernel/blu_spark kernel related things apply here too.
*NOTE: You can always flash my provided kernel images over the original one from Franco/eng.stk and vice versa without the need to prepare anything.*

About OnePlus 6T support:  
Due to lack of having a OnePlus 6T device the images i provide are ONLY tested on a OnePlus 6 device, however since the sources of these two devices are unified and original
franco kernel/blue_spark kernel supports both devices within one image it should be fine to also flash my pre-builts on a OnePlus 6T.

## Downloads

Pre-built images can be downloaded from [HERE](http://www.mediafire.com/folder/791mkwlmfklow/ZZupreme-Builds) and [HERE](https://www.androidfilehost.com/?w=files&flid=298769)

## Credits

Many thanks and credits to:

[Francisco Franco](https://github.com/franciscofranco) for all his great work! (kudos for the constant quality for years!)  
[eng.stk's](https://github.com/engstk) for all his great work! (kudos for the constant quality and 'speedness' for years!)  
[Nathan Chancellor](https://github.com/nathanchance) for profound infos about building and toolchains and the rest of his great work, which also includes upstreaming of these kernels btw.!  
[TheEmpressMiaw](https://github.com/TheEmpressMiaw) for testing ZZupreme Builds test images and ZZMoove governor! thx girl for risking it on ur one and only daily driver! much appreciated!  

## Support

Im NOT providing any support for the kernel images i build, however for the original kernels themself there is a
[offical Franco Kernel XDA support thread](https://forum.xda-developers.com/oneplus-6/development/kernel-francokernel-r1-18th-june-t3806062) and a [offical blu_spark Kernel XDA support thread](https://forum.xda-developers.com/oneplus-6/oneplus-6--6t-cross-device-development/kernel-t3800965) available.  
**In case of issues please BEFORE posting there flash the recent original Franco/blu_spark kernel and see if the issue is gone then, if not u can go on and post there. thx!**

## Disclaimer

IMPORTANT NOTE!! PLEASE READ IT CAREFULLY!! 

# NO WARRANTY OR SUPPORT! FLASH ON YOUR OWN RISK! #

This product includes copyrighted third-party software licensed under the terms of the GNU General Public License. Please see The GNU General Public License for the exact terms and conditions of this license. The firmware or any other product designed or produced by this project may contain in whole or in part pre-release, untested, or not fully tested works. This may contain errors that could cause failures or loss of data, and may be incomplete or contain inaccuracies. You expressly acknowledge and agree that use of software or any part, produced by this project, is at Your sole and entire risk

ANY PRODUCT IS PROVIDED 'AS IS' AND WITHOUT WARRANTY, UPGRADES OR SUPPORT OF ANY KIND. ALL CONTRIBUTORS EXPRESSLY DISCLAIM ALL WARRANTIES AND/OR CONDITIONS, EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES AND/OR CONDITIONS OF SATISFACTORY QUALITY, OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY, OF QUIET ENJOYMENT, AND NONINFRINGEMENT OF THIRD PARTY RIGHTS.
