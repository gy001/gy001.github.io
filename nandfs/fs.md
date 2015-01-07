# A new file system for NAND flash

## Background

NAND flash memory needs to be well monitored and organized so that the
upper system could work as expected. In recent [news][mr-reformat1], the
billion-dollar-worth Mars rover, Opportunity, suffered from frequent
reboots and the Earth team had to reformat its flash memory to get it
over with. Although the reformatting process isn't too risky according to
the rover operators, it is really a dreaded and ominous task compared
with reformatting your desktop computers. Since the file system on
board lacks of such functions as reporting the health of flash blocks,
worn-out blocks replacing, or bad block tolerance, the spontaneous and
undesired reboots have been an issue involving the NAND flash drive that
the team in NASA has been dealing with for a few years. Opportunity was
not the only one sufferring from NAND flash memory issues. Spirit, another
old rover had failed to mount the flash memory and all data that should have
been stored was lost, had to be reformatted to restore the functionality.

[mr-reformat1]: http://www.eteknix.com/nasas-mars-rover-resetted-wiped/

[mr-reformat2]: http://www.planetary.org/explore/space-topics/space-missions/mer-updates/2014/08-mer-update-opportunity-reboots-reformats.html

## Highlights

+ Recoverable after power-loss
+ Bad block tolerance
+ Fast mounting

## Structure

