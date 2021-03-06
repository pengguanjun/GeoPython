Title: GeoPython,a project of using Python for geology related daily work
Date: 2016-12-18 16:20
Category: Python


# [GeoPython, a Python tool set for geology related daily work](https://github.com/chinageology/GeoPython)



##### author: cycleuser

##### email: cycleuser@cycleuser.org

##### Copyright 2017 cycleuser


|MileStone|Date|Function|
|--|--|--|
|Beginning Date|2016-07-07 6:20|TAS|
|Adding QAPF|2016-07-09 08:32|QAPF|
|Adding Wulff|2016-12-18 08:32|Wulf|
|Reconsitution|2017-03-15 15:30|Pearce and  Harker|
|Single Zircon Ce|2017-03-25 15:30|Ballard|
|Multiple Zircon Ce|2017-03-28 15:30|MultiBallard|
|Multiple Samples CIPW Norm|2017-04-3 12:30|MultiCIPW|
|NewGUI|2017-07-23 12:30|GUI Powered By PyQt5|

## Introduction

GeoPython is a project of using Python for geology related daily work. It is a set of free softwares: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.


## New GUI！




Here is a new version of GUI, that is still under development.

The files of this New GUI can be found under the [NewGUI](/NewGUI) folder.

Only a few functions are available for now, at the moment I am typing here there is only TAS and not even a whole good TAS function.

We may all know that nice things always happen gradually. So please be patient and give me some time.

I must apologize for the slow development, that is partially caused by my bad physical situation from the tumor operation at the end of last year, and mainly because my bad choice of choosing Kivy in the past. Kivy is cute and funny, but not as reliable as PyQt at all. That means I must learn to use PyQt5 from beginning to use it as the framework of the GUI of GeoPython.


The New TAS function need Data template file named as [TAS.xlsx](NewGui/TAS.xlsx)
![](img\NewTAS.png)


The New Zircon Ce function need Data template file named as [ZirconCe.xlsx](NewGui/ZirconCe.xlsx)

![](img\NewZirconCe.png)


The New REE and Trace Elements function need Data template files:
[Trace27.xlsx](NewGui/Trace27.xlsx)
[Trace37.xlsx](NewGui/Trace37.xlsx)
[REE.xlsx](NewGui/REE.xlsx)


![](img\NewTrace.png)



## [Download](https://github.com/chinageology/GeoPython/blob/master/Download.md)

## Usage Under Windows


If you are using Windows 7, there might comes an`api-ms-win-crt`related error. You needto install KB2999226 and then install the `Visual C++ Redistributable 2015`.
Of course, a sweet guy like me just packed them up and share here: [32 bit Windows7 ](https://pan.baidu.com/s/1kVwSQ95)，[64 bit WInodws7 ](https://pan.baidu.com/s/1qY34ocW).

For Windows Users, donwload the Windows version zip file and extrat the whole file into a folder, then just put your data in the correspoinding Xlsx file and double click the correspoinding main.exe and click on the function you need.

![](https://github.com/chinageology/GeoPython/blob/master/img/Usage.png?raw=true)

## Usage Under OSX

For OSX Users, Download the OSX version zip file  and then extrat to get a App file. Got into the location of  `the App`and input your data into each files then double click `the App`file. The Svg and Png generated would also be saved at the same location of `the App` , same as the Data files. I would fix this in the former versions.

![](https://github.com/chinageology/GeoPython/blob/master/img/OSXUsage.png?raw=true)




## Usage with Python


### Dependence

This module is written with Python3.4 and based on numpy, matplotlib and pandas. That means you need to install them.

You can install these packages with PIP:

```Python
pip install numpy
pip install matplotlib
pip install pandas
pip install xlrd
```

### Installation
First, you need to install `geopython` using pip:

```Bash
pip install geopython
```

Then open you python console, and enter to the location path of data files, which are the xlsx files that  you still need to download from  [here](https://github.com/chinageology/GeoPython/blob/master/DataFileSamples.zip). Then you can use geopython as the codes below:

```Bash
ipython
```

```Python
import geopython as gp

gp.Tas("tas.xlsx").read()               # TAS diagram
gp.Ree("ree.xlsx").read()              # REE diagram
gp.Trace("trace.xlsx").read()              # Trace Elemenets spyder diagram
gp.Trace2("trace.xlsx").read()              # Trace Elements spyder diagram with a nother elements sequence
gp.Qfl("qfl.xlsx").read()              # QFL tectonic diagram
gp.Qmflt("qmflt.xlsx").read()              # Qmflt tectonic diagram
gp.QapfP("qapf.xlsx").read()              # Qapf diagram for Plutonic rocks
gp.QapfV("qapf.xlsx").read()              # Qapf diagram for Volcanic rocks
gp.Polar("strike.xlsx").read()              # Wulf and Schmidt net diagram of structure data
```

Remember that you need to import the module first and then you can use the functions in it.
You need to put you data in a xlsx file in the same form as the example files.

If python told you that it cannot find a xlsx file, you must have entered to the wrong location, and you need to use the cd command to go to the path containing xlsx files that you downloaded and modiffed.

Then you only need to input the data from the file, and everything will be done.

If the data file is in the right form and nothing goes wrong, you will have three files, which will be in the same location of these xlsx files:

* a svg(Scalable Vector Graphics) file which can be modified directly in Adobe Illustrator or Corel Draw X8;


* a png (Portable Network Graphics) .


![](https://github.com/chinageology/GeoPython/blob/master/img/Sample.png?raw=true)

