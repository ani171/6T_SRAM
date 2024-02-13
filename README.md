# 6T_SRAM

* Static Random Access Memory, is a type of volatile memory used in digital electronic devices, to store data temporarily.

![image](https://github.com/ani171/6T_SRAM/assets/97838595/1e24d746-e4f6-4ec8-836f-d078c2b16be2)

#### Read operation
* To read data from the cell, the wordline (WL) connected to the access transistors is activated allowing access to the storage nodes.
* If the cell is storing a logic high (1), the bitline (BL) connected to the output of the latch will be discharged to a logic low (0) due to the pull-down action of the cross-coupled NMOS transistors.
* If the cell is storing a logic low (0), the bitline will remain at logic high (1) due to the pull-up action of the cross-coupled PMOS transistors.

#### Write operation
* To write data into the cell, the bitline (BL) and wordline (WL) are appropriately controlled.
* For writing a logic high (1) into the cell, the BL is precharged to logic high (VDD) and the WL is brought to logic high (VDD) to enable the access transistors. This causes the cell to latch a logic high due to the feedback provided by the cross-coupled inverters.
* For writing a logic low (0) into the cell, the BL is discharged to logic low (0) and the WL is brought to logic high (VDD).
