## Cerified Flash Translation Layer (FTL) for NAND Flash

### Introduction 
----
**NAND** flash memory has been deployed in various computer systems from
embedded devices to laptops, desktops, and data centers.
It promises enormous performance gains and power savings 
relative to traditional magnetic disks while being much 
denser. 
Although flash offers a huge performance improvement, making
it as easy and efficient to use as traditional magnetic disk
drives presents a challenge. 

#### What's FTL?

1. FTL is the software/firmware between raw NAND flash and the file system.
2. FTL mainly does the address translation.
3. FTL does the wear-leveling to improve the life span of the hardware.

The storage system accessing NAND flash directly must be aware of the
complexities involved in doing so, in particular, the inability to
update data in place.  In other words, if the system wants to
overwrite the old data at a memory cell, it has to erase the entire block, which contains the cell and is possibly hundreds of KBs.
One approach to utilizing flash is through the use of flash-based file
systems, such as JFFS3, Yaffs2, UBIFS, etc. This approach, however,
requires an extensive rework of the storage system's existing
infrastructure and file system. The other, more popular approach is to
package NAND flash as a device (eg. SSD, SDCard, USB drive) that
provides a standard disk interface (eg. IDE, SATA, SAS). As flash
memory does not support overwriting data in place, flash devices
require a translation layer to map logical blocks to their locations
within physical flash memory. This layer is called the flash
translation layer (FTL).
To hide the limitation of erase-before-write, FTL redirects each write request
to an empty location in NAND flash memory that has been erased in advance,
and manages an internal mapping table to record the mapping information
from the logical address to the physical location.

#### Why should we formally verify FTL software?

1. The FTL algorithm is non-trivial.
2. Buggy software would lead to serious data damage/loss.

NAND flash has been suffering from the following inferent hardware issues: bit-error-rate, data retention, wear endurance, etc., which are becoming worse with the rapid development of hardware. The growing hardware unreliability makes the FTL software much more
complicated nowadays than what it was ten years ago.
However, the FTL software is not as reliable as we thought according to a study done recently. A large recall of Macbook Air laptops conducted by Apple Inc. in Oct. 2013 was due to serious SSD firmware bugs, technically, bugs from the FTL.

On the one hand, much work has been done about verifying file systems in the past decade, however, their research results assume that the devices underlying are functionally correct and reliable. On the other hand, few work can be found about modeling or verifying the FTL bridging NAND flash and file systems. We think that the FTL software (or firmware), growing rapidly, is definitely worth doing research to improve the reliability of NAND flash based devices.

#### What could you get from this project?

+ The way of defining FTL algorithm formally.
+ The way of specifying correctness requirement of the software.
+ The method to prove the software design.

### A simple FTL: BAST
---

##### Author: 

+ [Yu Guo](http://gy001.github.io)
+ Lei Qiao
+ Longying Yang
+ [Baojian Hua](http://staff.ustc.edu.cn/~bjhua/)

**abstract**: Flash translation layer (FTL) is a part of software running on the
NAND flash memory, which is ubiquitous in various devices.  FTL algorithm hides the complexity of NAND flash characteristics and provides a simple and standard interface like magnetic disks. In this part, we present a general and abstract formal model for FTL algorithms, define their functional correctness as refinement, and propose a verification framework. We demonstrate its use by verifying a classic FTL algorithm BAST.  Our entire development has been
formalized in the proof assistant Coq.

##### Download: 
[https://github.com/gy001/veriFTL](https://github.com/gy001/veriFTL)

##### Verify: 

```bash
$ cd veriFTL/bast0-coq
$ make Verification.vo
```
