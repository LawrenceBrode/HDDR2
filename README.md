# hDDR2

> **handmadeDDR2** | "Double Data Rate 2"

##### Why?
###### Becouse I Can.

> NOTE: With this article I am not providing academic study material but
> simply a summary that can be understood even by a novice. A detailed
> explanation would take several hours and days to understand.


## What is the RAM?

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
