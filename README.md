## find_content [![HitCount](http://hits.dwyl.io/GiovaLomba/wd.svg?style=plastic)](http://hits.dwyl.io/GiovaLomba/find_content)

It looks for files into the target location whose content matches the 
given pattern. The name `find_content` has been chosen keeping account
of the comprise between having a meaningful name and typing laziness.

#### Why YAST (Yet Another Search Tool)?

Looking for files is easy, looking into files it's a bit less easy.
Personally I've not very clear all assumptions and configuration the
modern operating systems and their shipped utilities apply during
content search. So, to be in control, here are some reason:

+ **Flexibility**: I can search patterns into binaries maybe using
  regex.
+ **Filtering**: Metadata filtering, creation, access, edit, file size,
  ecc.
+ **Control**: Knowing exactly what is happening controlling verbosity.
+ **Multiprocessing**: You can feel a bit like the gladiator when: *At
  my signal, unleash hell!*
+ **BS 1**: I wanted to revamp and improve a more than five year old
  search software.
+ **BS 2**: I could do it, so I did it.

#### Reasonable defaults?

The following is a list (not necessarily exhaustive) of settings the 
software application implements as defaults behaviours:

-  It skips binary files.
 - It skips files greater than `100MB`.
-  By default it uses `1` single process in a sequential fashion.
 
 You knows: *good fences make good neighbours!*
 
#### How does it works?

Here you can learn about the features the `find_content` application
exposes to the users, how and when should they be used.

```
(c) 2019 Giovanni Lombardo mailto://g.lombardo@protonmail.com
find_content version 1.0.0

usage: find_content [-h] [-b] [-e [EXTS [EXTS ...]]] [-sd [SD [SD ...]]]
                 [-sf [SF [SF ...]]] [-gt [SGT]] [-lt [SLT]] [-bf [BEFORE]]
                 [-af [AFTER]] [-ac] [-ae] [-aa] [-p [PROC]] [-v]
                 [location] [pattern]

It looks for files into the target location whose content matches the given pattern.

defaults behaviours:
 - skip binary files.
 - skip files greater than 100MB.
 - #cpu parallel processes.

positional arguments:
  location              The location to look for matching items.
  pattern               The pattern to look for into items content.

optional arguments:
  -h, --help            show this help message and exit
  -b, --binary          Allows searching into binary files.
  -e [EXTS [EXTS ...]], --extensions [EXTS [EXTS ...]]
                        The list of file extensions to be considered (others are skipped).
  -sd [SD [SD ...]], --skip-dirs [SD [SD ...]]
                        The list of directory patterns that will be ignored.
  -sf [SF [SF ...]], --skip-files [SF [SF ...]]
                        The list of file patterns that will be ignored.
  -gt [SGT], --skip-gt [SGT]
                        The maximum size (in B) of considered files (others are skipped).
  -lt [SLT], --skip-lt [SLT]
                        The minimum size (in B) of considered files (others are skipped).
  -bf [BEFORE], --before [BEFORE]
                        The 'before' reference date in the format %Y-%m-%d %H:%M
  -af [AFTER], --after [AFTER]
                        The 'after' reference date in the format %Y-%m-%d %H:%M
  -ac, --created        When given it evaluates the created attribute of selected files.
  -ae, --edited         When given it evaluates edit attribute of selected files.
  -aa, --accessed       When given it evaluates last access attribute of selected files.
  -p [PROC], --processes [PROC]
                        The number of processes to start for the task.
  -v, --verbose         Logs verbose output (really slow).
  
Elapsed time 'find_content':  0.001995 seconds.
```

#### Contributions [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=plastic)](https://github.com/GiovaLomba/find_content/issues)

Contributions are always welcomed. Here a reasonably short list of
things you can contribute with:

+ You find a misbehaviour (aka bug): please report the issue so that it
can be fixed and all can benefits of the fix.

+ The software has been tested only on the OS versions mentioned below:
if you use the software on other platforms and it works, please report
the fact so that the documentation can be updated.

+ You would like the application to be able to do something it does not:
please request the features, it may be even quick and easy to implement.

+ You can write tutorial on specific or uninteded usages of the software.

+ You can enrich the documentation with real usage examples and use cases.

#### Downloads

 + [Windows 10 amd64](https://github.com/GiovaLomba/find_content/raw/master/find_content.exe)
   - **MD5**        |da07de77cfd32fc876703166291c3f0a|
   - **SHA256**     |cd76e8c7395b7f477167c186bc86facee92ced0d05429b64c2479ac7f7a22fda|
   - **VirusTotal** |[VirusTotal](https://www.virustotal.com/gui/file/cd76e8c7395b7f477167c186bc86facee92ced0d05429b64c2479ac7f7a22fda/detection)|
   
   
 + [Mac OS X 10.14](https://github.com/GiovaLomba/find_content/raw/master/find_content_osx)
   - **MD5**        |731bb760759c8e7a0a8978a709101f24|
   - **SHA256**     |139904f340379b7487f9988a3d4419b339377973997c790a1d136eee91453213|
   - **VirusTotal** |[VirusTotal](https://www.virustotal.com/gui/file/139904f340379b7487f9988a3d4419b339377973997c790a1d136eee91453213/detection)|

#### Powered by

![Python](https://www.python.org/static/img/python-logo.png "Python")
<br/> 

<!--
![PyInstaller](https://www.pyinstaller.org/_images/pyinstaller-draft1c-header-trans.png)
-->
