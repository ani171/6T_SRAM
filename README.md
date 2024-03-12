# 6T_SRAM

* SRAM has become a major component in many VLSI Chips due to their large storage density and small access time. SRAM has become the topic of substantial research due to the rapid development of low-power, low-voltage memory design during recent years due to increased demand for notebooks, laptops, IC memory cards, and handheld communication devices.
* 6T static random-access memory is a type of semiconductor memory that uses bistable latching circuitry to store each bit. The term static differentiates it from dynamic RAM which must be periodically refreshed. SRAM exhibits data remembrance but is still volatile in the conventional sense, that data is eventually lost when memory is not powered. 

![image](https://github.com/ani171/6T_SRAM/assets/97838595/a859c0d6-9465-4757-a292-26e9422d3f0b)

The two basic requirements of an SRAM cell can be understood as follows:
1. Read Stability: The data once read from an SRAM cell should remain stable and not be upset or altered by the read operation itself. *Read upset* refers to the unintentional alteration of data due to the process of reading. To avoid Read upset the Cell ratio β should be greater than 1 <br> 
``` Cell ratio, β ={ (W\L) pull-down transistors } / {(W\L) access transistor} ```
2. Write Stability: When data needs to be written to an SRAM cell, the cell should reliably accept the new data and update its stored value without causing read upset or other unintended changes to neighboring cells or circuitry. This ensures that the SRAM cell maintains its stability and integrity during write operations, allowing for accurate storage and retrieval of data. This is ensured by maintaining the Pull up ratio, given by <br>
```Pull-up ratio, P.R ={ (W\L) pull up transistors } / {(W\L) access transistor } ```

#### Read operation
* To read data from the cell, the wordline (WL) connected to the access transistors is activated allowing access to the storage nodes.
* If the cell is storing a logic high (1), the bitline (BL) connected to the output of the latch will be discharged to a logic low (0) due to the pull-down action of the cross-coupled NMOS transistors.
* If the cell is storing a logic low (0), the bitline will remain at logic high (1) due to the pull-up action of the cross-coupled PMOS transistors.

#### Write operation
* To write data into the cell, the bitline (BL) and wordline (WL) are appropriately controlled.
* For writing a logic high (1) into the cell, the BL is precharged to logic high (VDD) and the WL is brought to logic high (VDD) to enable the access transistors. This causes the cell to latch a logic high due to the feedback provided by the cross-coupled inverters.
* For writing a logic low (0) into the cell, the BL is discharged to logic low (0) and the WL is brought to logic high (VDD).

*With CR=1.25 and PR=0.85 using 180nm and width of pull up transistors(wp) fixed at 400nm we get*
1. Width of access transistors Wa= 470nm
2. Width of pulldown transistors Wn= 590nm

![sram](https://github.com/ani171/6T_SRAM/assets/97838595/4ce4188a-5392-4469-80a5-e8e4996d6952)

#### WRITE '0' Operation
* The write driver makes BL=0V and BL'= VDD
* Word line WL is made high

![wrie0_ckt](https://github.com/ani171/6T_SRAM/assets/97838595/855d0ea6-2893-4296-9242-ccf049b7ef06)
![write0_grp](https://github.com/ani171/6T_SRAM/assets/97838595/f8abf407-0b52-4b1d-a6df-5903cc974dfe)


#### WRITE '1' Operation
![write1_ckt](https://github.com/ani171/6T_SRAM/assets/97838595/18d6f70d-b7cc-4bf7-9848-7b6cf3c87529)

![write1_grph](https://github.com/ani171/6T_SRAM/assets/97838595/537f7e2c-05f3-4729-a61a-8f6df186ffd8)


#### READ '0' Operation
![read0_ckt](https://github.com/ani171/6T_SRAM/assets/97838595/7b1c5840-49f5-4023-a3d2-1ab6a572aff4)
![read0_grph](https://github.com/ani171/6T_SRAM/assets/97838595/c9602683-0414-4a32-83f5-e9ac9df390af)


#### READ '1' Operation
![read1_ckt](https://github.com/ani171/6T_SRAM/assets/97838595/709a0593-f62b-49c2-935d-a37b161d9cc2)
![read1_grp](https://github.com/ani171/6T_SRAM/assets/97838595/e7b3e763-ff21-44a5-829c-ac2f5be668c4)
