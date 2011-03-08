=====================
Amino Standard Pinout
=====================

The Amino interface definition provides 2 connectors as described below

Female headers that support the blades, view from the top

Secondary extended header (8bit) available on full slots

=== === 
1V  5V
D9  D10
D11 D12
CO  CK
CI  GND
=== ===

Secondary header not extended (4bit) on basic slots

=== === 
CO  CK
CI  GND
=== ===

Basic header available on all slots

=== === 
D1  D5
D2  D6
D3  D7
D4  D8
3V3 GND
=== ===

D1-D4 Are single bit digital ports configured individually as inputs or outputs

D5-D12 Can be configured as a single 8 bit or a dual 4 bit port configured either as input or outputs. These can also be reconfigured on the fly an or bitbanged.

CI,CO,CK Are digital signals enabling serial configuration of the blade and or reading of configuration/parameters/operation of the blade. They can also be used in conjunction with D1-12 in order to provide high speed synchronised input and output at multibit widths from 1 bit to 8 bit.

1.1 Pin configuration
---------------------
The configuration of the D1-D12 pins is a compromise, if an FPGA were used these pins could efficiently be used in any manner, however on MCUs and the XS1 these pinouts are driven by ports with bit width limitations. In order to maximise throughput this configuration was chosen to deliver good all round performance at the selected bit widths of 1,4 and 8.

1.2 Slot modes
--------------
It should be noted that in a 4bit slot (one without the extended connector) 8bit width ports are not available, the widest transfer width is 4bits in and out of the blade.

1.3 Digital I/O operation
---------------------
The use od the digital pins for input and output extends from basic GPIO like operation to more complex asynchronous and synchronous transfers according to blade operation.

1.4 Advanced Modes
------------------
There is also a number of optional advanced communications and extension modes for a full (8bit slot) which provide high speed intercommunication connects, some of which are architecture dependent. Where these interconnect standards are public they may be used between blades and blade holders, they may also be extended to other blades and blade holders to build distributed processing networks.


 




