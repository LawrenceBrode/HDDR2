
# hDDR2

> **handmadeDDR2** | "Double Data Rate 2"

##### Why?
###### Becouse I Can.

> NOTE: With this article I am not providing academic study material but
> simply a summary that can be understood even by a novice. A detailed
> explanation would take several hours and days to understand.


## What is the RAM?
You are supposed to know what the f..k a RAM is if you are reading this.
### How (modern) RAM works?

 
|Structure					|Explanation|
|-									|-|
|Memory Channel		|The memory channel control the "set" of DIMM's|
|DIMM						|The DIMM (Dual In-Line Memory Module) is the "RAM MODULE"|
|Rank							|The Ranks are the faces of the DIMM where a set of DRAM	chips are placed|
|Bank							|Each DRAM chip is devided into several "sectors" that can be imagined as chips|
|Row							|The row can be compared to the traditional "address" of a RAM chip or the row of a notebook|
|Column						|The Column can be compared to an additional address that define the memory location in a "2D" place, as a matrix|

### Let's try to address a DRAM chip (B-R-C | Bank-Row-Column)
For this example we are going to use a [winbond 512 Mbit DDR2](https://github.com/LawrenceBrode/HDDR2/blob/d97dd640fa0fb63eee98a2fcc034407cdeb084aa/DATASHEETS/2304140030_Winbond-Elec-W9751G6NB-25_C908414.pdf) chip.
This is a 64MB (512 Mbit) DDR2 chip with transfer rates up to 1066 Mbps (DDR2-1066).
It store DATA in a 16 bit length so for a 64 bit CPU architecture we would just need 4 chip paired and we would archive a total of 256 MB DDR2 module.
If we would had a 8 bit DATA length we would need to pair 8 chips.

![W9751G6NB DESCRIPTION](https://raw.githubusercontent.com/LawrenceBrode/HDDR2/407b1c770dfbab35c849f52770f4a09ed2ac064d/img/Screenshot%202024-04-08%20231550.png)

#### W9751G6NB

|BANK|ROW|COLUMN|
|-|-|-|
|4 BANKS (2 BIT ADDRESS)|8192 ROWS (13 BIT ADDRESS)|1024 COLUMNS (10 BIT ADDRESS)|

![ADDRESSES](https://raw.githubusercontent.com/LawrenceBrode/HDDR2/main/img/Screenshot%202024-04-08%20231639.png)

> Simple math: total addressing is: 33'554'432 addresses =
> BANKSxROWSxCOLUMNS

###### WHY? BANKS->2 BIT	|	ROWS->13 BIT|		COLUMNS->10 BIT| 	TOTAL->25 BIT ADDRESS-> 2^25=33'554'432 LOCATIONS

If we want to find the total memory size we just have to multiply locations per data width -> 33'554'432 x 16 = 536'870'912 bits -> /8 -> 67'108'864 Bytes -> 64 MB

**Simple? Yes.**

