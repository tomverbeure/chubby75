
# Colorlight 5A-75B

The Colorlight 5A-75B is an evolution of the RV901T with 8 HUB75 ports that
uses a Lattice ECP5-25 chip: the LFE5U-25F with CABGA381 package to be precise.

This makes the board extremely interesting because it's supported by the Yosys and NextPnR
open-source backend flows.

The board has the following components:

* LFE5U-25F FPGA

    * [ECP5 Family Datasheet](https://www.latticesemi.com/view_document?document_id=50461)
    * [ECP5U-25 Pinout CSV](https://www.latticesemi.com/view_document?document_id=50485)
    * [Lattice Package Diagrams](https://www.latticesemi.com/view_document?document_id=213)
    * [JTAG BSDL file](https://www.latticesemi.com/view_document?document_id=50579)

        The BSDL file requires a Lattice account before it can be downloaded.


* 1 25Q16 16Mbit serial PROM for FPGA configuration

    * [Winbond W25Q16DV datasheet](https://www.winbond.com/resource-files/w25q16dv_revi_nov1714_web.pdf)
    
    Different boards will have different serial PROMs, but they're all compatible...

* 2 1M x 16bit SDRAMs (on my board, they're EtronTech EM636165-6G 166MHz)

    * [Datasheet](http://www.etron.com/manager/uploads/EM636165_34_General%20.pdf)

* 2 1Gb Ethernet PHYs (Boardcom B50612D, just like the RV901T)

* Tons of level shifters to translate from 3.3V to 5V signaling

The board has 1 unpopulated 4-pin connector with the JTAG signals and 1 unpopulated 2-pin connector with
GND and the 3.3V. This makes it extremely easy to connect a JTAG programmer to the board!

![JTAG connection](./jtag.jpg)

![OpenOCD detect ECP5 FPGA](./openocd.png)

