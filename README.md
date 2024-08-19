# Compiled Cheat Engine (x64) 7.5 DMA Plugin
Based on this repository: https://github.com/Metick/CheatEngine-DMA

## Why?
Because it's very tricky to find out how to compile it right way. 

To compile it's on your own, you have to manualy download next repositories:
1. https://github.com/ufrisk/LeechCore for **leechcore** library
2. https://github.com/ufrisk/MemProcFS for **vmm** library
3. https://github.com/cheat-engine/cheat-engine for **lua53-64** library
4. Compile them all in x64 Release mode with same Win10 SDK version
5. Put 3 lib files into corresponding plugin lib directories
6. Put all 3 compiled DLLs into **prepared empty folder**
7. Make changes in plugin source code to fix some minor compiler errors, it's easy
8. Compile plugin in Release x64
9. Put compiled **plugin.dll** file into **prepared folder** with those 3 DLLs.
10. Now copy all 4 files from **prepared folder** to CE 7.5 directory, say **Yes** to replace lua53-64.dll
11. Launch Cheat Engine 7.5 **x64** (not i386 !!!)
12. Now your added plugin will work

## Download precompiled plugin binaries
You can just skip this pain-in-ass steps and download my precompiled plugin. Just put it into CE 7.5 directory and agree to replace **lua53-64.dll**. It should work perfectly.
If not working try to install **MSVC 2022 x64 Runtime Redistributable** package from official Microsoft site.

## How to check if it works
After installing and activating plugin console window with logs will show up and when you open process list in CE to attach you will see all processess of your DMA Host PC. If you have DMA card USB connected it have to detect it immediately and list all processess of your Host PC.
