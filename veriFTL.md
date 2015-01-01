# What's FTL?

1. FTL is the software/firmware between raw NAND flash and the file system.
2. FTL mainly does the address translation.
3. FTL does the wear-leveling to improve the life span of the hardware.

# Why should we formally verify FTL software?

1. The FTL algorithm is non-trivial.
2. Buggy software would lead to serious data damage/loss.
3. 

# What can you learn from this project?

+ The way of defining FTL algorithm formally.
+ The way of specifying correctness requirement of the software.
+ The method to prove the software design.